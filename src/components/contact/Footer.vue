<template>
    <footer class="footer">
        <div class="footer-content">
            <p>Copyright ©2024 Ghassan Al Karaan</p>
            
            <div class="tech-used">
                <div class="tech-stack-icons">
                    <img src="@/assets/icons/email.svg" alt="Mongo" class="tech-icon">
                    <img src="@/assets/icons/linkedin.svg" alt="Node.js" class="tech-icon">
                    <img src="@/assets/icons/github.svg" alt="Express.js" class="tech-icon">
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
    display: flex;
    justify-content: space-between;
}



.tech-used {
    justify-content: center;
    align-items: center;
}

.tech-used .tech-stack-icons .tech-icon {
    /* border: 1px solid rgba(105, 113, 162, 0.16); */
    border-radius: 100%;
    background-color: #FFFFFFFF;
    width: 34px;
    height: 34px;
    padding: 4px;

    margin-right: 10px;

    transition: all 0.2s ease;
    overflow: visible;
}

.tech-used .tech-stack-icons .tech-icon:hover {
    background-color: #04071D;
}
</style>