<script setup>
function openLinkedIn() {
    window.open('https://linkedin.com/in/ghassan-alkaraan', '_blank');
}
function openGithub() {
    window.open('https://github.com/ghassanalkaraan', '_blank');
}
function openEmail() {
    window.open('mailto:ghass.karaan@gmail.com', '_blank');
}
</script>
<template>
    <footer class="footer">
        <div class="footer-content">
            <p>Copyright ©2024 Ghassan Al Karaan</p>

            <div class="tech-used">
                <div class="tech-stack-icons">
                    <img src="@/assets/icons/linkedin.svg" alt="Linkedin" class="social-icon" @click="openLinkedIn">
                    <img src="@/assets/icons/github.svg" alt="Github" class="social-icon" @click="openGithub">
                    <img src="@/assets/icons/email.svg" alt="Email" class="social-icon" @click="openEmail">
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    height: 70px;
    color: white;
    font-size: 14px;
    display: flex;
    justify-content: center;
}

.footer-content {
    max-width: 1100px;
    width: 100%;
    margin: 0 1rem;
    display: flex;
    justify-content: space-between;
}

.tech-used {
    justify-content: center;
    align-items: center;
}

.tech-used .tech-stack-icons .social-icon {
    width: 34px;
    height: 34px;

    margin-right: 12px;
    cursor: pointer;
    transition: all 0.2s ease;
    overflow: visible;
}

.tech-used .tech-stack-icons .social-icon:hover, .tech-used .tech-stack-icons .social-icon:focus {
    transform: translateY(-4px);
    outline: none;
}

@media screen and (max-width: 480px) {
    .footer {
        margin-bottom: 1rem;
    }
    .footer-content {
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        gap: 1rem;
    }
    .tech-used .tech-stack-icons .social-icon {
        
    width: 30px;
    height: 30px;}
    
}
</style>