<template>
    <nav class="navbar">
      <div class="navbar-container">
        <!-- Logo -->
        <a href="/" class="navbar-logo"><img class="logo" src="../../public/logo.jpeg" alt="" srcset=""></a>
  
        <!-- Toggle Button for Mobile -->
        <button @click="toggleMenu" class="navbar-toggle" aria-label="Toggle navigation">
          <span v-if="!isMenuOpen">☰</span>
          <span v-else>✖</span>
        </button>
  
        <!-- Links -->
        <ul :class="['navbar-links', { 'navbar-links--open': isMenuOpen }]">
          <li v-for="link in navLinks" :key="link.text">
            <!-- Use router-link if 'to' exists, otherwise use anchor tag -->
            <router-link v-if="link.to" :to="link.to" @click="handleLinkClick">{{ link.text }}</router-link>
            <a v-else @click.prevent="scrollToSection(link.href.slice(1))">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  import { ref } from 'vue';
  import gsap from 'gsap';
  import { ScrollToPlugin } from 'gsap/ScrollToPlugin';
  
  gsap.registerPlugin(ScrollToPlugin);
  
  export default {
    name: 'NavBar',
    setup() {
      // State for menu toggle
      const isMenuOpen = ref(false);
  
      // Function to toggle menu
      const toggleMenu = () => {
        isMenuOpen.value = !isMenuOpen.value;
      };
  
      // Function for smooth scrolling to internal sections
      const scrollToSection = (id) => {
        gsap.to(window, {
          duration: 1.5,
          scrollTo: { y: `#${id}`, offsetY: 70 }, // Scroll to section ID with offset for header
          ease: 'power2.out',
        });
        // Close mobile menu after clicking a link
        isMenuOpen.value = false;
      };
  
      // Navigation links
      const navLinks = [
        { text: 'Home', to: '/' },
        { text: 'About Us', to: '/about' },
        { text: 'Services', href: '#services' },
        { text: 'Team', href: '#team' },
        { text: 'Contact Us', href: '#contact' },
      ];
  
      // Close the menu after clicking a link
      const handleLinkClick = () => {
        isMenuOpen.value = false;
      };
  
      return { isMenuOpen, toggleMenu, scrollToSection, navLinks, handleLinkClick };
    },
  };
  </script>
  
  <style scoped>
  /* Basic styling */
  .navbar {
    background-color: #004080;
    color: white;
    padding: 1rem;
    position: relative;
  }
  .logo{
    width: 50px;
    
  }
  .navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .navbar-logo {
    font-size: 1.5rem;
    color: white;
    text-decoration: none;
  }
  
  .navbar-toggle {
    display: none;
    font-size: 1.5rem;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
  }
  
  a {
    cursor: pointer;
  }
  
  .navbar-links {
    list-style: none;
    display: flex;
    gap: 1rem;
    margin: 0;
    padding: 0;
    z-index: 1;
  }
  
  .navbar-links a,
  .navbar-links router-link {
    color: white;
    text-decoration: none;
  }
  
  /* Responsive styles */
  @media (max-width: 768px) {
    .navbar-toggle {
      display: block;
    }
  
    .navbar-links {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 100%;
      left: 0;
      width: 100%;
      background-color: #004080;
      padding: 1rem 0;
      align-items: center;
    }
  
    .navbar-links--open {
      display: flex;
    }
  }
  </style>
  