

<script>
    
    import emailjs from 'emailjs-com';
  import Swal from 'sweetalert2';

  let name = '';
  let phone = '';

  let query = '';

  const handleSubmit = async () => {
    try {
      // Send form data to email service
      const templateParams = {
        name,
        phone,
      
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
  title: 'Message Sent Successfully!',
  html: 'Our team will contact you as soon as possible. In the meantime, feel free to <a href="tel:+918925677718">call us</a> for immediate assistance.',
  timer: 3000, 
  showConfirmButton: false, 
  allowOutsideClick: false, 
  allowEscapeKey: false 
});


        closeModal();
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
  };
    
    let features = [
      "Cement - Zuari Cement / Dalmia Cement",
      "Steel TMT Bars - ARS 550D TMT Bars",
      "Quality Brick",
      
      "M Sand - Double Wash",
      "Plastering - P Sand",
      "Asian Paints (Premium)",
      "Teak Wood I Quality",
      "KAG / Anuj Tiles",
      "HIFI Switch",
      "Parryware Sanitaryware"
    ];


    let features2 = [
    "Cement - Coromandel / UltraTech",
    "Steel TMT Bars - iSTEEL XLS TMT Bars",
    "Quality Brick",

    "M Sand - Triple Wash",
    "Plastering - P Sand",
    "Asian Paints (Royal)",
    "Teak Wood I Quality",
    "Johnson / Kajaria Tailes",
    "Greatwhite / Anchor Switch",
    "Jaquar Sanitaryware"
  ];


  let showModal = false;
  
  function openModal() {
    showModal = true;
  }
  
  function closeModal() {
    showModal = false;
  }


  export let activePage = "Home";
  </script>

<div class="rs-breadcrumbs img1">
    <div class="container">
      <div class="breadcrumbs-inner">
        <h1 class="page-title">
          Free Quote - Benchmark Builders
        </h1>
        <span class="sub-text">
          Discover our flexible Quote options tailored to meet your construction and design needs.
        </span>
        <ul class="breadcrumbs-area">
          <li title={`Go to ${activePage}`}>
            <a class:active={activePage === "Home"} href="/">Home</a>
          </li>
          <li>Free Quote</li>
        </ul>
      </div>
    </div>
  </div>
  



<div class="rs-pricing pricing-style1 pt-120 pb-120 md-pt-80 md-pb-80">
    <div class="container">
        <div class="row">
            <div class="col-lg-6 col-md-6 md-mb-50">
                <div class="pricing-table-wrap">
                    <div class="pricing-table-header">
                        <h3 class="pricing-table-title">Basic</h3>
                    </div>
                   
                    <div class="pricing-table-price-tag">
                        
                        <span class="pricing-table-price-text">2499</span>
                        <span class="pricing-table-currency">₹</span>
                        <span class="pricing-table-period">Per Sq.Ft</span>
                    </div>

                    <ul class="pricing-table-features-list">
                     
                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Septic tank 4000ltr
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Sump tank 4000ltr
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Grill gate
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Spot lights
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">2 Years Maintenance
                         </span>
                      </li>
                  
                     
                  </ul>
                  
                  
                  

                    <div class="pricing-table-header">
                      <h3 class="pricing-table-title">Material specifications</h3>
                  </div>
                    <ul class="pricing-table-features-list">
                      
                            {#each features as feature (feature)}
                              <li>
                                <i class="fa fa-check"></i>
                                <span class="feature-text">{feature}</span>
                              </li>
                            {/each}
                     
                        
                    </ul>
                    <div class="btn-part mt-45 md-mt-30 text-center">
                        <button on:click={openModal} class="readon more pricing" ><span>Get Your Quote Now</span></button>

                    </div>
                </div>
            </div>
            <div class="col-lg-6 col-md-6 md-mb-50">
                <div class="pricing-table-wrap">
                    <div class="pricing-table-header">
                        <h3 class="pricing-table-title">Premium</h3>
                    </div>
                   
                    <div class="pricing-table-price-tag">
                        
                        <span class="pricing-table-price-text">2999</span>
                        <span class="pricing-table-currency">₹</span>
                        <span class="pricing-table-period">Per Sq.Ft</span>
                    </div>
                    <ul class="pricing-table-features-list">
                     
                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Septic tank 8000ltr
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Sump tank 8000ltr
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">Grill gate
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">False celieng
                         </span>
                      </li>

                      <li>
                        <i class="fa fa-check"></i>
                        <span class="feature-text">5 Years Maintenance
                         </span>
                      </li>
                  
                     
                  </ul>
                  
                  
                  

                    <div class="pricing-table-header">
                      <h3 class="pricing-table-title">Material specifications</h3>
                  </div>
                    <ul class="pricing-table-features-list">
                        {#each features2 as feature (feature)}
                        <li>
                          <i class="fa fa-check"></i>
                          <span class="feature-text">{feature}</span>
                        </li>
                      {/each}
                       
                    </ul>
                    <div class="btn-part mt-45 md-mt-30 text-center">
                        <button on:click={openModal} class="readon more pricing" ><span>Get Your Quote Now</span></button>

                    </div>
                </div>
            </div>
        
        </div>
    </div>
</div>


{#if showModal}
  <div class="modal-overlay">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <button on:click={closeModal} class="modal-close-btn">Close</button>
        
        <!-- Your form content goes here -->
        <form on:submit|preventDefault={handleSubmit}>
            <label for="name">Name:</label>
            <input bind:value={name} type="text" id="name" name="name" required>
          
            <label for="phone">Phone Number:</label>
            <input bind:value={phone} type="tel" id="phone" name="phone" required>
          
          
          
            <label for="query">Query:</label>
            <textarea bind:value={query} id="query" name="query" required></textarea>
          
            <button type="submit">Submit</button>
          </form>
      </div>
    </div>
  </div>
{/if}


<style>
 /* Add this to your CSS file for styling */
 .modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000; /* Adjust the z-index to make sure it overlays other content */
}

.modal-dialog {
  width: 400px;
  z-index: 1100; /* Make sure the modal is above the overlay */
}

.modal-content {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

.modal-close-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  background: none;
  border: none;
  cursor: pointer;
  font-size: 16px;
  color: #333;
  z-index: 1200; /* Ensure the close button is above other content */
}

form {
  margin-top: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  box-sizing: border-box;
}

button {
  background-color: #007bff;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

</style>