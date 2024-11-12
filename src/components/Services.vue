<template>
    <section class="services-section">
      <div class="container">
        <div class="service" v-for="(service, index) in services" :key="index">
          <div class="service-number">{{ index + 1 }}</div>
          <h3 class="service-title">{{ service.title }}</h3>
          <p class="service-description">{{ service.description }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ServicesSection',
    data() {
      return {
        services: [
          { title: 'Project Planning and Scheduling', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
          { title: 'Procurement & Resource Management', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
          { title: 'Project Documentation and Reporting', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
          { title: 'Consulting Team Recruitment & Management', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
          { title: 'Stakeholder Engagement Management', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
          { title: 'Training', description: "I'm a paragraph. Click here to add your own text and edit me. Let your users get to know you." },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Mobile-First Styles */
  .services-section {
    padding: 3rem 1rem;
    background-color: #f9f9f9;
  }
  
  .container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    width:90%;
    margin: 0 auto;

    
  }
  
  .service {
    text-align: center;
    padding: 2rem;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .service-number {
    font-size: 2.5rem;
    font-weight: bold;
    color: #d6336c;
    margin-bottom: 1rem;
  }
  
  .service-title {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 1rem;
  }
  
  .service-description {
    font-size: 1rem;
    color: #666;
  }
  html {
    scroll-behavior: smooth;
  }
  
  /* Tablet Styles */
  @media (min-width: 600px) {
    .container {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  
  /* Desktop Styles */
  @media (min-width: 1024px) {
    .container {
      grid-template-columns: repeat(3, 1fr);
    }
  }
  </style>
  