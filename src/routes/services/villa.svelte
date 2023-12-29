<script>
    import Comp1 from "../../components/Comp1.svelte";
    export let activePage = "Home";
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Villa - Benchmark Builders
        </h1>
        <span class="sub-text">
          Elevate Your Living Experience with Benchmark Villas.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Services</li>
          <li>Villa</li>
        </ul>
      </div>
    </div>
  </div>
  
  <div class="rs-services-single pt-120 pb-120 md-pt-80 md-pb-80">
      <div class="container">
        <div class="row">
          <div class="col-lg-8 md-mb-50">
            <div class="services-img mb-35">
              <img src="assets/images/villa.jpg" alt="">
            </div>
            <div class="services-title pb-24">
              <h2 class="title">Benchmark Villas - Luxurious Living Redefined</h2>
            </div>
            <p class="desc-part pb-24">
              Welcome to Benchmark Villas, where luxury meets tranquility. Our villas are meticulously designed to provide you with an unmatched living experience. From contemporary architecture to state-of-the-art amenities, Benchmark Villas redefine the concept of modern living.
            </p>
            <ul class="check-lists3">                              
              <li>Elegant and modern villa designs</li>
              <li>Spacious interiors with thoughtful layouts</li>
              <li>High-end fixtures and finishes</li>          
              <li>Beautifully landscaped surroundings</li>          
            </ul>
            <!-- Counter Section Start -->
            <!-- Your counter section content here -->
            <!-- Counter Section End -->
            <p class="desc-part pb-50">
              Our villas are crafted with precision, offering a perfect blend of aesthetics and functionality. Whether you're seeking a serene retreat or a stylish abode, Benchmark Villas cater to the needs of discerning homeowners. Experience the epitome of luxury living with Benchmark Villas.
            </p>
            <div class="row mb-60 md-mb-30">
              <div class="col-lg-6 col-md-6 sm-mb-30">
                <img class="bdru-4" src="assets/images/villa-1.jpg" alt="">
              </div>
              <div class="col-lg-6 col-md-6">
                <img class="bdru-4" src="assets/images/villa-2.avif" alt="">
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
  