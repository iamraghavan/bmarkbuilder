<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Landscape Design - Benchmark Builders
        </h1>
        <span class="sub-text">
          Transforming Outdoor Spaces with Aesthetic Excellence and Precision.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>services</li>
          <li>Landscape Design</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
      <div class="container">
        <div class="row">
          <div class="col-lg-8 md-mb-50">
            <div class="services-img mb-35">
              <img src="assets/images/landscape-design.jpg" alt="">
            </div>
            <div class="services-title pb-24">
              <h2 class="title">Benchmark Builders - Landscape Design</h2>
            </div>
            <p class="desc-part pb-24">
              Welcome to Benchmark Builders - Landscape Design, where we specialize in creating captivating outdoor environments. Our team of skilled landscape designers is dedicated to turning your outdoor spaces into works of art.
            </p>
            <ul class="check-lists3">                              
              <li>Customized landscape design solutions</li>
              <li>Expertise in plant selection and horticulture</li>
              <li>Attention to detail in every aspect</li>          
              <li>Enhancing the natural beauty of your surroundings</li>          
            </ul>
            <!-- Counter Section Start -->
            <!-- Your counter section content here -->
            <!-- Counter Section End -->
            <p class="desc-part pb-50">
              Whether you're looking to create a serene garden, a functional outdoor living space, or a vibrant commercial landscape, Benchmark Builders is here to bring your ideas to life. Let us transform your outdoor space into a stunning masterpiece.
            </p>
            <div class="row mb-60 md-mb-30">
              <div class="col-lg-6 col-md-6 sm-mb-30">
                <img class="bdru-4" src="assets/images/services/services-single/ser3.jpg" alt="">
              </div>
              <div class="col-lg-6 col-md-6">
                <img class="bdru-4" src="assets/images/services/services-single/ser4.jpg" alt="">
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
  