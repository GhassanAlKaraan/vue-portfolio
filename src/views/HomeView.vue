<script setup>
import Hero from "@/components/Hero.vue";
import PortfolioGrid from "@/components/PortfolioGrid.vue";
import Projects from "@/components/Projects.vue";
</script>

<template>
  <main>
    <section id="about" class="about">
      <Hero />
      <PortfolioGrid />
    </section>
    <section id="projects" class="projects">
      <Projects />
    </section>
    <section id="experience" class="experience">
      <h2>Work Experience</h2>
      <div>
        <h3>Company XYZ</h3>
        <p>Position: Senior Software Developer</p>
        <p>Duration: 2018 - Present</p>
        <p>Description: Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.</p>
      </div>
      <div>
        <h3>Company ABC</h3>
        <p>Position: Junior Software Developer</p>
        <p>Duration: 2015 - 2018</p>
        <p>Description: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
          labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.</p>
      </div>
      <p>Porttitor rhoncus dolor purus non enim praesent elementum facilisis. Nisi scelerisque eu ultrices vitae auctor
        eu augue ut lectus. Ipsum faucibus vitae aliquet nec ullamcorper sit amet risus nullam. Dictum varius duis at
        consectetur lorem. Nisi vitae suscipit tellus mauris a diam maecenas sed enim ut. Cursus sit amet dictum sit
        amet. Egestas purus viverra accumsan in nisl nisi scelerisque eu ultrices. Sit amet porttitor eget dolor morbi
        non.</p>
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
