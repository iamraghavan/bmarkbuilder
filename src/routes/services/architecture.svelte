<script>
  import Comp1 from "../../components/Comp1.svelte";
  export let activePage = "Home";
</script>




<div class="rs-breadcrumbs img1">
  <div class="container">
    <div class="breadcrumbs-inner">
      <h1 class="page-title">
        Architecture - Benchmark Builders
      </h1>
      <span class="sub-text">
        Crafting Inspirational Spaces with Expertise and Innovation.
      </span>
      <ul class="breadcrumbs-area">
        <li title={`Go to ${activePage}`}>
          <a class:active={activePage === "Home"} href="/">Home</a>
        </li>
        <li>services</li>
        <li>Architecture</li>
      </ul>
    </div>
  </div>
</div>



<div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 md-mb-50">
          <div class="services-img mb-35">
            <img src="assets/images/architecture.jpg" alt="">
          </div>
          <div class="services-title pb-24">
            <h2 class="title">Benchmark Builders - Architecture</h2>
          </div>
          <p class="desc-part pb-24">
            Welcome to Benchmark Builders - Architecture, where we bring your visions to life. Our dedicated team of architects is committed to delivering top-notch design and construction solutions tailored to your needs.
          </p>
          <ul class="check-lists3">                              
            <li>Innovative architectural designs</li>
            <li>Quality construction services</li>
            <li>Commitment to client satisfaction</li>          
            <li>Experienced and skilled architects</li>          
          </ul>
          <!-- Counter Section Start -->
          <!-- Your counter section content here -->
          <!-- Counter Section End -->
          <p class="desc-part pb-50">
            At Benchmark Builders, we believe in creating spaces that inspire. Whether you're planning a new home, office, or commercial project, our architects are here to turn your ideas into reality. Let us be your partner in building the future.
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
  