<script setup>

import { ref } from 'vue';

const props = defineProps({
    onSubmit: {
        type: Function,
        required: true
    }
});

const state = ref({
    isLoading: false,
});

const handleSubmit = () => {
    state.isLoading = true;
    try {
        props.onSubmit();
    } catch (e) {
        console.error(e);
    } finally {
        state.isLoading = false;
        //TODO: tell the user the message was sent
    }
};

</script>

<template>
    <button class="submit-btn" @click="handleSubmit">
        <span>Submit</span>&nbsp;<font-awesome-icon icon="arrow-up-right-from-square" />
    </button>
</template>

<style scoped>
.submit-btn {
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

.submit-btn span {
    letter-spacing: 0.1rem;
    transition: 0.3s;
    box-sizing: border-box;
    position: relative;
    background: inherit;
}

.submit-btn span::before {
    box-sizing: border-box;
    position: absolute;
    content: "";
    background: inherit;
}

.submit-btn:hover, .submit-btn:focus {
    background: rgba(4, 7, 29);
    box-shadow: 0 0 1000px 50px rgba(255, 255, 255, 0.5);
    outline: none;
}

.submit-btn:hover span::before, .submit-btn:focus span::before {
    animation: chitchat linear both 1.2s;
    outline: none;
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
