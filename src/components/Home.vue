<template>
    <div>
      <!-- Pass scrollToSection as a prop to NavBar -->
      <NavBar :scrollToSection="scrollToSection" />
      <Hero id="hero" />
      
      <!-- Section IDs for smooth scrolling -->
      <section id="services">
        <Services />
      </section>
      <section id="team">
        <Team />
      </section>
      <section id="contact">
        <Contact />
      </section>
      <Footer/>
    </div>
  </template>

<script>
import gsap from 'gsap';
import { ScrollToPlugin } from 'gsap/ScrollToPlugin';
import NavBar from "./NavBar.vue";
import Hero from "./Hero.vue";
import Services from "./Services.vue";
import Team from './Team.vue';
import Contact from './Contact.vue';
import Footer from "./Footer.vue";
gsap.registerPlugin(ScrollToPlugin);

export default {
    components:{
        NavBar,
        Hero,
        Services,
        Team,
        Contact,
        Footer

    },
    setup () {
        

        return {}
    },
    methods: {
    scrollToSection(id) {
      gsap.to(window, {
        duration: 1.5, // Duration of the animation in seconds
        scrollTo: { y: `#${id}`, offsetY: 70 }, // Scroll to the section by ID with an offset for header
        ease: 'power2.out', // Easing function
      });
    },
  },

}
</script>

<style lang="scss" scoped>

</style>