<script setup>
import { defineProps } from 'vue';

// Defining the props with a default link URL
const props = defineProps({
    linkUrl: {
        type: String,
        default: 'https://github.com/GhassanAlKaraan'
    }
});

// Function to open the link in a new tab
function openLink() {
    window.open(props.linkUrl, '_blank');
}
</script>

<template>
    <!-- Button for linking to the GitHub source -->
    <button class="github-link" @click="openLink">
        <span>Check Source Code</span>
    </button>
</template>

<style scoped>
/* Styling the button */
.github-link {
    background: none;
    border: none;
    padding: 0.5rem 1rem;
    font-weight: 400;
    text-decoration: none;
    color: #CBACF9; /* Light purple color */
    font-size: 1rem;
    cursor: pointer;
    transition: color 0.3s ease; /* Smooth color transition */
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: Menlo, Roboto Mono, monospace;
    position: relative;
}

/* Hover effect: changes the text color to white */
.github-link:hover {
    color: #FFFFFF;
}

/* Styling the span that contains the text */
.github-link span {
    position: relative;
    padding-bottom: 0.2rem; /* Space for underline */
}

/* Underline effect */
.github-link span::after {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 2px; /* Thickness of the underline */
    background-color: #CBACF9; /* Same color as the text */
    transform: scaleX(0); /* Initially hidden */
    transition: transform 0.3s ease-in-out; /* Smooth animation */
}

/* Hover state for the underline */
.github-link:hover span::after {
    transform: scaleX(1); /* Expands the underline */
}
</style>
