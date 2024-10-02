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
                        <h4 class="experience-title">Software Developer <span class="at-symbol">@</span> GTS</h4>
                        <p>Contributed to JD Edwards ERP customization and worked on Odoo, Flutter projects.</p>
                    </div>

                </div>



                <!-- Experience Card 2 -->
                <div class="card">
                    <img src="@/assets/images/experience/mobile-dev.png" alt="Mobile Developer">
                    <div class="content">
                        <h4 class="experience-title">Mobile App Dev <span class="at-symbol">@</span> Kizana.co</h4>
                        <p>Lead frontend developer for Kizana app, managing features, maintenance, and UI/UX
                            improvements.</p>

                    </div>
                </div>

                <!-- Experience Card 3 -->
                <div class="card">
                    <img src="@/assets/images/experience/freelancer.png" alt="Freelance Developer">
                    <div class="content">
                        <h4 class="experience-title">Freelance App Dev</h4>
                        <p>Collaborated with clients on mobile and web projects, delivering customized solutions.</p>
                    </div>
                </div>

                <!-- Experience Card 4 -->
                <div class="card">
                    <img src="@/assets/images/experience/noc.png" alt="NOC Engineer">
                    <div class="content">
                        <h4 class="experience-title">NOC Engineer <span class="at-symbol">@</span> MobiMind</h4>
                        <p>Provided technical support for 200+ users, managing network and server infrastructure.</p>
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
    text-align: center;
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
    margin: 3rem;
}

.card {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 1.5rem;

    border: 1px solid rgba(105, 113, 162, 0.16);

    border-top: 5px solid rgba(105, 113, 162, 0.16);
    border-radius: 23px;
    overflow: hidden;
    position: relative;
    background: linear-gradient(to bottom right, #04071D, #0C0E23);
    padding: 1.5rem 2rem;
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

.card .at-symbol {
    color: var(--color-heading-secondary);
}

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

@media screen and (max-width: 1024px) {
    .experiences-heading h2 {
        font-size: 36px;
    }


}

@media screen and (max-width: 768px) {
    .experiences-heading {
        padding: 0 1rem;
    }

    .experiences-heading h2 {
        font-size: 26px;
    }

    .container .experiences-grid {
        grid-template-columns: 1fr;
    }
}


@media screen and (max-width: 580px) {

    p {
        font-size: 1rem;
    }

    .container .experiences-grid {
        margin: 1rem;
    }

}

@media screen and (max-width: 480px) {

    .card .content h4,
    .experience-title {
        font-size: 1.5rem;
        line-height: 1.1;
    }

    .card .content p {
        font-size: 0.8rem;
    }

    .card img {
        width: 60px;
        height: 60px;
    }

    .card {
        padding: 1rem;
    }


    .wrapper {
        padding: 2rem 0;
    }

    .wrapper .container {
        padding: 0 2rem;
    }

    .container .experiences-grid {
        margin: 0.5rem;
    }
}
</style>