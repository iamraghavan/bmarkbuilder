<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Exterior Design - Benchmark Builders
        </h1>
        <span class="sub-text">
          Transforming Spaces with Creative Exterior Designs.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>services</li>
          <li>Exterior Design</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 md-mb-50">
          <div class="services-img mb-35">
            <img src="assets/images/exterior-design.jpg" alt="Exterior Design">
          </div>
          <div class="services-title pb-24">
            <h2 class="title">Benchmark Builders - Exterior Design</h2>
          </div>
          <p class="desc-part pb-24">
            Welcome to Benchmark Builders - Exterior Design, where we redefine the aesthetics of your space. Our team of creative designers specializes in crafting exterior spaces that leave a lasting impression.
          </p>
          <ul class="check-lists3">                              
            <li>Unique and creative exterior designs</li>
            <li>Attention to detail in every project</li>
            <li>Integration of functionality and aesthetics</li>          
            <li>Skilled and imaginative design team</li>          
          </ul>
          <!-- Counter Section Start -->
          <!-- Your counter section content here -->
          <!-- Counter Section End -->
          <p class="desc-part pb-50">
            Benchmark Builders is your trusted partner in creating outdoor spaces that resonate with your lifestyle. From residential exteriors to commercial landscapes, we bring a blend of innovation and functionality to every project.
          </p>
          <div class="row mb-60 md-mb-30">
            <div class="col-lg-6 col-md-6 sm-mb-30">
              <img class="bdru-4" src="https://i.pinimg.com/originals/86/af/e1/86afe13bb4c7b500a5e8aa7f03f7fc66.jpg" alt="Exterior Design">
            </div>
            <div class="col-lg-6 col-md-6">
              <img class="bdru-4" src="https://img.freepik.com/premium-photo/luxury-house-architecture-drawing-sketch-plan-blueprint_691560-6473.jpg?w=826" alt="Exterior Design">
            </div>
          </div>
          <!-- Testimonial Section Start -->
          <!-- Your testimonial section content here -->
          <!-- Testimonial Section End -->
        </div>
     
        <!-- Def -->
        <Comp1/>
      
      </div> 
    </div> 
  </div>
  