<template>
    <div>
        <NavBar />
        <section class="about-section">
            <div class="container">
                <div class="content-wrapper">
                    <div class="text-content">
                        <h1 class="main-heading">About US</h1>
                        <h2 class="subheading">Company Profile</h2>
                        <p>
                            For over 15 years, RCM has been at the forefront of project management excellence,
                            transforming visions into reality across The Gambia. We offer comprehensive services across
                            multiple sectors, delivering tailored solutions for each client.
                        </p>
                        <p>
                            Our seasoned consultants bring multi-disciplinary expertise in sectors like Agriculture,
                            Education, Health, Tourism, Trade, and Energy. With over 1,000 expert CVs, we ensure quality
                            expertise on demand.
                        </p>
                    </div>
                    <div class="image-wrapper">
                        <img src="../../public/background.jpg" alt="Laptop on desk" />
                    </div>
                </div>
            </div>
        </section>
        <Footer/>
    </div>
</template>

<script>
import NavBar from './NavBar.vue';
import Footer from "./Footer.vue";

export default {
    components: {
        NavBar,
        Footer
    },
    name: "AboutSection",
};
</script>

<style scoped>
/* Responsive styling */

.content-wrapper {
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.text-content,
.image-wrapper {
    flex: 1 1 100%;
    max-width: 100%;
}

.main-heading {
    font-size: 2rem;
}

.subheading {
    font-size: 1rem;
}

p {
    font-size: 0.9rem;
    text-align: justify;
}

.about-section {
    padding: 4rem 1rem;
    background-color: #f9f9f9;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}

.content-wrapper {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 2rem;
}

.text-content {
    flex: 1 1 50%;
    max-width: 600px;
}

.main-heading {
    font-size: 2.5rem;
    font-weight: bold;
    margin-bottom: 1rem;
    line-height: 1.2;
}

.subheading {
    font-size: 1.2rem;
    font-weight: bold;
    color: #d6336c;
    margin-bottom: 1rem;
}

p {
    line-height: 1.6;
    font-size: 1rem;
    margin-bottom: 1.5rem;
}

img {
    max-width: 100%;
    height: auto;
}

@media(min-width:64rem) {
    .text-content {
        width: 60%;
        margin: 0 auto;
    }
}
</style>