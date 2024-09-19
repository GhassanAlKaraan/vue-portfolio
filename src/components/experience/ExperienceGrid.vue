<template>
    <div class="wrapper">
        <div class="experiences-heading">
            <h2>My <span>work experience</span></h2>
        </div>
        <div class="container">
            <div class="experiences-grid">

                <!-- Experience Card 1 -->
                <div class="card">
                    <img src="@/assets/images/experience/software-dev.png" alt="Software Developer">
                    <div class="content">
                        <h4 class="experience-title">Software Developer - GTS</h4>
                        <p>Developed this web portfolio to highlight my skills and experience.</p>
                    </div>

                </div>



                <!-- Experience Card 2 -->
                <div class="card">
                    <div class="content">
                        <h4 class="experience-title">Mobile App Dev - Kizana.co</h4>
                        <p>Crafted an e-commerce app with Firebase integration for user authentication and inventory.
                        </p>

                    </div>
                </div>

                <!-- Experience Card 3 -->
                <div class="card">
                    <div class="content">
                        <h4 class="experience-title">Freelance App Dev</h4>
                        <p>Worked on this Flutter application that tracks your income and expenses through audio
                            commands.</p>
                    </div>
                </div>

                <!-- Experience Card 4 -->
                <div class="card">
                    <div class="content">
                        <h4 class="experience-title">NOC Support Engineer - MobiMind</h4>
                        <p>Learned to develop a fullcation and CRUD functionality using the MEVN
                            stack.</p>
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

.experiences-heading {
    margin-bottom: 2rem;
}

.experiences-heading h2 {
    font-size: 42px;
    color: #fff;
}

.experiences-heading h2 span {
    color: var(--color-heading-secondary);
}

.container .experiences-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
}

.card {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 1.5rem;

    border: 1px solid rgba(105, 113, 162, 0.16);

    border-top: 5px solid rgba(105, 113, 162, 0.16);
    border-radius: 23px;
    overflow: hidden;
    position: relative;
    background: linear-gradient(to bottom right, #04071D, #0C0E23);
    padding: 2rem 2.5rem;
    color: #fff;
    transition: all 0.3s ease;
}

.card img {
    max-height: 87px;
    max-width: 95px;
}

.card .content {
    display: flex;
    flex-direction: column;
    justify-content: start;
}

/* .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 0 10px rgba(207, 207, 207, 0.2);
} */

.experience-title {
    font-size: 24px;
    margin-bottom: 0.5rem;
}

p {
    line-height: 1.2;
    font-size: 16px;
    color: #BEC1DD;
    margin-bottom: 1rem;
}
</style>