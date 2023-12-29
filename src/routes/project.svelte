<script>
    import { onMount } from 'svelte';
    import { ref, onValue } from 'firebase/database';
    import { db } from './firebase'; // Adjust the path as needed
  
    let projects = [];
  
    onMount(() => {
      const projectsRef = ref(db, 'projects');
  
      onValue(projectsRef, (snapshot) => {
        if (snapshot.exists()) {
          projects = Object.entries(snapshot.val()).map(([projectId, project]) => ({
            id: projectId,
            ...project
          }));
        }
      });
    });
  
    export let activePage = "Home";
  </script>
  
  <style>
    /* Add this CSS to your Svelte component or external stylesheet */

/* Style for the project content */
.project-content {
  margin-top: 15px;
}

/* Style for the project inner table */
.project-inner table {
  width: 100%;
  border-collapse: collapse;
}

/* Style for table cells */
.project-inner td {
  padding: 8px;
  border: 1px solid #ddd;
}


.project-img {
  position: relative;
  overflow: hidden;
}

/* Style for the image */
.project-img img {
  width: 100%; /* Make the image fill the container width */
  height: auto; /* Maintain the aspect ratio */
  border-radius: 5px; /* Optional: Add a border-radius for a slightly rounded appearance */
  display: block; /* Ensure the image behaves as a block element */
}

/* Style for the placeholder text when no images are available */
.project-img p {
  text-align: center;
  color: #555; /* Customize the color as needed */
  padding: 10px;
  margin: 0;
}


/* Add padding and border to the project item */
.project-item {
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

/* Style for the image */
.project-img img {
  width: 100%;
  height: auto;
  border-radius: 5px;
}

/* Add icons based on your preference */


/* Style for the project title */
.project-inner td:first-child {
  font-weight: bold;
}

/* Customize the color and style of the icons */


  </style>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Projects - Benchmark Builders
        </h1>
        <span class="sub-text">
          Explore our portfolio of projects showcasing excellence and innovation.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Projects</li>
        </ul>
      </div>
    </div>
  </div>
  
 <!-- Update the HTML structure for projects -->
<div class="rs-project project-style1 gray-bg pt-120 pb-120 md-pt-80 md-pb-80">
  <div class="container">
    <div class="row">
      {#each projects as project (project.id)}
        <div class="col-lg-6 col-md-6 mb-30">
          <div class="card">
            <div class="card-body">
              <div class="project-img">
                {#if project.images && project.images.length > 0}
                  <img src={project.images[0]} alt="Project" on:error={() => console.log('Image failed to load:', project.images[0])}>
                {:else}
                  <p>No images available for this project</p>
                {/if}
              </div>
              <div class="project-content">
                <div class="project-inner">
                  <h3 class="card-title">{project.title}</h3>
                  <table class="table table-bordered">
                    <tbody>
                      <tr>
                        <th scope="row">Unit Type</th>
                        <td>{project.unitType}</td>
                      </tr>
                      <tr>
                        <th scope="row">Build Up Area</th>
                        <td>{project.buildUpArea}</td>
                      </tr>
                      <tr>
                        <th scope="row">Land Approval</th>
                        <td>{project.landApproval}</td>
                      </tr>
                      <tr>
                        <th scope="row">Landmark</th>
                        <td>{project.landmark}</td>
                      </tr>
                      <tr>
                        <th scope="row">Highlight</th>
                        <td>{project.highlight}</td>
                      </tr>
                      <tr>
                        <th scope="row">Location Highlight</th>
                        <td>{project.lochighlight}</td>
                      </tr>
                      <tr>
                        <th scope="row">Project Status</th>
                        <td>{project.projectStatus}</td>
                      </tr>
                    </tbody>
                  </table>
                </div>
              </div>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>

  
  