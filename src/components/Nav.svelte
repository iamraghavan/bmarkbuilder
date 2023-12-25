<script>
	let options = [
	  { text: 'Architecture', href: '/services/architecture' },
	  { text: 'Exterior Design', href: '/services/exterior-design' },
	  { text: 'Renovation', href: '/services/renovation' },
	  { text: 'Landscape Design', href: '/services/landscape-design' },
	  { text: 'Individual House', href: '/services/individual-house' },
	  { text: 'Commercial Buildings', href: '/services/commercial-buildings' },
	  { text: 'Apartment', href: '/services/apartment' },
	  { text: 'Villa', href: '/services/villa' }
	];

	let bmoptions = [
		{ text: 'About us', href: '/about'},
		{ text: 'Media Galley', href: '/media-gallery' },
		{ text: 'Joint Venture', href: '/joint-venture'},
	]
  </script>


<style>

/* Base styles for the rectangle share image logo */
.rectangle-share-logo {
  width: 100%; /* Set the width to 100% for responsiveness */
  max-width: 19rem; /* Limit the maximum width to 19rem */
  height: auto; /* Allow the height to adjust proportionally */
  padding: 1.2rem 0; /* Adjust padding values */
  /* Add any additional styling for the image logo, such as border-radius, box-shadow, etc. */
}

/* Media query for smaller screens */
@media only screen and (max-width: 768px) {
  .rectangle-share-logo {
    max-width: 15rem; /* Adjust the maximum width for smaller screens */
  }
}

/* Media query for even smaller screens */
@media only screen and (max-width: 480px) {
  .rectangle-share-logo {

    max-width: 12rem; /* Adjust the maximum width for even smaller screens */
  }
}




</style>

<div class="full-width-header">
	<!--Header Start-->
	<header id="rs-header" class="rs-header">
		<!-- Toolbar Area Start -->
		<div class="toolbar-area topbar-style1 hidden-md">
			<div class="container">
				<div class="row rs-vertical-middle">
				   <div class="col-lg-7">
						<div class="toolbar-contact">
							<ul class="rs-contact-info">                   
							<li>
									<i class="fi fi-rr-envelope-plus"></i>                  
									<a href="mailto:benchmarkbuilder21@gmail.com">benchmarkbuilder21@gmail.com</a>               
								</li>
								<li>
									  <i class="fi fi-rr-phone-call"></i>                                      
									<a href="tel:+91 89256 77718"> +91 89256 77718</a>                   
								</li>
							</ul>
						</div>
					</div>
					<div class="col-lg-5">
						<div class="toolbar-sl-share">
							<ul class="clearfix">
								<li class="opening"> <em><i class="fi-rr-map-marker-home"></i> No. 220, G.S.T Road, J.C. Nagar, Urapakkam, Chennai
								</em> </li>
					
								<li><a href="/"><i class="fa fa-whatsapp"></i></a></li>
								<li><a href="/"><i class="fa fa-instagram"></i></a></li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div>
		<!-- Toolbar Area End -->

		<!-- 





 -->
		
		<!-- Menu Start -->
		<div class="menu-area menu-sticky">
			<div class="container">
				<div class="row-table">
					<div class="col-cell header-logo">                                  
						<div class="logo-area">
							<a href="/">
								<img class="normal-logo rectangle-share-logo" src="assets/images/LGLogo2.png" alt="logo">  
								<img class="sticky-logo rectangle-share-logo" src="assets/images/LGLogo2.png" alt="logo">
							</a>
						</div>
					</div>
					<div class="col-cell">
						<div class="rs-menu-area">
							<div class="main-menu">
								<nav class="rs-menu hidden-md">
									<ul class="nav-menu">
										<li class=" current-menu-item">
											<a href="/">Home</a>
											
										</li>
										<li class="menu-item-has-children">
											<a href="about.html">BM Builders</a>
											<ul class="sub-menu">
												{#each bmoptions as { text, href }}
												<li><a href={href}>{text}</a></li>
											  {/each}
											</ul>
										</li>
										<li class="menu-item-has-children">
											<a href="services.html">Our Services</a>
											<ul class="sub-menu">
												{#each options as { text, href }}
												<li><a href={href}>{text}</a></li>
											  {/each}
											</ul>
										</li>
										<li class="">
											<a href="/projects/">Projects</a>
											
										</li>
										<li class="">
											<a href="/">Careers</a>
											
										</li>
									
										<li>
											<a href="contact.html">Contact us</a>
										</li>
									</ul> <!-- //.nav-menu -->
								</nav>
							</div> <!-- //.main-menu -->
						</div>
					</div>
					<div class="col-cell">
						<div class="expand-btn-inner">
							<ul>
								
								<!-- <li class="btn-quote"><a class="quote-button" href="/">Let's Talk</a></li> -->
								<li class="humburger">
									<a style="padding-top: 20px; padding-right: 10px;" id="nav-expander" class="nav-expander bar" href="/">
										<svg style="color: black;" xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
											<path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"/>
										  </svg>
									</a>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div>
		<!-- Menu End -->

		<!-- Canvas Mobile Menu start -->
		<nav class="right_menu_togle mobile-navbar-menu" id="mobile-navbar-menu">
			<div class="close-btn">
				<a id="nav-close2" class="nav-close">
					<div class="line">
						<span class="line1"></span>
						<span class="line2"></span>
					</div>
				</a>
			</div>
			<ul class="nav-menu">
				<li class=" current-menu-item">
					<a href="/">Home</a>
					
				</li>
				<li>
					<a href="/about">About us</a>
				</li>
				<li class="menu-item-has-children">
					<a href="/">Our Services</a>
					<ul class="sub-menu">
						{#each options as { text, href }}
												<li><a href={href}>{text}</a></li>
											  {/each}
					</ul>
				</li>
				<li class="">
					<a href="/">Careers</a>
					
				</li>
			
				<li>
					<a href="contact.html">Contact us</a>
				</li>
			</ul> 
			<!-- //.nav-menu -->
		   
			<!-- //.nav-menu -->
			<div class="canvas-contact">
				  <div class="address-area">
					  <div class="address-list">
						  <div class="info-icon">
							  <i class="fi fi-rr-map-marker-home"></i>
						  </div>
						  <div class="info-content">
							  <h4 class="title">Contact</h4>
							  <em>No. 220, G.S.T Road, J.C. Nagar, Urapakkam, Chennai</em>
						  </div>
					  </div>
					  <div class="address-list">
						  <div class="info-icon">
							  <i class="fi fi-rr-envelope-plus"></i>
						  </div>
						  <div class="info-content">
							  <h4 class="title">Email</h4>
							  <em><a href="mailto:info@konstruk.com"> benchmarkbuilder21@gmail.com</a></em>
						  </div>
					  </div>
					  <div class="address-list">
						  <div class="info-icon">
							  <i class="fi fi-rr-phone-call"></i>
						  </div>
						  <div class="info-content">
							  <h4 class="title">Free Call</h4>
							  <em>+91 89256 77718</em>
						  </div>
					  </div>
				  </div>
			</div>
		</nav>
		<!-- Canvas Menu end -->                             
	</header>
	<!--Header End-->
</div>