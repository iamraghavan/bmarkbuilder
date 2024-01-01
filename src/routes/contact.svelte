<script>
  import emailjs from 'emailjs-com';
  import Swal from 'sweetalert2';

  let name = '';
  let email = '';
  let phone = '';
  let message = '';

  async function handleSubmit() {
    try {
      // Send form data to email service
      const templateParams = {
        name,
        phone,
        email,
        message,
      };

      const response = await emailjs.send(
        'service_4qmuoao', // Replace with your EmailJS service ID
        'template_y1ru6qm', // Replace with your EmailJS template ID
        templateParams,
        'LHEzahpPnpyu_0R-s' // Replace with your EmailJS user ID
      );

      // Check if the email was sent successfully
      if (response.status === 200) {
        // Show success message
        Swal.fire({
          icon: 'success',
          title: 'Message Sent Successfully!',
          html: 'Our team will contact you as soon as possible. In the meantime, feel free to <a href="tel:+918925677718">call us</a> for immediate assistance.',
          timer: 3000,
          showConfirmButton: false,
          allowOutsideClick: false,
          allowEscapeKey: false,
        });

        // Reset form values
        name = '';
        email = '';
        phone = '';
        message = '';
      } else {
        // Show error message
        Swal.fire({
          icon: 'error',
          title: 'Error!',
          text: 'Oops, something went wrong. Please try again later.',
        });
      }
    } catch (error) {
      console.error('Error sending email:', error);
      // Show error message
      Swal.fire({
        icon: 'error',
        title: 'Error!',
        text: 'Oops, something went wrong. Please try again later.',
      });
    }
  }

  export let activePage = "Home";
</script>



<div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Contact Us - Benchmark Builders
        </h1>
        <span class="sub-text">
          Reach Out to Us for Your Dream Projects.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Contact Us</li>
        </ul>
      </div>
    </div>
  </div>


  <div class="rs-contact contact-style6 pb-120 md-pb-80">
    <div class="row no-gutters">
      <div class="col-lg-6">
        <div class="contact-map">
            <iframe title="Google Maps Location" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15558.88808494719!2d80.0688641!3d12.8612224!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a52f7850831a8d1%3A0xbe0ee0210d0cfb5d!2sBench%20Mark%20Builders!5e0!3m2!1sen!2sin!4v1703868434025!5m2!1sen!2sin"></iframe>

        
        </div>
      </div>
      <div class="col-lg-6">
        <div class="contact-section">
          <div class="contact-wrap">
            <div class="sec-title mb-60">
              <h2 class="title title4 ser-style4">Get in touch</h2>
            </div>
            <div id="form-messages"></div>
            <form id="contact-form" method="post"  on:submit|preventDefault={handleSubmit} action="">
              <fieldset>
                <div class="row">
                  <div class="col-lg-6 col-md-6 col-sm-6 mb-30">
                    <input bind:value={name} class="from-control" type="text" id="name" name="name" placeholder="Name" required="">
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 mb-30">
                    <input bind:value={email} class="from-control" type="text" id="email" name="email" placeholder="E-Mail" required="">
                  </div>
                  <div class="col-lg-12 col-md-12 col-sm-12 mb-30">
                    <input bind:value={phone} class="from-control" type="text" id="phone" name="phone" placeholder="Phone Number" required="">
                  </div>
                  
                  <div class="col-lg-12 mb-30">
                    <textarea bind:value={message} class="from-control" id="message" name="message" placeholder="Your Message Here" required=""></textarea>
                  </div>
                </div>
                <div class="btn-part">
                  <div class="form-group mb-0">
                    <input class="readon more submit sub-con" type="submit" value="Submit Now">
                  </div>
                </div>
              </fieldset>
            </form>
          </div>
        </div>
      </div>
    </div>
    <!-- Contact Icons Section End -->
    <div class="rs-contact pt-120 md-pt-80">
      <div class="container">
        <div class="row">
          <div class="col-lg-4 col-md-6 md-mb-30">
            <div class="contact-box">
              <div class="contact-icon">
                <img src="assets/images/contact/style1/icons/1.png" alt="images">
              </div>
              <div class="content-text">
                <h4 class="title"><a href="/">Office address</a></h4>
                <p class="services-txt"> Plot No 19, G1 Thamarai Flats, 3rd St, J.C. Nagar, <br> Urapakkam, Chennai, Tamil Nadu 603210 </p>
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 sm-mb-30">
            <div class="contact-box">
              <div class="contact-icon">
                <img src="assets/images/contact/style1/icons/2.png" alt="images">
              </div>
              <div class="content-text">
                <h4 class="title"><a href="/">Email us</a></h4>
                <span><a href="mailto:benchmarkbuilders21@gmail.com">benchmarkbuilders21@gmail.com</a></span>
                
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-md-6">
            <div class="contact-box">
              <div class="contact-icon">
                <img src="assets/images/contact/style1/icons/3.png" alt="images">
              </div>
              <div class="content-text">
                <h4 class="title"><a href="/">Call us</a></h4>
                <span><a href="tel:+918925677718">(+91) 89256 77718</a></span><br>
                <span><a href="tel:+9189256777189">(+91) 89256 77719</a></span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Contact Icons Section End -->
  </div>
  