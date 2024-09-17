<script setup>
import { ref } from 'vue';

const emailCopied = ref(false);

const copyEmail = () => {
    const email = 'ghass.karaan@gmail.com';
    navigator.clipboard.writeText(email)
        .then(() => {
            emailCopied.value = true;
            setTimeout(() => {
                emailCopied.value = false;
            }, 2000);
        })
        .catch(err => {
            console.error('Failed to copy email: ', err);
        });
};
</script>

<template>
    <button class="copy-email-btn" @click="copyEmail">
        <div :class="['email-to-be-copied', { hidden: emailCopied }]">
            <font-awesome-icon icon="copy" />  Copy my email address
        </div>
        <div :class="['email-copied', { show: emailCopied }]">Email Copied!</div>
    </button>
</template>


<style scoped>
.copy-email-btn {
    position: relative;
    display: inline-block;
    color: #E4ECFF;
    border: 1px solid rgba(105, 113, 162, 0.16);
    border-radius: 7px;
    padding: 0.75rem 2rem;
    background: linear-gradient(to right, #161A31, #06091F);
    font-size: 14px;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
    width: 200px;
    /* Set a fixed width */
    height: 40px;
    /* Set a fixed height */
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
}

.copy-email-btn:hover {
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
}

.email-to-be-copied,
.email-copied {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    transition: all 0.3s ease-in-out;
    white-space: nowrap;
}

.email-to-be-copied.hidden {
    opacity: 0;
    transform: translate(-50%, 100%);
    /* Move down */
}

.email-copied {
    opacity: 0;
    transform: translate(-50%, 100%);
}

.email-copied.show {
    opacity: 1;
    transform: translate(-50%, -50%);
    /* Move up */
}
</style>