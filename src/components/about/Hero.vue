<script setup>
import GlitchButton from "@/components/about/GlitchButton.vue";
</script>

<template>
    <div class="hero">

        <h3 class="hero-role">Bringing Any App Idea to Life with Flutter & Vue.js</h3>
        <h2 class="hero-title">
            Transforming Concepts into Seamless <span class="secondary-title">User Experiences</span>
        </h2>
        <h3 class="hero-about">Hi! I'm Ghassan, a Full-Stack Developer specializing in building apps.
        </h3>
        <GlitchButton />
    </div>
</template>

<style scoped>
.hero {
    padding: 10rem 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2rem;

}

.hero .hero-role {
    font-weight: 200;
    letter-spacing: 3px;
    font-size: 16px;
    TEXT-TRANSFORM: UPPERCASE;
    color: #E4ECFF;
    text-align: center;
}

.hero .hero-about {
    font-weight: 200;
    font-size: 24px;
    color: #E4ECFF;
    text-align: center;
}

.hero .hero-title {
    line-height: 1;
    word-spacing: -5px;
    text-align: center;
    max-width: 1100px;
    font-size: 72px;
    color: var(--color-heading-primary);
}

.hero .hero-title .secondary-title {
    color: var(--color-heading-secondary);
}

.hero .resume-btn {
    background: linear-gradient(to left, rgba(4, 7, 29), rgba(16, 18, 48));
    color: #fff;
    padding: 1rem 2rem;
    font-weight: 400;
    font-size: 18px;
    cursor: pointer;
    border-radius: 13px;
    border: 1px solid rgba(105, 113, 162, 0.16);
    transition: all 0.3s ease;
}

.hero .resume-btn:hover, .hero .resume-btn:focus {
    background: rgba(4, 7, 29);
    box-shadow: 0 0 1000px 50px rgba(255, 255, 255, 0.5);
    outline: none;
}

@media screen and (max-width: 1024px) {
    .hero .hero-title {
        font-size: 60px;
    }

    .hero .hero-role {
        font-size: 16px;
    }

    .hero .hero-about {
        font-size: 22px;
    }
}

@media screen and (max-width: 768px) {
    .hero {
        padding: 7rem 2rem;
    }
    .hero .hero-title {
        font-size: 50px;
    }
    .hero .hero-role {
        font-size: 14px;
    }

    .hero .hero-about {
        font-size: 20px;
    }
}
@media screen and (max-width: 480px) {
    .hero .hero-title {
        font-size: 40px;
    }
    .hero .hero-role {
        font-size: 12px;
    }

    .hero .hero-about {
        font-size: 18px;
    }
    
    }
</style>