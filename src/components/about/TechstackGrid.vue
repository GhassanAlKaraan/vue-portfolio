<template>

    <div class="tech-stack-grid">
        <div class="card div1">Flutter</div>
        <div class="card div2">VueJs</div>
        <div class="card div3">Dart</div>
        <div class="card div4">Javascript</div>
        <div class="card div5">ExpressJs</div>
        <div class="card div6">SQL / noSQL</div>
        <div class="card div7"></div>
        <div class="card div8"></div>
    </div>

</template>

<style scoped>
.card {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #10132E;
    border-radius: 7px;
    font-size: 14px;
    font-weight: 500;
}

.tech-stack-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(7, 1fr);
    gap: 10px;
    width: 100%;
    height: 110%;
}

.div1 {
    grid-row: span 2 / span 2;
}

.div2 {
    grid-row: span 2 / span 2;
    grid-column-start: 2;
    grid-row-start: 2;
}

.div3 {
    grid-row: span 2 / span 2;
    grid-column-start: 1;
    grid-row-start: 3;
}

.div4 {
    grid-row: span 2 / span 2;
    grid-column-start: 2;
    grid-row-start: 4;
}

.div5 {
    grid-row: span 2 / span 2;
    grid-column-start: 1;
    grid-row-start: 5;
}

.div6 {
    grid-row: span 2 / span 2;
    grid-column-start: 2;
    grid-row-start: 6;
}

.div7 {
    grid-column-start: 1;
    grid-row-start: 7;
}

.div8 {
    grid-column-start: 2;
    grid-row-start: 1;
}

@media  screen and (max-width: 768px) {
    .card {
        padding: 0.5rem;
        font-size: 12px;
    }
    
}
</style>