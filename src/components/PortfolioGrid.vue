<script setup>
import TechstackGrid from "@/components/TechstackGrid.vue";
import CopyButton from "@/components/CopyButton.vue";
</script>


<template>

    <div class="wrapper">
        <div class="container">
            <div class="grid">
                <div class="card div1">
                    <img src="../assets/images/about/collab.png" alt="Collab Image" class="collab-img">
                    <img src="../assets/images/about/cursor1.png" alt="Cursor1 Image" class="cursor1-img">
                    <img src="../assets/images/about/cursor2.png" alt="Cursor2 Image" class="cursor2-img">
                    <p class="collab-text">
                        I prioritize client collaboration, fostering open communication
                    </p>
                </div>
                <div class="card div2">
                    <img src="../assets/images/about/globe.png" alt="Globe Image" class="time-zone-globe-img">
                    <img src="../assets/images/background/bg-bright-grid.png" class="bright-grid-img">
                    <p class="time-zone-text">
                        I'm very flexible with time zone communications
                    </p>
                    <img src="../assets/images/about/glass.png" alt="Shiny Glass" class="shiny-glass-img">
                </div>
                <div class="card div3">
                    <div class="text">
                        <p>I constantly try to improve</p>
                        <p class="tech-stack-text">
                            My Tech Stack
                        </p>
                    </div>
                    <div class="tech-stack-grid-container">
                        <TechstackGrid />
                    </div>
                </div>
                <div class="card div5">
                    <p>Tech enthusiast with a passion for development.</p>
                    <img src="../assets/images/about/tab.png" alt="Tab" class="tab-img">
                    <img src="../assets/images/background/bg-bright-grid.png" class="bright-grid-img">
                </div>
                <div class="card div6">
                    <img src="../assets/images/background/bg-color-blur.png" class="color-blur-img">
                    <div class="text">
                        <p>Do you want to start a project together?</p>
                        <CopyButton />
                    </div>
                </div>
                <div class="card div7">
                    <div class="text">
                        <p>The inside scoop</p>
                        <p class="building-text">
                            Currently building a community website
                        </p>
                    </div>
                    <img src="../assets/images/background/bg-bright-grid.png" class="bright-grid-img">
                    <img src="../assets/images/background/bg-code-editor.png" class="code-editor-img">
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: 4rem;
}

.wrapper .container {
    max-width: 1100px;
}

.card {
    border: 1px solid rgba(105, 113, 162, 0.16);
    border-radius: 23px;
    overflow: hidden;
    position: relative;
}

.card p {
    line-height: 1.2;
}

.div1 .collab-img {
    width: 100%;
    height: 100%;
    object-fit: cover;

}

.div1 .collab-text {
    position: absolute;
    bottom: 0;
    left: 0;
    max-width: 60%;
    text-align: left;
    font-size: 32px;
    font-weight: 700;
    color: #fff;
    margin-left: 2rem;
    margin-bottom: 4rem;
    z-index: 3;
}

.div1 .cursor1-img {
    position: absolute;
    top: 20%;
    left: 10%;
    z-index: 2;
}

.div1 .cursor2-img {
    position: absolute;
    bottom: 30%;
    right: 15%;
    z-index: 2;
}

.div2 .time-zone-globe-img {
    position: absolute;
    bottom: 0;
    z-index: 1;
}

.div2 .shiny-glass-img {
    position: absolute;
    bottom: 0;
    z-index: 0;
}

.div2 .time-zone-text {
    position: absolute;
    top: 0;
    left: 0;
    max-width: 90%;
    text-align: left;
    font-size: 28px;
    font-weight: 700;
    color: #fff;
    margin-top: 4rem;
    margin-left: 1rem;
    z-index: 3;
}

.div2 .shiny-glass-img,
.div2 .time-zone-globe-img {
    opacity: 0.7;
}

.div3 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;

    background: linear-gradient(45deg, #04071D, #0C0E23);
}

.div3 .text {
    position: absolute;
    left: 0;
    margin-left: 1rem;
    z-index: 3;
}

.div3 p {
    color: #C1C2D3;
    font-weight: 200;
    margin-bottom: 0.5rem;
}

.div3 .tech-stack-text {
    text-align: left;
    font-size: 32px;
    font-weight: 700;
    color: #fff;
}

.div3 .tech-stack-grid-container {
    position: absolute;
    z-index: 1;
    right: 0;
    top: -10px;
    width: 55%;
    height: 100%;
    padding: 0 1rem;
}

.div5 p {
    position: absolute;
    z-index: 3;
    padding: 2rem;
    text-align: left;
    font-size: 24px;
    font-weight: 700;
    color: #fff;
}

.div5 .tab-img {
    position: absolute;
    bottom: 0;
    right: 0;
    z-index: 2;
}

.div6 p {
    font-size: 24px;
    font-weight: 700;
    width: 60%;
}

.div6 .text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    position: absolute;
    z-index: 3;
    padding: 1rem;

    text-align: center;
    color: #fff;
}

.div7 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
}

.div7 .code-editor-img {
    position: absolute;
    bottom: -30px;
    right: 0;
    z-index: 1;
}

.div7 .text {
    position: absolute;
    z-index: 3;
    left: 0;    
    margin-left: 2rem;
}

.div7 p {
    text-transform: uppercase;
    color: #C1C2D3;
    font-weight: 200;
    margin-bottom: 0.5rem;
    font-size: 16px;
}

.div7 .building-text {
    max-width: 70%;
    text-align: left;
    font-size: 30px;
    font-weight: 700;
    color: #fff;
    z-index: 3;
}

/* Grid layout */

.grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(10, 1fr);
    gap: 1.5rem;
}

.div1 {
    grid-column: span 3 / span 3;
    grid-row: span 6 / span 6;
}

.div2 {
    grid-column: span 2 / span 2;
    grid-row: span 3 / span 3;
    grid-column-start: 4;
}

.div3 {
    grid-column: span 2 / span 2;
    grid-row: span 3 / span 3;
    grid-column-start: 4;
    grid-row-start: 4;
}

.div5 {
    grid-column: span 2 / span 2;
    grid-row: span 2 / span 2;
    grid-row-start: 7;
}

.div6 {
    grid-column: span 2 / span 2;
    grid-row: span 2 / span 2;
    grid-column-start: 1;
    grid-row-start: 9;
}

.div7 {
    grid-column: span 3 / span 3;
    grid-row: span 4 / span 4;
    grid-column-start: 3;
    grid-row-start: 7;
}

/* Utility */
.bright-grid-img {
    position: absolute;
    z-index: 1;
    width: 100%;
    height: 100%;
    object-fit: center/cover;
}

.color-blur-img {
    position: absolute;
    z-index: 1;
    width: 100%;
    height: 100%;
    object-fit: center/cover;
}

</style>