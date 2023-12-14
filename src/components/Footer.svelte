<script>
    const services = [
      { text: 'Architecture', href: '/architecture' },
	  { text: 'Exterior Design', href: '/exterior-design' },
	  { text: 'Renovation', href: '/renovation' },
	  { text: 'Landscape Design', href: '/landscape-design' },
	  { text: 'Individual House', href: '/individual-house' },
	  { text: 'Commercial Buildings', href: '/commercial-buildings' },
	  { text: 'Apartment', href: '/apartment' },
	  { text: 'Villa', href: '/villa' }
  ];


  const imptlink = [
    { text: 'Privacy Policy', href: '/architecture' },
	  { text: 'Terms & Condition', href: '/exterior-design' },
	  { text: 'Career', href: '/renovation' },
	  { text: 'News & Blog', href: '/landscape-design' },
	  { text: 'Budget Calculator', href: '/individual-house' },
  ]

  
  const currentDate = new Date();

// Get the current year
const currentYear = currentDate.getFullYear();

  
  let contactDetails = [
      {
        title: 'Chennai office',
        address: 'No. 220, G.S.T Road, J.C. Nagar, Urapakkam, Chennai',
        icon: 'assets/images/contact/style1/icons/1.png',
      },
      {
        title: 'Email us',
        emails: ['benchmarkbuilders21@gmail.com', 'enquiry@benchmarkbuilders21.com'],
        icon: 'assets/images/contact/style1/icons/2.png',
      },
      {
        title: 'Call us',
        phoneNumbers: ['+91 89256 77718', '+91 89256 77718'],
        icon: 'assets/images/contact/style1/icons/3.png',
      },
    ];
  

  

  </script>
  

<footer id="rs-footer" class="rs-footer footer-main-home">
    <div class="footer-top">
        <div class="container">
            <div class="row">
                <div class="col-lg-3 pr-20 md-pr-15 md-mb-20">
                    <div class="footer-logo mb-51 md-mb-30">
                        <a href="index.html"><img style="
                          width: auto;
                          height: 10rem;
                      " src="assets/images/logo-bm.png" alt="bench mark builders"></a>
                    </div>
                    <div class="textwidget">
                        <p class="pb-20">Benchmark Builders is committed to providing top-notch construction solutions.</p>
                        <p class="pb-25"><strong>Opening Hours</strong> : Monday – Sat: 9am to 6pm</p>
                    </div>
                    <ul class="footer-social md-mb-30">  
                        <li><a href="/"><i class="fa fa-facebook"></i></a></li>                     
                        <li><a href="/"><i class="fa fa-whatsapp"></i></a></li>                     
                        <li><a href="/"><i class="fa fa-youtube"></i></a></li>                     
                        <li><a href="/"><i class="fa fa-instagram"></i></a></li>                     
                      </ul>
                </div>
                <div class="col-lg-4 md-mb-10">
                    <h3 class="footer-title">Contact Info</h3>
                    <ul class="address-widget">
                      {#each contactDetails as { title, address, emails, phoneNumbers, icon }}
                        <li>
                          <i class="fi fi-rr-map-marker-home"></i>
                          <div class="desc">
                            {#if address}
                              {address}
                            {/if}
                            {#if emails}
                              {#each emails as email}
                                <a href="mailto:{email}">{email}</a><br>
                              {/each}
                            {/if}
                            {#if phoneNumbers}
                              {#each phoneNumbers as phoneNumber}
                                <a href="tel:{phoneNumber}">{phoneNumber}</a><br>
                              {/each}
                            {/if}
                          </div>
                        </li>
                      {/each}
                    </ul>
                  </div>
                <div class="col-lg-3 md-mb-10">
                    <h3 class="footer-title">Our Services</h3>
                    <ul class="site-map">
                        {#each services as { text, herf }}
    <li><a href={herf}>{text}</a></li>
  {/each}
                    </ul>
                </div>
                <div class="col-lg-2">
                  <h3 class="footer-title">Important Links</h3>
                  <ul class="site-map">
                      {#each imptlink as { text, herf }}
  <li><a href={herf}>{text}</a></li>
{/each}
                  </ul>
                </div>
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">                    
            <div class="row y-middle">
                <div class="col-lg-6 md-mb-10 text-lg-end text-center order-last">
                  <div class="copyright">
                   <p class="text-white">Developed & Supported By <span style="color:#eda73e ">Bumble Bees</span> It Solutions</p>
                  </div>
                  </div>
                <div class="col-lg-6">
                    <div class="copyright text-lg-start text-center">
                        <p>© 2020 - {currentYear} BenchMark Builders - All Rights Received </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</footer>