<script>
  import { onMount } from 'svelte';
  import { getAuth, onAuthStateChanged, signOut } from 'firebase/auth';
  import {
    getStorage,
    ref as storageRef,
    uploadBytes,
    getDownloadURL,
  } from 'firebase/storage';
  import { push, ref as rtdbRef, set, getDatabase, onValue } from 'firebase/database';
  import { child, remove } from 'firebase/database';
  import Swal from 'sweetalert2';
  import { goto } from '@sapper/app';
  import firebaseApp from '../firebase';


let istTime = '';

function updateClock() {
  const now = new Date();
  const options = {
    timeZone: 'Asia/Kolkata',
    hour: 'numeric',
    minute: 'numeric',
    second: 'numeric',
    day: 'numeric',
    month: 'long',
    year: 'numeric'
  };

  istTime = new Intl.DateTimeFormat('en-US', options).format(now);
}

onMount(() => {
  // Update the clock every second
  const interval = setInterval(updateClock, 1000);

  // Clean up the interval on component destroy
  return () => clearInterval(interval);

  // Initial update
  updateClock();
});

  const auth = getAuth(firebaseApp);
  const storage = getStorage(firebaseApp);
  const db = getDatabase(firebaseApp);

  let project = {
    title: '',
    dmcaApproval: false,
    landApproval: false,
    buildUpArea: 0,
    unitType: '',
    projectStatus: '',
    landmark: '',
    youtubeUrl: '',
    images: [],
    elevationImages: [],
  };

  let storedData = []; // Placeholder for stored data

  
  onMount(() => {
  // Check if the user is authenticated
  onAuthStateChanged(auth, (user) => {
    if (!user) {
      goto('/admin');
    }
  });

  // Update the clock every second
  const interval = setInterval(updateClock, 1000);

  // Cleanup function to clear the interval on component destroy
  const cleanup = () => clearInterval(interval);

  // Initial update
  updateClock();

  const dbRef = rtdbRef(db, 'projects');
  onValue(dbRef, (snapshot) => {
    storedData = [];
    snapshot.forEach((childSnapshot) => {
      storedData.push({ id: childSnapshot.key, ...childSnapshot.val() });
    });

    console.log('Fetched data:', storedData); // Log the fetched data

    // You can also log the length of storedData to check if any data is available
    console.log('Data length:', storedData.length);
  });

  // Return the cleanup function
  return cleanup;
});





  const handleLogout = async () => {
    await signOut(auth);
    goto('/admin');
  };

  const handleAddProject = async () => {
  try {
    const downloadURLs = [];

    // Upload project images to Firebase Storage
    for (const file of project.images) {
      const fileName = `Projects/${project.title}/${getFormattedDate()}-${project.landmark.replace(
        /\s/g,
        ''
      )}-${file.name}`;
      const storageRefVar = storageRef(storage, fileName);
      await uploadBytes(storageRefVar, file);
      const downloadURL = await getDownloadURL(storageRefVar);
      downloadURLs.push(downloadURL);
    }

    // Upload elevation images to Firebase Storage
    for (const file of project.elevationImages) {
      const elevationFileName = `Projects/${project.title}/Elevation/${getFormattedDate()}-${project.landmark.replace(
        /\s/g,
        ''
      )}-${file.name}`;
      const elevationStorageRef = storageRef(storage, elevationFileName);
      await uploadBytes(elevationStorageRef, file);
    }

    // Save project data to Firebase Realtime Database
    const dbRef = rtdbRef(db, 'projects');

    if (project.id) {
      // If project has an ID, update the existing project
      const projectRef = child(dbRef, project.id);
      await set(projectRef, { ...project, images: downloadURLs });
    } else {
      // If project doesn't have an ID, add a new project
      const newProjectRef = push(dbRef);
      await set(newProjectRef, { ...project, images: downloadURLs });
    }

    // Reset the form after successful upload
    project = {
      title: '',
      dmcaApproval: false,
      landApproval: false,
      buildUpArea: 0,
      unitType: '',
      projectStatus: '',
      landmark: '',
      youtubeUrl: '',
      images: [],
      elevationImages: [],
    };

    Swal.fire({
      icon: 'success',
      title: 'Project added/updated successfully!',
    });
  } catch (error) {
    console.error('Error adding/updating project:', error);
    Swal.fire({
      icon: 'error',
      title: 'Error adding/updating project',
      text: 'Please try again.',
    });
  }
};


  const getFormattedDate = () => {
    const now = new Date();
    const dd = String(now.getDate()).padStart(2, '0');
    const mm = String(now.getMonth() + 1).padStart(2, '0');
    const yy = String(now.getFullYear()).slice(-2);
    return `${dd}${mm}${yy}`;
  };

  // Placeholder functions for edit and delete actions
 


  const handleEdit = async (id) => {
    // Implement edit functionality
    const projectToEdit = storedData.find((item) => item.id === id);

    // Populate the form with the data of the selected project
    project = { ...projectToEdit };
  };

  const handleDelete = async (id) => {
    // Implement delete functionality
    try {
      const dbRef = rtdbRef(db, 'projects');
      const projectRef = child(dbRef, id);
      await remove(projectRef);

      // Remove the deleted project from the storedData array
      storedData = storedData.filter((item) => item.id !== id);

      Swal.fire({
        icon: 'success',
        title: 'Project deleted successfully!',
      });
    } catch (error) {
      console.error('Error deleting project:', error);
      Swal.fire({
        icon: 'error',
        title: 'Error deleting project',
        text: 'Please try again.',
      });
    }
  };

  const handleAction = (action, id) => {
    if (action === 'edit') {
      handleEdit(id);
    } else if (action === 'delete') {
      handleDelete(id);
    }
  };


</script>

<style>
  div {
    padding: 0px 12px;
  }

  form {
    max-width: 400px; /* Adjust the width as needed */
    margin: 0 auto;
  }

  .form-group {
    margin-bottom: 15px;
  }

  label {
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  .form-control {
    width: 100%;
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    line-height: 1.5;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
  }

  .form-check {
    margin-bottom: 0.5rem;
  }

  .btn-primary,
  .btn-danger {
    width: 100%;
    margin-top: 15px;
  }


  #clock {
    font-size: 1.3rem;
    /* text-align: center; */
    
  }


  /* table */

  /* Basic Table Styles */
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

th, td {
  padding: 12px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

th {
  background-color: #f2f2f2;
}

/* Hover Effect */
tr:hover {
  background-color: #f5f5f5;
}

/* Button Styles for Edit and Delete */
.edit-btn, .delete-btn {
  padding: 8px 12px;
  margin-right: 5px;
  cursor: pointer;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
}

.delete-btn {
  background-color: #dc3545;
}

/* Responsive Table Styles */
@media (max-width: 768px) {
  table {
    overflow-x: auto;
    display: block;
  }

  th, td {
    min-width: 120px;
    box-sizing: border-box;
  }
}

</style>

<div>
  <div class="container-fluid">
    <div class="row">
      <div class="col-md-6">
        <h1 class="mb-4">Welcome to the Admin Panel</h1>
      </div>
      <div class="col-md-2 text-md-right">
        <button on:click={handleLogout} class="btn btn-danger">Logout</button>
      </div>
      <div class="col-md-4 text-md-right">
        <p id="clock">{istTime}</p>
      </div>
    </div>
  </div>
  

  <div class="row mt-4">
    <!-- Add Project Form -->
    <form class="col-md-4">
      <div class="form-group">
        <label for="title">Project Title:</label>
        <input bind:value={project.title} type="text" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="approval" class="mt-3">Approval:</label>
        <div class="form-check">
          <input bind:checked={project.dmcaApproval} type="checkbox" class="form-check-input" id="dmcaApprovalCheckbox" />
          <label class="form-check-label" for="dmcaApprovalCheckbox">DMCA</label>
        </div>
        <div class="form-check">
          <input bind:checked={project.landApproval} type="checkbox" class="form-check-input" id="landApprovalCheckbox" />
          <label class="form-check-label" for="landApprovalCheckbox">Land Approval</label>
        </div>
      </div>

      <div class="form-group">
        <label for="build_up_area" class="mt-3">Build-up Area:</label>
        <input bind:value={project.buildUpArea} type="number" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="unit_type" class="mt-3">Unit Type:</label>
        <select bind:value={project.unitType} class="form-control" required>
          <option value="">Select Unit Type</option>
          <option value="1BHK">1BHK</option>
          <option value="2BHK - 3BHK">2BHK - 3BHK</option>
          <option value="4BHK">4BHK</option>
        </select>
      </div>

      <div class="form-group">
        <label for="project_status" class="mt-3">Project Status:</label>
        <select bind:value={project.projectStatus} class="form-control" required>
          <option value="">Select Project Status</option>
          <option value="Completed">Completed</option>
          <option value="Project On Going">Project On Going</option>
          <option value="Project Kickoff">Project Kickoff</option>
        </select>
      </div>

      <div class="form-group">
        <label for="landmark" class="mt-3">Landmark:</label>
        <input bind:value={project.landmark} type="text" required class="form-control" />
      </div>

      <div class="form-group">
        <label for="images" class="mt-3">Project Images:</label>
        <input type="file" multiple accept="image/*" class="form-control" bind:files={project.images} />
      </div>

      <div class="form-group">
        <label for="elevationImages" class="mt-3">Elevation Images:</label>
        <input type="file" multiple accept="image/*" class="form-control" bind:files={project.elevationImages} />
      </div>

      <div class="form-group">
        <label for="youtube_url" class="mt-3">YouTube Video URL:</label>
        <input bind:value={project.youtubeUrl} type="text" class="form-control" />
      </div>

      <button on:click={handleAddProject} type="button" class="btn btn-primary mt-3" style="margin-bottom: 3rem;">Add Project</button>
    
    </form>

    <!-- Display Data Table -->
    <div class="col-md-8">
      {#if storedData.length > 0}
        <table class="table">
          <thead>
            <tr>
              <th>Title</th>
              <th>Build-up Area</th>
              <th>Unit Type</th>
              <th>Project Status</th>
              <th>Landmark</th>
              <th>Action</th>
            </tr>
          </thead>
          <tbody>
            {#each storedData as item, index (index)}
  <tr>
    <td>{item.title}</td>
    <td>{item.buildUpArea}</td>
    <td>{item.unitType}</td>
    <td>{item.projectStatus}</td>
    <td>{item.landmark}</td>
    <td>
      <button on:click={() => handleAction('edit', item.id)} class="btn btn-primary btn-sm edit-btn">Edit</button>
      <button on:click={() => handleAction('delete', item.id)} class="btn btn-danger btn-sm ml-1 delete-btn">Delete</button>
    </td>
  </tr>
{/each}
          </tbody>
        </table>
      {:else}
        <p>No data available</p>
      {/if}
    </div>
  </div>
</div>
