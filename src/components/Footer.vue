<template>
    <footer class="footer">
      <p>© {{ currentYear }} RCM. All rights reserved.</p>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    data() {
      return {
        currentYear: new Date().getFullYear(),
      };
    },
  };
  </script>
  
  <style scoped>
  .footer {
    padding: 1rem;
    text-align: center;
    background-color: #004080;
    color: #FFF;
    font-size: 0.9rem;
  }
  </style>
  