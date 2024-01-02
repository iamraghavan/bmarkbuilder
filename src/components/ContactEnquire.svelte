<script>
    import emailjs from 'emailjs-com';
    import Swal from 'sweetalert2';
  
    let name = '';
    let phoneNumber = '';
    let email = '';
    let address = '';
    let query = '';
  
    async function handleSubmit() {
      try {
        // Send form data to email service
        const templateParams = {
          name,
          phoneNumber,
          email,
          address,
          query,
        };
  
        const response = await emailjs.send(
            'service_4qmuoao', // replace with your EmailJS service ID
        'template_y1ru6qm', // replace with your EmailJS template ID
        templateParams,
        'LHEzahpPnpyu_0R-s' // replace with your EmailJS user ID
        );
  
        // Check if the email was sent successfully
        if (response.status === 200) {
          // Show success message
          Swal.fire({
            icon: 'success',
            title: 'Form Submitted Successfully!',
            text: 'We will get in touch with you soon.',
          });
  
          // Reset form values
          name = '';
          phoneNumber = '';
          email = '';
          address = '';
          query = '';
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
  </script>

<div class="rs-contact contact-style2">
    <div class="container">
        <div class="requset-contact">
            <div class="sec-title mb-40 md-mb-30">
                <h2 class="title title2">
                    Request A Services
                </h2>
            </div>
            <div class="row">
           
                <div class="col-lg-4 col-sm-6 mb-30">
                    <span class="wpcf7-form-control-wrap">
                        <input type="text" id="name" name="name" placeholder=" Name" required="">
                    </span>
                </div>
                <div class="col-lg-4 col-sm-6 mb-30">
                    <span class="wpcf7-form-control-wrap arrow2">
                        <input type="text" id="phone-number" name="phone-number" placeholder="Phone Number" required="">
                    </span>
                </div>
                <div class="col-lg-4 col-sm-6 mb-30">
                    <span class="wpcf7-form-control-wrap">
                        <input type="text" id="email" name="email" placeholder="Email" required="">
                    </span>
                </div>
               
                <div class="col-lg-4 col-sm-6 md-mb-30">
                    <span class="wpcf73-form-control-wrap">
                        <input type="text" id="query" name="Services" placeholder="Query" required="">
                    </span>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="services-btn">
                        <p class="submit-btn">
                            <input on:submit|preventDefault={handleSubmit} type="submit" value="Submit Services Request" class="Submit Services Request">
                        </p>
                    </div>
                </div>
                
            </div>
        </div>
    </div>
</div>