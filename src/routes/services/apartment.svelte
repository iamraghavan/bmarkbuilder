<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Apartments - Benchmark Builders
        </h1>
        <span class="sub-text">
          Discover Exceptional Living Spaces with Benchmark Builders Apartments.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Services</li>
          <li>Apartments</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 md-mb-50">
          <div class="services-img mb-35">
            <img src="assets/images/apartment.avif" alt="">
          </div>
          <div class="services-title pb-24">
            <h2 class="title">Benchmark Builders - Apartments</h2>
          </div>
          <p class="desc-part pb-24">
            Welcome to Benchmark Builders - Apartments, where modern living meets comfort and style. Our apartments are thoughtfully designed to provide you with a perfect blend of luxury and functionality.
          </p>
          <ul class="check-lists3">                              
            <li>Modern and stylish architecture</li>
            <li>Thoughtfully designed interiors</li>
            <li>Prime locations for convenience</li>          
            <li>Amenities for a comfortable lifestyle</li>          
          </ul>
          <!-- Counter Section Start -->
          <!-- Your counter section content here -->
          <!-- Counter Section End -->
          <p class="desc-part pb-50">
            Benchmark Builders Apartments offer you a living experience that goes beyond the ordinary. Whether you're looking for a cozy studio or a spacious family home, our apartments are crafted to meet your lifestyle needs. Elevate your living experience with us.
          </p>
          <div class="row mb-60 md-mb-30">
            <div class="col-lg-6 col-md-6 sm-mb-30">
              <img class="bdru-4" src="assets/images/apartment-1.avif" alt="">
            </div>
            <div class="col-lg-6 col-md-6">
              <img class="bdru-4" src="assets/images/apartment-2.avif" alt="">
            </div>
          </div>
          <!-- Testimonial Section Start -->
          <!-- Your testimonial section content here -->
          <!-- Testimonial Section End -->
        </div>
       
        <!-- Default Content -->
        <Comp1/>
      </div> 
    </div> 
  </div>
  