<!-- [projectid].svelte -->

<script context="module">
    import { getDatabase, ref, get } from "firebase/database";
    import { firebaseApp } from "../firebase";
  
    export async function preload({ params }) {
      const projectId = params.projectid;
      const db = getDatabase(firebaseApp);
      const projectRef = ref(db, `projects/${projectId}`);
      const snapshot = await get(projectRef);
      const projectData = snapshot.val();
  
      return {
        projectData,
      };
    }
  </script>
  
  <script>
  
  
    export let projectData;
  
   
  
 
  </script>
  
  <!-- Add your HTML and layout components here -->
  <!-- <h1>{projectData.title}</h1>
  <p>{projectData.landmark}, {projectData.unitType}</p>
  <img src={projectData.images[0]} alt={projectData.title} /> -->
  
  <!-- You can include additional components or HTML as needed -->

  <!-- <div class="rs-slider case-slider-style3 pt-120 md-pt-80">
    <div class="container">
       <div class="rs-carousel owl-carousel owl-loaded owl-drag" >
          <div class="owl-stage-outer">
             <div class="owl-stage" style="transform: translate3d(-3348px, 0px, 0px); transition: all 0.8s ease 0s; width: 7812px;">
                <div class="owl-item cloned" style="width: 1116px;">
                   <div class="slider-img">
                    <img src={projectData.images[0]} alt={projectData.title} />
                   </div>
                </div>
           
             </div>
          </div>
          
       </div>
    </div>
 </div> -->


 <div class="rs-project-details pt-70 md-pt-80">
    <div class="container">
       <div class="project-information mb-45">
          <div class="row">

            <div class="mx-3">{projectData.title}</div>

             <div class="col-lg-3 col-md-6 md-mb-30">
                <div class="project-content">
                   <div class="project-right-border"></div>
                   <h4 class="title">Location</h4>
                   <div class="description">
                      <p>{projectData.landmark}</p>
                   </div>
                </div>
             </div>
             <div class="col-lg-3 col-md-6 md-mb-30 pl-50 md-pl-15">
                <div class="project-content">
                   <div class="project-right-border border-two"></div>
                   <h4 class="title">Unites</h4>
                   <div class="description">
                      <p>{projectData.unitType}</p>
                   </div>
                </div>
             </div>
             <div class="col-lg-3 col-md-6 sm-mb-30">
                <div class="project-content">
                   <div class="project-right-border border-three"></div>
                   <h4 class="title">DMCA Approval</h4>
                   <div class="description">
                      <p>{projectData.dmcaApproval}</p>
                   </div>
                </div>
             </div>
             <div class="col-lg-3 col-md-6">
                <div class="project-content">
                   <h4 class="title">Status</h4>
                   <div class="description">
                      <p>{projectData.projectStatus}</p>
                   </div>
                </div>
             </div>
          </div>
       </div>
       
      
       
     
    </div>
    
 </div>



  