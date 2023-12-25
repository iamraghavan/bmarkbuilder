<!-- Projects / index file -->

<script>
    
    export let activePage = "Home"; 
    import { onMount } from 'svelte';
  import { db } from '../firebase'; // adjust the path based on your project structure
  import { ref, onValue } from 'firebase/database';

  import { goto } from '@sapper/app';

  function somefun(projectid) {
    goto(`projects/${projectid}`, { state: { value: projectid} });
  }


//   export let project;

//   const navigateToProject = (projectId) => {
//     goto(`projects/${projectId}`);
//   };

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
</script>

<div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Projects - Benchmark Builders
        </h1>
        
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Projects</li>
        </ul>
      </div>
    </div>
  </div>

  
  <div class="rs-project project-style1 gray-bg pt-120 pb-120 md-pt-80 md-pb-80">
      <div class="container">
          <div class="row">
            {#each projects as project}


    

              <div class="col-lg-4 col-md-6 mb-30">
                  <div class="project-item">
                      <div class="project-img">
                        <img src={project.images[0]} alt="Project">
                      </div>
                      <div class="project-content">  
                          <div class="project-inner">
                              <h3 class="title">{project.title}</h3>
                              
                          </div>
                          <div class="p-icon">
                            <button class="more-info-btn" on:click={(event) => {
                                event.preventDefault();
                                somefun(project.id);
                              }}>
                              More Info
                            </button>
                        </div>
                        </div>
                  </div>
              </div>
              {/each}
          </div>
      </div>
  </div>


  <style>
    .more-info-btn {
  display: inline-block;
  padding: 10px 20px;
  font-size: 16px;
  font-weight: bold;
  text-align: center;
  text-decoration: none;
  cursor: pointer;
  background-color: #4caf50; /* Green background color */
  color: #fff; /* White text color */
  border: 2px solid #4caf50; /* Green border */
  border-radius: 5px;
  transition: background-color 0.3s, color 0.3s;
}

.more-info-btn:hover {
  background-color: #fff; /* White background on hover */
  color: #4caf50; /* Green text color on hover */
}

/* Additional styles based on your design needs */
.more-info-btn-container {
  margin-top: 20px;
  text-align: center;
}
  </style>