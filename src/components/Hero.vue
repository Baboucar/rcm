<template>
    <section class="hero-section">
      <div class="overlay">
        <div class="content">
          <h1 class="main-heading">Transforming Visions Into Reality</h1>
          <p class="subheading">The Gambia's Leading Project Management Experts</p>
          <button class="cta-button">Get Started</button>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Home',
  };
  </script>
  
  <style scoped>
  /* Hero Section styling */
  .hero-section {
    position: relative;
    height: 500px;
    background-image: url('../../public/background.jpg'); 
    background-size:cover;
    background-position: center;
    align-items: center;
    justify-content: center;
    
  }
  
  .overlay {
    position: absolute;
    width: 92%;
    top: 0;
    left: 0;
    height: 500px;
    background-color: rgba(0, 20, 50, 0.7); /* Adds a dark overlay */
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    text-align: center;
    padding: 0 1rem;
  }
  
  .content {
    max-width: 600px;
    padding: 1rem;
  }
  
  .main-heading {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  
  
  .cta-button {
    background-color: #d6336c;
    color: white;
    padding: 0.8rem 1.5rem;
    border: none;
    border-radius: 5px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .cta-button:hover {
    background-color: #c0275e;
  }
  img{
    max-width: 100%;
    height: auto;
  }
  /* Responsive styling */
@media(min-width: 64rem){
    .overlay{
        width: 100%;
    }  
    .subheading {
        font-size: 1.2rem;
        margin-bottom: 1.5rem;
      }
      .main-heading {
        font-size: 3rem;
        font-weight: bold;
        margin-bottom: 0.5rem;
      }
}
 
  </style>
  