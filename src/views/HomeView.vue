<script setup>
import Hero from "@/components/about/Hero.vue";
import PortfolioGrid from "@/components/about/PortfolioGrid.vue";
import ProjectsGrid from "@/components/projects/ProjectsGrid.vue";
import MovingText from "@/components/projects/MovingText.vue";
import ExperienceGrid from "@/components/experience/ExperienceGrid.vue";
import ContactForm from "@/components/contact/ContactForm.vue";
import Footer from "@/components/contact/Footer.vue";
</script>

<template>
  <main>
    <section id="about" class="about">
      <Hero />
      <PortfolioGrid />
    </section>
    <section id="projects" class="projects">
      <ProjectsGrid />
      <MovingText />
    </section>
    <section id="experience" class="experience">
      <ExperienceGrid />
    </section>
    <section id="contact" class="about">
      <ContactForm />
      <Footer/>
    </section>
  </main>
</template>
