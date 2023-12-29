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
</script>

<div class="col-lg-4 pl-36 md-pl-15">
    <ul class="services-list mb-50">
        {#each options as { text, href }}
		<li><a href={href}>{text}</a></li>
		{/each}
     </ul>

     <div class="services-add mb-50">
        <div class="services-overlay"></div>
        <div class="address-wrap-item mb-20">
            <div class="icon-part mb-37">
                <i class="fa fa-phone"></i>
            </div>
            <h2 class="title">Have any Questions? Call us <span>Today!</span></h2>
            <div class="divider">
                <span class="divider-separator"></span>
            </div>
            <div class="contact">
                <a style="font-size: 1.98rem !important;" href="tel:+918925677718">+(91) 89256 77718</a>
            </div>
        </div>
    </div>
    <div class="brochures">
        <div class="content-text">
            <h3 class="title">Brochures</h3>
            <p class="desc-part">
                Explore our comprehensive brochures for detailed insights into our services and offerings.
            </p>
        </div>
        <div class="btn-wrapper">
            <a class="dual-btn" href="/">Download</a>
      
        </div>
    </div>
     
  <!-- Your additional content here -->
</div>