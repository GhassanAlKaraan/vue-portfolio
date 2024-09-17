<script setup></script>

<template>
    <div class="wrapper">
        <div class="projects-heading">
            <h2>A small selection of <span>recent projects</span></h2>
        </div>
        <div class="container">
            <div class="projects-grid">
                <!-- Project Card 1 -->
                <div class="card">
                    <div>
                        <div class="project-image">
                            <img src="../assets/images/background/shiny-glass-2.png" class="img-1" />
                            <img src="../assets/images/projects/project1.png" class="img-2" />
                        </div>
                        <h4 class="project-title">3D Solar System Planets to Explore</h4>
                        <p>Explore the wonders of our solar system with this captivating 3D simulation.</p>
                    </div>
                    <div class="tech-used">
                        <p>Tech Used: ...</p>
                        <a href="#" class="btn">Check Source Code</a>
                    </div>
                </div>

                <!-- Project Card 2 -->
                <div class="card">
                    <div class="project-image">
                        <img src="../assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="../assets/images/projects/project1.png" class="img-2" />
                    </div>
                    <h4 class="project-title">Yoom - Video Conferencing App</h4>
                    <p>Simplify your video conferencing experience.</p>
                    <div class="tech-used">
                        <p>Tech Used: ...</p>
                        <a href="#" class="btn">Check Source Code</a>
                    </div>
                </div>

                <!-- Project Card 3 -->
                <div class="card">
                    <div class="project-image">
                        <img src="../assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="../assets/images/projects/project1.png" class="img-2" />
                    </div>
                    <h4 class="project-title">AI Image SaaS - Canva Application</h4>
                    <p>A real software-as-a-service app with AI features.</p>
                    <div class="tech-used">
                        <p>Tech Used: ...</p>
                        <a href="#" class="btn">Check Source Code</a>
                    </div>
                </div>

                <!-- Project Card 4 -->
                <div class="card">
                    <div class="project-image">
                        <img src="../assets/images/background/shiny-glass-2.png" class="img-1" />
                        <img src="../assets/images/projects/project1.png" class="img-2" />
                    </div>
                    <h4 class="project-title">Animated Apple iPhone 3D Website</h4>
                    <p>Recreated the Apple iPhone 15 website.</p>
                    <div class="tech-used">
                        <p>Tech Used: ...</p>
                        <a href="#" class="btn">Check Source Code</a>
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
    gap: 2rem;
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
    padding: 2rem 1.5rem;
    color: #fff;
    transition: all 0.3s ease;
}

.card:hover {
    filter: brightness(1.2);

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
    position: absolute;
    top: 20%;
    z-index: 2;
    object-fit: cover;
    transform: rotate(3deg);
    max-width: 90%;
    max-height: 90%;
}

.project-title {
    font-size: 28px;
    margin-bottom: 1rem;
}

p {
    font-size: 20px;
    color: #BEC1DD;
    margin-bottom: 1rem;
}

.btn {
    text-decoration: none;
    color: white;
    font-size: 1rem;
}

.btn:hover {
    background-color: red;
}

.tech-used {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 1rem;
}
</style>
