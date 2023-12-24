<script>
    export let title = "custom";
    export let subtitle = "subtitle";
  </script>
  
  <section id="hero" class="d-flex justify-content-center align-items-center">
    <div class="container position-relative aos-init aos-animate" data-aos="zoom-in" data-aos-delay="100">
      <h1 class="text-white">{title}</h1>
      <h2>{subtitle}</h2>
      <!-- You can add more content here as needed -->
    </div>
  </section>
  
  <style>
  #hero {
  width: 100%;
  height: 80vh;
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("https://firebasestorage.googleapis.com/v0/b/intricate-aria-345510.appspot.com/o/parallax1.jpg?alt=media&token=f4b8ddcd-af05-47aa-a8dc-7e15da46036a") top center;
  background-attachment: scroll;
  background-size: cover;
  position: relative;
}

#hero h1 {
  margin: 0;
  font-size: 48px;
  font-weight: 700;
  line-height: 56px;
  color: #fff;
  /* font-family: "Poppins", sans-serif; */
}

#hero h2 {
  color: #eee;
  margin: 10px 0 0 0;
  font-size: 24px;
  font-family: var(--bs-font-sans-serif);
}

/* Media Queries for Responsive Design */
@media (max-width: 768px) {
  #hero h1 {
    font-size: 36px;
    line-height: 42px;
  }

  #hero h2 {
    font-size: 18px;
  }
}

@media (max-width: 576px) {
  #hero h1 {
    font-size: 24px;
    line-height: 28px;
  }

  #hero h2 {
    padding-top: 1rem;
    font-size: 16px;
    line-height: 1.5;
  }
}
  </style>
  