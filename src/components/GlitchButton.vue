<script setup>
function openResume() {
    window.open('https://drive.google.com/file/d/1iEt3iOnuIHb7egvlZtm4o6NWUhqXsAMJ/view?usp=drive_link', '_blank');
}
</script>

<template>
<button class="resume-btn" @click="openResume" @mouseenter="startAnimation" @mouseleave="stopAnimation">
  <span>My Resume</span>&nbsp;<font-awesome-icon icon="arrow-up-right-from-square" />
</button>
</template>

<style scoped>
.resume-btn {
    background: linear-gradient(to left, rgba(4, 7, 29), rgba(16, 18, 48));
    color: #fff;
    padding: 1rem 2rem;
    font-weight: 400;
    font-size: 18px;
    cursor: pointer;
    border-radius: 13px;
    border: 1px solid rgba(105, 113, 162, 0.16);
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: Menlo, Roboto Mono, monospace;
}

.resume-btn span {
    letter-spacing: 0.1rem;
    transition: 0.3s;
    box-sizing: border-box;
    position: relative;
    background: inherit;
}

.resume-btn span::before {
    box-sizing: border-box;
    position: absolute;
    content: "";
    background: inherit;
}

.resume-btn:hover{
    background: rgba(4, 7, 29);
    box-shadow: 0 0 1000px 50px rgba(255, 255, 255, 0.5);
}

.resume-btn:hover span::before{
    animation: chitchat linear both 1.5s;
}

@keyframes chitchat {
    0% {
        content: "#";
    }

    5% {
        content: ".";
    }

    10% {
        content: "^{";
    }

    15% {
        content: "-!";
    }

    20% {
        content: "#$_";
    }

    25% {
        content: "№:0";
    }

    30% {
        content: "#{+.";
    }

    35% {
        content: "@}-?";
    }

    40% {
        content: "?{4@%";
    }

    45% {
        content: "=.,^!";
    }

    50% {
        content: "?2@%";
    }

    55% {
        content: "\;1}]";
    }

    60% {
        content: "?{%:%";
        right: 0;
    }

    65% {
        content: "|{f[4";
        right: 0;
    }

    70% {
        content: "{4%0%";
        right: 0;
    }

    75% {
        content: "'1_0<";
        right: 0;
    }

    80% {
        content: "{0%";
        right: 0;
    }

    85% {
        content: "]>'";
        right: 0;
    }

    90% {
        content: "4";
        right: 0;
    }

    95% {
        content: "2";
        right: 0;
    }

    100% {
        content: "";
        right: 0;
    }
}
</style>
