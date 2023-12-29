<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Renovation - Benchmark Builders
        </h1>
        <span class="sub-text">
          Transforming Spaces with Excellence and Creativity.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>services</li>
          <li>Renovation</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
      <div class="container">
        <div class="row">
          <div class="col-lg-8 md-mb-50">
            <div class="services-img mb-35">
              <img src="assets/images/renovation.jpeg" alt="">
            </div>
            <div class="services-title pb-24">
              <h2 class="title">Benchmark Builders - Renovation</h2>
            </div>
            <p class="desc-part pb-24">
              Welcome to Benchmark Builders - Renovation, where we breathe new life into your spaces. Our dedicated team of renovation experts is committed to delivering exceptional results, transforming your home or business into a place you'll love.
            </p>
            <ul class="check-lists3">                              
              <li>Comprehensive renovation services</li>
              <li>Attention to detail and craftsmanship</li>
              <li>Timely project completion</li>          
              <li>Customized solutions for your needs</li>          
            </ul>
            <!-- Counter Section Start -->
            <!-- Your counter section content here -->
            <!-- Counter Section End -->
            <p class="desc-part pb-50">
              At Benchmark Builders, we understand that your space is a reflection of your lifestyle. Whether it's a home makeover, office upgrade, or any other renovation project, our experts are here to enhance functionality and aesthetics. Trust us to redefine your space.
            </p>
            <div class="row mb-60 md-mb-30">
              <div class="col-lg-6 col-md-6 sm-mb-30">
                <img class="bdru-4" src="https://img.freepik.com/premium-photo/residential-house-with-tools-architect-blueprints_505080-502.jpg" alt="">
              </div>
              <div class="col-lg-6 col-md-6">
                <img class="bdru-4" src="https://img.freepik.com/premium-photo/house-construction-blueprints_190619-41.jpg?w=826" alt="">
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
  