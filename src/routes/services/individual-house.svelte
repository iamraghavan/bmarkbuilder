<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Individual House - Benchmark Builders
        </h1>
        <span class="sub-text">
          Crafting Unique Homes Tailored to Your Lifestyle.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>services</li>
          <li>Individual House</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 md-mb-50">
          <div class="services-img mb-35">
            <img src="assets/images/individual-house.avif" alt="">
          </div>
          <div class="services-title pb-24">
            <h2 class="title">Benchmark Builders - Individual House</h2>
          </div>
          <p class="desc-part pb-24">
            Welcome to Benchmark Builders - Individual House, where we turn your dream home into a reality. Our team of dedicated professionals is committed to creating homes that reflect your unique style, needs, and aspirations.
          </p>
          <ul class="check-lists3">                              
            <li>Customized home design solutions</li>
            <li>Quality craftsmanship</li>
            <li>Personalized attention to detail</li>          
            <li>Timely and efficient construction</li>          
          </ul>
          <!-- Counter Section Start -->
          <!-- Your counter section content here -->
          <!-- Counter Section End -->
          <p class="desc-part pb-50">
            At Benchmark Builders, we understand that your home is more than just a structure; it's a reflection of your identity. Our architects and builders work closely with you to design and build an individual house that suits your lifestyle and preferences.
          </p>
          <div class="row mb-60 md-mb-30">
            <div class="col-lg-6 col-md-6 sm-mb-30">
              <img class="bdru-4" src="assets/images/individual-house-1.avif" alt="">
            </div>
            <div class="col-lg-6 col-md-6">
              <img class="bdru-4" src="assets/images/individual-house-2.jpg" alt="">
            </div>
          </div>
          <!-- Testimonial Section Start -->
          <!-- Your testimonial section content here -->
          <!-- Testimonial Section End -->
        </div>
        
        <!-- Default Component -->
  
        <Comp1/>
        
      </div> 
    </div> 
  </div>
  