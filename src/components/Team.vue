<template>
    <section class="team-section">
        <h2>Our Team</h2>
      <div class="container">
        <div class="team-member" v-for="(member, index) in teamMembers" :key="index">
          <img :src="member.photo" :alt="member.name" class="member-photo" />
          <h3 class="member-name">{{ member.name }}</h3>
          <p class="member-role">{{ member.role }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'TeamSection',
    data() {
      return {
        teamMembers: [
          {
            name: 'Eli Glickman',
            role: 'Senior Consultant & Partner',
            photo: require('../../public/team.png'), // Replace with actual image paths
          },
          {
            name: 'Norah Emerson',
            role: 'Senior Consultant & Partner',
            photo: require('../../public/team.png'),
          },
          {
            name: 'Adam Cho',
            role: 'Senior Consultant & Partner',
            photo: require('../../public/team.png'),
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Mobile-First Styles */
  .team-section {
    padding: 3rem 1rem;
    background-color: #f9f9f9;
  }
  
  .container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .team-member {
    text-align: center;
  }
  
  .member-photo {
    width: 100%;
    max-width: 300px;
    height: auto;
    border-radius: 8px;
    margin-bottom: 1rem;
  }
  
  .member-name {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  .member-role {
    font-size: 1rem;
    color: #666;
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
  