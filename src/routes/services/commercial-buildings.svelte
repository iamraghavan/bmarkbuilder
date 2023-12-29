<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Commercial Buildings - Benchmark Builders
        </h1>
        <span class="sub-text">
          Elevate Your Business Space with Benchmark Builders' Expertise.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>services</li>
          <li>Commercial Buildings</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 md-mb-50">
          <div class="services-img mb-35">
            <img src="assets/images/Change-order-in-construction.jpg" alt="">
          </div>
          <div class="services-title pb-24">
            <h2 class="title">Benchmark Builders - Commercial Buildings</h2>
          </div>
          <p class="desc-part pb-24">
            Welcome to Benchmark Builders - Commercial Buildings, where we redefine business spaces. Our dedicated team of architects specializes in creating innovative and functional commercial structures that align with your brand and business goals.
          </p>
          <ul class="check-lists3">                              
            <li>Customized commercial building designs</li>
            <li>Efficient and sustainable construction solutions</li>
            <li>Focus on client-specific requirements</li>          
            <li>Proven expertise in commercial architecture</li>          
          </ul>
          <!-- Counter Section Start -->
          <!-- Your counter section content here -->
          <!-- Counter Section End -->
          <p class="desc-part pb-50">
            At Benchmark Builders, we understand the importance of a well-designed and purposeful commercial space. Whether you're planning a new office building, retail space, or any other commercial project, our architects are committed to delivering exceptional results. Let us transform your vision into a business reality.
          </p>
          <div class="row mb-60 md-mb-30">
            <div class="col-lg-6 col-md-6 sm-mb-30">
              <img class="bdru-4" src="assets/images/commercial-buildings-1.jpg" alt="">
            </div>
            <div class="col-lg-6 col-md-6">
              <img class="bdru-4" src="assets/images/commercial-buildings-2.jpg" alt="">
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
  