<template>
    <div>
    <section class="contact-section">
        <h2>Contact Us</h2>
      <div class="container">
        <div class="contact-form">
          <h2 class="contact-title">Contact Us</h2>
          <p class="contact-subtitle">Reach out with any questions or inquiries</p>
          <form @submit.prevent="submitForm">
            <div class="form-row">
              <input type="text" placeholder="First name *" required />
              <input type="text" placeholder="Last name *" required />
            </div>
            <div class="form-row">
              <input type="email" placeholder="Email *" required />
              <input type="tel" placeholder="Phone" />
            </div>
            <textarea placeholder="Leave us a message..." rows="4"></textarea>
            <button type="submit" class="submit-button">Submit</button>
          </form>
        </div>
        <div class="contact-info">
          <div class="info-block">
            <h3>Address</h3>
            <p>RCM (GAMBIA), Hendon Complex, Senegambia, <br> Bertil Harding Highway, The Gambia</p>
          </div>
          <div class="info-block">
            <h3>Phone</h3>
            <p>+220 2722211</p>
          </div>
          <div class="info-block">
            <h3>WhatsApp </h3>
            <p>+220 2722211</p>
          </div>
          <div class="info-block">
            <h3>Email</h3>
            <p>info@rcmgambia.com</p>
          </div>
          <div class="social-links">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </section>
    <section>
        <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3880.299744257863!2d-16.710338024671938!3d13.45561130408164!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xec29a1a1b4e557b%3A0x58cac58614a5cd1!2sBertil%20Harding%20Hwy%2C%20Serrekunda!5e0!3m2!1sen!2sgm!4v1731450385205!5m2!1sen!2sgm" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </section>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ContactUs',
    methods: {
      submitForm() {
        // Handle form submission here
        alert('Form submitted!');
      },
    },
  };
  </script>
  
  <style scoped>
  /* Mobile-First Styles */
  .contact-section {
    padding: 2rem 1rem;
    background-color: #f9f9f9;
  }
  .map{
    width: 100%;
  }
  .container {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .contact-form {
    background-color: #fff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .contact-title {
    font-size: 1.8rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  .contact-subtitle {
    font-size: 1rem;
    margin-bottom: 1.5rem;
  }
  
  form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  
  .form-row {
    display: flex;
    gap: 1rem;
  }
  
  input, textarea {
    flex: 1;
    padding: 0.75rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1rem;
  }
  
  .submit-button {
    background-color: #d6336c;
    color: white;
    padding: 0.75rem;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .submit-button:hover {
    background-color: #ec0e5c;
  }
  
  .contact-info {
    text-align: left;
  }
  
  .info-block {
    margin-bottom: 1rem;
  }
  
  .info-block h3 {
    font-size: 1.1rem;
    font-weight: bold;
    margin-bottom: 0.25rem;
  }
  
  .social-links {
    display: flex;
    gap: 1rem;
    font-size: 1.5rem;
  }
  
  .social-links a {
    color: #000;
    transition: color 0.3s;
  }
  
  .social-links a:hover {
    color: #a5673f;
  }
  
  /* Tablet Styles */
  @media (min-width: 768px) {
    .container {
      flex-direction: row;
      gap: 4rem;
    }
  
    .contact-form {
      flex: 2;
    }
  
    .contact-info {
      flex: 1;
    }
  }
  
  /* Desktop Styles */
  @media (min-width: 1024px) {
    .form-row {
      gap: 2rem;
    }
  
    input, textarea {
      padding: 1rem;
      font-size: 1.1rem;
    }
  
    .submit-button {
      padding: 1rem;
      font-size: 1.1rem;
    }
  
    .contact-title {
      font-size: 2rem;
    }
  
    .contact-subtitle {
      font-size: 1.2rem;
    }
  }
  </style>
  