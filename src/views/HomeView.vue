<script setup>
import Hero from "@/components/about/Hero.vue";
import PortfolioGrid from "@/components/about/PortfolioGrid.vue";
import ProjectsGrid from "@/components/projects/ProjectsGrid.vue";
import MovingText from "@/components/projects/MovingText.vue";
import ExperienceGrid from "@/components/experience/ExperienceGrid.vue";
</script>

<template>
  <main>
    <section id="about" class="about">
      <Hero />
      <PortfolioGrid />
    </section>
    <section id="projects" class="projects">
      <ProjectsGrid />
      <MovingText/>
    </section>
    <section id="experience" class="experience">
      <ExperienceGrid />
    </section>
    <section id="contact" class="about">
      <h2>My Contact</h2>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
        Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
        aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.</p>
      <p>Email: lorem.ipsum@example.com</p>
      <p>Phone: (123) 456-7890</p>
      <p>LinkedIn: linkedin.com/in/loremipsum</p>
      <p>GitHub: github.com/loremipsum</p>
      <p>Felis donec et odio pellentesque diam volutpat commodo sed. Tortor consequat id porta nibh venenatis cras sed.
        Ipsum nunc aliquet bibendum enim facilisis gravida neque. Nibh tellus molestie nunc non blandit massa enim nec.
        Sagittis nisl rhoncus mattis rhoncus urna neque viverra. Purus in massa tempor nec feugiat nisl pretium fusce.
      </p>
    </section>
    <section id="dummy data">
      <h2>More contacts</h2>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
        Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
        aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.</p>
      <p>Email: lorem.ipsum@example.com</p>
      <p>Phone: (123) 456-7890</p>
      <p>LinkedIn: linkedin.com/in/loremipsum</p>
      <p>GitHub: github.com/loremipsum</p>
      <p>Felis donec et odio pellentesque diam volutpat commodo sed. Tortor consequat id porta nibh venenatis cras sed.
        Ipsum nunc aliquet bibendum enim facilisis gravida neque. Nibh tellus molestie nunc non blandit massa enim nec.
        Sagittis nisl rhoncus mattis rhoncus urna neque viverra. Purus in massa tempor nec feugiat nisl pretium fusce.
      </p>
    </section>
  </main>
</template>

<style scoped>
</style>
