<template>
    <nav>
        <div class="links">
            <ul>
                <li v-for="section in sections" :key="section">
                    <a
                        :href="`#${section}`"
                        :class="{ active: activeSection === section }"
                        @click.prevent="scrollToSection(section)"
                    >
                        {{ section.charAt(0).toUpperCase() + section.slice(1) }}
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const sections = ['about', 'projects', 'experience', 'contact'];
const activeSection = ref('');

const setActiveSection = () => {
    const scrollY = window.scrollY;
    let currentSection = '';

    sections.forEach((section) => {
        const element = document.getElementById(section);
        if (element && element.offsetTop <= scrollY + 200) {
            currentSection = section;
        }
    });

    activeSection.value = currentSection;
};

const scrollToSection = (section) => {
    const element = document.getElementById(section);
    if (element) {
        window.scrollTo({
            top: element.offsetTop - 50, // Adjust for navbar height
            behavior: 'smooth'
        });
    }
};

onMounted(() => {
    window.addEventListener('scroll', setActiveSection);
});

onUnmounted(() => {
    window.removeEventListener('scroll', setActiveSection);
});
</script>

<style scoped>
nav {
    display: flex;
    align-items: center;
    justify-content: center;
    position: sticky;
    top: 0;
    padding-top: 2%;
    z-index: 1000;
}

.links {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: max-content;
    background: linear-gradient(to right, rgba(4, 7, 29, 0.8), rgba(16, 18, 48, 0.8));
    border-radius: 13px;
    border: 1px solid rgba(105, 113, 162, 0.16);
    z-index: 1000;
    padding: 1rem 2rem;
}

ul {
    display: flex;
    gap: 1rem;
    list-style: none;
}

li {
    font-size: 18px;
}

a {
    font-size: 16px;
    background: none;
    text-decoration: none;
    color: #C1C2D3;
    margin: 0 0.5rem;
    position: relative; /* Make sure the a tag can hold pseudo-elements */
    cursor: pointer;
}

a::after {
    content: "";
    display: block;
    width: 0;
    height: 0;
    height: 5px;
    background-color: transparent;
    border-radius: 100%;
    position: absolute;
    bottom: -22px;
    left: 50%;
    transform: translateX(-50%);
    transition: width 0.3s ease, background-color 0.3s ease;
}

a.active {
    color:white
}

.active::after {
    width: 7px;
    height: 7px;
    background-color: white;
}


a:hover {
    color: white;
}

@media (max-width: 480px) {
    .logo {
        display: none;
    }
}
</style>
