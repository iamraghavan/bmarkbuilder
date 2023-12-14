<script>
    let services = [
  { title: "Architecture", link: "/architecture", image: "assets/images/BMService/architecture-image.webp" },
  { title: "Exterior Design", link: "/exterior-design", image: "assets/images/BMService/exterior-design-image.jpg" },
  { title: "Renovation", link: "/renovation", image: "assets/images/BMService/renovation-image.jpg" },
  { title: "Landscape Design", link: "/landscape-design", image: "assets/images/BMService/landscape-design-image.jpeg" },
  { title: "Individual House", link: "/individual-house", image: "assets/images/BMService/individual-house-image.png" },
  { title: "Commercial Buildings", link: "/commercial-buildings", image: "assets/images/BMService/commercial-buildings-image.png" },
  { title: "Apartment", link: "/apartment", image: "assets/images/BMService/apartment-image.jpg" },
  { title: "Villa", link: "/villa", image: "assets/images/BMService/villa-image.jpg" }
];

  </script>
  
  <style>
    /* Add your styling for the services items here */
  </style>
  
  <div class="rs-services services-style4 bg10 pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
      <div class="sec-title text-center mb-60 md-mb-40">
        <span class="sub-text sub-text3 black-color">
          
          Our Services
        </span>
        <h2 class="title black-color">
        Designing Dreams, <br> Building Realities
        </h2>
      </div>
      <div class="row">
        {#each services as { title, link, image }}
          <div class="col-lg-4 col-md-6 mb-40">
            <div class="services-item">
              <div class="services-image">
                <img src={image} alt="Images">
              </div>
              <div class="services-text">
                <div class="services-inner">
                  <h3 class="title"><a href={link}>{title}</a></h3>
                  <div class="services-btn">
                    <a class="red-btn-text" href={link}><i class="fa flaticon-right-arrow"></i></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
  