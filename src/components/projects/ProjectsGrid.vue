<script setup>
import GithubLink from "@/components/projects/GithubLink.vue";
</script>

<template>
    <div class="wrapper">
        <div class="projects-heading">
            <h2>A small selection of <span>recent projects</span></h2>
        </div>
        <div class="container">
            <div class="projects-grid">

                <!-- Project Card 1 -->
                <div class="card">
                    <div class="project-image">
                        <img src="@/assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="@/assets/images/projects/portfolio-project.png" class="img-2" />
                    </div>
                    <h4 class="project-title">My Personal Portfolio</h4>
                    <p>Developed this web portfolio to highlight my skills and experience.</p>
                    <div class="tech-used">
                        <div class="tech-stack-icons">
                            <img src="@/assets/icons/vue.svg" alt="Vue.js" class="tech-icon">
                            <img src="@/assets/icons/html.svg" alt="HTML" class="tech-icon">
                            <img src="@/assets/icons/css.svg" alt="CSS" class="tech-icon">
                            <img src="@/assets/icons/javascript.svg" alt="Javascript" class="tech-icon">
                        </div>
                        <GithubLink linkUrl="https://github.com/GhassanAlKaraan/vue-portfolio" />
                    </div>
                </div>



                <!-- Project Card 2 -->
                <div class="card">
                    <div class="project-image">
                        <img src="@/assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="@/assets/images/projects/ecommerce-project.png" class="img-2-mobile-app" />
                    </div>
                    <h4 class="project-title">Gas Station E-commerce App</h4>
                    <p>Crafted an e-commerce app with Firebase integration for user authentication and inventory
                        management, featuring an admin panel for product and order management.</p>
                    <div class="tech-used">
                        <div class="tech-stack-icons">
                            <img src="@/assets/icons/flutter.svg" alt="Flutter" class="tech-icon">
                            <img src="@/assets/icons/dart.svg" alt="Dart" class="tech-icon">
                            <img src="@/assets/icons/firebase.svg" alt="Firebase" class="tech-icon">
                        </div>
                        <GithubLink linkUrl="https://github.com/GhassanAlKaraan/petrol-n-gas" />
                    </div>
                </div>

                <!-- Project Card 3 -->
                <div class="card">
                    <div>
                        <div class="project-image">
                            <img src="@/assets/images/background/shiny-glass-2.png" class="img-1" />
                            <img src="@/assets/images/projects/smart-piggy-project.png" class="img-2-mobile-app-2" />
                        </div>
                        <h4 class="project-title">Smart Piggy</h4>
                        <p>Worked on this Flutter application that tracks your income and expenses through audio
                            commands, Integrated with GROQ AI API for Audio Analysis and Text Formatting Using Whisper
                            and Llama3 Models.</p>
                    </div>
                    <div class="tech-used">
                        <div class="tech-stack-icons">
                            <img src="@/assets/icons/flutter.svg" alt="Flutter" class="tech-icon">
                            <img src="@/assets/icons/dart.svg" alt="Dart" class="tech-icon">
                            <img src="@/assets/icons/ai.svg" alt="AI" class="tech-icon">
                        </div>
                        <GithubLink linkUrl="https://github.com/GhassanAlKaraan/smart-piggy" />
                    </div>
                </div>

                <!-- Project Card 4 -->
                <div class="card">
                    <div class="project-image">
                        <img src="@/assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="@/assets/images/projects/vue-demo-project.png" class="img-2" />
                    </div>
                    <h4 class="project-title">CRUD and Auth demo: Web App</h4>
                    <p>Learned to develop a full-stack web app with authentication and CRUD functionality using the MEVN
                        stack.</p>
                    <div class="tech-used">
                        <div class="tech-stack-icons">
                            <img src="@/assets/icons/vue.svg" alt="Vue" class="tech-icon">
                            <img src="@/assets/icons/javascript.svg" alt="Javascript" class="tech-icon">
                            <img src="@/assets/icons/mongo.svg" alt="Mongo" class="tech-icon">
                            <img src="@/assets/icons/nodejs.svg" alt="Node.js" class="tech-icon">
                            <img src="@/assets/icons/express.svg" alt="Express.js" class="tech-icon">
                        </div>
                        <GithubLink linkUrl="https://github.com/GhassanAlKaraan/vue3-app-demo" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 4rem 0;
}

.wrapper .container {
    max-width: 1100px;
    width: 100%;
}

.projects-heading {
    margin-bottom: 2rem;
}

.projects-heading h2 {
    font-size: 42px;
    color: #fff;
}

.projects-heading h2 span {
    color: var(--color-heading-secondary);
}

.container .projects-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
}

.card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;


    border: 1px solid rgba(105, 113, 162, 0.16);
    border-radius: 23px;
    overflow: hidden;
    position: relative;
    background: linear-gradient(to bottom right, #04071D, #0C0E23);
    padding: 1.5rem;
    color: #fff;
    transition: all 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 0 10px rgba(207, 207, 207, 0.2);
}

.project-image {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #13162D;
    border-radius: 14px;
    position: relative;
    width: 100%;
    height: 250px;
    margin-bottom: 1rem;
    overflow: hidden;
}

/* .project-image:has(.img-2-mobile-app) {
    overflow: visible;
} */
.project-image .img-1 {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    object-fit: cover;
    width: 100%;
    height: 100%;
}

.project-image .img-2 {
    border-radius: 7px;
    position: absolute;
    top: 10%;
    z-index: 2;
    object-fit: cover;
    transform: rotate(-5deg);
    width: 75%;
}

.project-image .img-2-mobile-app {
    position: absolute;
    top: -20%;
    z-index: 2;
    object-fit: cover;
    transform: rotate(5deg);
    width: 100%;
    filter: brightness(0.8);

}

.project-image .img-2-mobile-app-2 {
    position: absolute;
    top: -45%;
    z-index: 2;
    object-fit: cover;
    transform: rotate(5deg);
    width: 100%;
    filter: brightness(0.8);

}

.project-title {
    font-size: 28px;
    margin-bottom: 1rem;
}

p {
    line-height: 1.2;
    font-size: 20px;
    color: #BEC1DD;
    margin-bottom: 1rem;
}

.btn {
    text-decoration: none;
    color: #CBACF9;
    font-size: 1rem;
}

.btn:hover {
    background-color: white;
}

.tech-used {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 1rem;
}

.tech-used .tech-stack-icons .tech-icon {
    border: 1px solid rgba(105, 113, 162, 0.16);
    border-radius: 100%;
    background-color: #13162D;
    width: 44px;
    height: 44px;
    padding: 8px;

    margin-right: -6px;

    transition: all 0.2s ease;
    overflow: visible;
}

.tech-used .tech-stack-icons .tech-icon:hover {
    background-color: #04071D;
}
</style>
