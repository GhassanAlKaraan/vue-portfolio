<template>
    <nav :class="{ hidden: isNavbarHidden }">
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
const activeSection = ref('about');
const isNavbarHidden = ref(false);
let lastScrollY = 0;
let scrollTimeout = null;

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

const handleScroll = () => {
    const currentScrollY = window.scrollY;

    if (currentScrollY > lastScrollY) {
        isNavbarHidden.value = true; // Hide navbar when scrolling down
    } else {
        isNavbarHidden.value = false; // Show navbar when scrolling up
    }

    lastScrollY = currentScrollY;
    setActiveSection();

    // Debounce for detecting scroll stop
    if (scrollTimeout) {
        clearTimeout(scrollTimeout);
    }
    scrollTimeout = setTimeout(() => {
        isNavbarHidden.value = false; // Show navbar after scroll stop
    }, 150); // Adjust delay as needed
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
    window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
});
</script>


<style scoped>
nav {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    padding-top: 2%;
    z-index: 1000;
    transition: transform 0.3s ease-in-out;
}

nav.hidden {
    transform: translateY(-120%);
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
    padding: 1rem 0.5rem;
}

ul {
    display: flex;
    /* gap: 1rem; */
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

    padding: 1rem 0.5rem;
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
    bottom: -8px;
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


a:hover, a:focus {
    color: white;
    outline: none;
}

@media screen and (max-width: 480px) {

    a{
        font-size: 14px;
    }
}
</style>
