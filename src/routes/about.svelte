<!-- AboutUs.svelte -->
<svelte:head>

<title>About us - Bench Mark Builder</title>

    <meta name="title" content="About us - Bench Mark Builder">
<meta name="description" content="Imagine your dream home! BenchMark Builders brings it to life. Trust us for quality construction. Your dream home is just a step away!">
<meta name="keywords" content="warehouse construction in chennai, construction in chennai, plots for sale in chennai,builders in chennai,plots in chennai,best builders in chennai,top builders in chennai,construction company,building construction,home construction,building company,building construction company in chennai,construction company in chennai,chennai construction ,constructions in chennai">
<meta name="robots" content="noindex, nofollow">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<meta name="language" content="English">
<meta name="revisit-after" content="2 days">
<meta name="author" content="Bumble Bees IT Solutions">

</svelte:head>
<script>
  import Testimonials from "../components/Testimonials.svelte";

    export let activePage = "Home"; 
  </script>
  
  <div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          About Us - Benchmark Builders
        </h1>
        <span class="sub-text">
          We are a team with 20 years of experience, dedicated to providing exceptional services. Our goal is to create dream homes for our clients.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>About Us</li>
        </ul>
      </div>
    </div>
  </div>
  


  <div id="rs-about" class="rs-about about-style3 about-modify1 pt-120 pb-70 md-pt-80 md-pb-80">
    <div class="container">
        <div class="row y-middle">
            <div class="col-lg-5 md-mb-50">
                <div class="image-part2">
                    <img src="assets/images/Chennai-Promotions.png" alt="Logo-About">
                </div>
            </div>
            <div class="col-lg-7">
                <div class="sec-title">
                    <span class="sub-text sub-text9">About Us</span>
                    <h4 class="title title7 pb-30">
                        Discovering Bench Mark Builders <br> From Ideas to Reality
                    </h4>
                    <p class="desc desc9 desc-small" style="text-align: justify; font-size: 20px; 
                        line-height: 1.6;
                        color: #555; 
                        margin-bottom: 15px;">
                        Bench Mark Builders stands as a leading architectural and construction firm based in Chennai, India. With over 5 years of experience, our journey began with the vision of our Founder & Chief Executive Officer, Mohamed Ishaq Syed, and the guidance of our Managing Director, R. Karaunainathan.
            
                        Over the years, we have excelled in creating innovative and unique designs, ensuring bold execution, and tailoring solutions to meet the diverse requirements of our clients. Our expertise lies in both interior and exterior design, where we blend creativity with functionality to bring your vision to life. We specialize in the techniques and industry involved in the assembly and erection of structures, ensuring top-notch quality in every project.
                    </p>
                </div>
            </div>
            
        </div>
    </div>
</div>




<div class="rs-inner-blog pt-60 pb-105 md-pt-80 md-pb-80">
    <div class="container">
        <div class="row">
            <div class="col-lg-12 md-mb-50">
                <div class="blog-details">
                    <div class="bs-img mb-50">
                        <!-- Replace the image source with an appropriate image for your About Us section -->
                        <img src="assets/images/popin.jpg" alt="Bench Mark Builders">
                    </div>
                    <div class="blog-full">
                        <div class="blog-content-full">
                            <p class="pb-25">
                                Welcome to Bench Mark Builders! We take pride in being a leading architectural and construction firm based in Chennai, India. Our journey is marked by a commitment to excellence, innovation, and client satisfaction.
                            </p>
                            <h3 class="title pb-35">Our Vision</h3>
                            <p class="pb-25">
                                At Bench Mark Builders, we envision a world where architecture meets functionality, and every space tells a unique story. Our goal is to transform your ideas into tangible and visually stunning structures that stand the test of time.
                            </p>
                         
                        </div>
                    </div>
                </div>
            </div>


            <div class="row y-middle">
                <div class="col-lg-6 pr-50 md-pr-15 md-mb-30">
                    <div class="project-content mb-45">
                        <div class="project-title">
                            <h2 class="title pb-35">Project Goals</h2>
                        </div>
                        <div class="desc pb-30">
                            With a team of dedicated professionals, we specialize in both interior and exterior design. Our expertise lies in bringing together creativity, functionality, and quality craftsmanship to deliver projects that exceed expectations.
                        </div>
                        <ul class="check-lists check-lists3 check-single">                              
                            <li>Innovative and unique designs</li>
                            <li>Expertise in both interior and exterior design</li>
                            <li>Quality craftsmanship and execution</li>
                            <li>Client-focused approach</li>      
                        </ul>
                        <div class="desc pt-20">
                            We understand that every project is unique, and we tailor our solutions to meet the diverse requirements of our clients. Bench Mark Builders is not just a construction firm; we are your partners in turning your dreams into reality.

                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="project-goal">
                        <img src="assets/images/BMBUILDERS-1080x1080-BNO-01.png" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<Testimonials/>