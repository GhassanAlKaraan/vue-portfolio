<script setup>
function handleClick() {
    window.open("https://github.com/GhassanAlKaraan", "_blank");
}
</script>

<template>
    <a href="https://github.com/GhassanAlKaraan" target="_blank" @click.prevent="handleClick">
        <article>
            <p class="example-right">See more on GitHub      See more on GitHub      See more on GitHub      See more on GitHub    
                See more on GitHub      See more on GitHub      See more on GitHub      See more on GitHub      See more on GitHub    
                See more on GitHub      </p>
        </article>
    </a>
</template>

<style scoped>
a {
    text-decoration: none;
    color: inherit;
}

article {
    width: 100%;
    overflow: hidden;
    position: relative;
    min-height: 4em;
}

article p {
    text-decoration: underline;
    font-size: 18px;
}

p:hover {
    text-decoration: none;
}

/* Safari 4.0 - 8.0 */
@-webkit-keyframes mymove {
    from {
        left: 0;
    }

    to {
        left: -140px;
    }
}

@keyframes mymove {
    from {
        left: 0;
    }

    to {
        left: -140px;
    }
}


.example-right {
    white-space: nowrap;
    position: absolute;
    /* top:2em; */
    /* opacity: .4; */
    text-transform: uppercase;
}

.example-right {
    -webkit-animation: urmove 8s linear infinite;
    /* Safari 4.0 - 8.0 */
    white-space: nowrap;
    animation: urmove 8s linear infinite alternate;
}

.example-right {
    cursor: pointer;
    transition: all 0.3s ease;
}

.example-right:hover {
    padding: 4px 0;
    color: black;
    background-color: #BEC1DD;
    transform: scale(1.2);
}

/* Safari 4.0 - 8.0 */
@-webkit-keyframes urmove {
    from {
        right: 0;
    }

    to {
        right: -140px;
    }
}

@keyframes urmove {
    from {
        right: 0;
    }

    to {
        right: -140px;
    }
}


@keyframes early {
    from {
        opacity: 1;
    }

    to {
        opacity: 0;
    }
}

.early {
    animation: fadeIn ease-in 1;
    /* call our keyframe named fadeIn, use animation ease-in and repeat it only 1 time */

    animation-fill-mode: forwards;
    /* this makes sure that after animation is done we remain at the last keyframe value (opacity: 1)*/

    animation-duration: 1s;
    animation-delay: 1.5s
}
</style>