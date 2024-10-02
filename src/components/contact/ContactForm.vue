<template>
    <div class="wrapper">
        <div class="contact-heading">
            <img src="@/assets/images/background/bg-bright-grid.png" class="bright-grid-img">
            <h2>Ready to take <span>your</span> digital presence to the next level?</h2>
            <p>Reach out to me today and let's discuss how I can help you achieve your goals.</p>
        </div>
        <div class="container">
            <form name="contact" netlify>
                <input type="hidden" name="form-name" value="contact">
                <div class="form-group">
                    <input type="text" id="name" v-model="name" placeholder="Name" required>
                </div>
                <div class="form-group">
                    <input type="email" id="email" v-model="email" placeholder="Email" required>
                </div>
                <div class="form-group">
                    <textarea id="message" v-model="message" placeholder="Your Message" required></textarea>
                </div>
                <button type="submit" class="submit-btn"><span>Send Message</span></button>
            </form>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 4rem 0;
}

.wrapper .container {
    max-width: 1100px;
    width: 100%;
    position: relative;
    z-index: 2;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.contact-heading {
    position: relative;
    overflow: visible;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 2rem;
}

.contact-heading p {
    line-height: 1.2;
    font-size: 16px;
    color: #BEC1DD;
    margin: 1.5rem;
    position: relative;
    z-index: 2;
}

.contact-heading h2 {
    max-width: 60%;
    line-height: 1;
    text-align: center;
    font-size: 42px;
    color: #fff;
    position: relative;
    z-index: 2;
}

.contact-heading h2 span {
    color: var(--color-heading-secondary);
}

.bright-grid-img {
    position: absolute;
    z-index: 1;
    width: 100%;
    object-fit: center/cover;
    pointer-events: none;
}

form {
    display: flex;
    flex-direction: column;
    justify-content: center;
    
    gap: 1rem;
    width: 60%;
    position: relative;
    z-index: 2;

    /* border: 1px solid red; */
}

.form-group {
    display: flex;
    flex-direction: column;
}

/* label {
    font-weight: 200;
    font-size: 24px;
    color: #E4ECFF;
} */

input, textarea {
    padding: 0.5rem;
    border: 1px solid rgba(105, 113, 162, 0.16);
    border-radius: 7px;
    background-color: rgba(255, 255, 255, 0.1);
    line-height: 1.2;
    font-size: 16px;
    color: #BEC1DD;

    transition: all 0.3 ease;
}

input:focus, textarea:focus {
    outline: none;
    border-color: var(--color-heading-secondary);
    box-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
}

textarea {
    height: 150px;
    resize: vertical;
    font-family: inherit;
}

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

.submit-btn:hover {
    background: rgba(4, 7, 29);
}

.submit-btn:hover span::before {
    animation: chitchat linear both 1.2s;
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

@media screen and (max-width: 1024px) {
    .contact-heading h2 {
        font-size: 36px;
    }
    form {
        width: 70%;
    }
    
}

@media screen and (max-width: 768px) {
    .contact-heading {
        padding: 0 1rem;
    }

    .contact-heading h2 {
        font-size: 26px;
    }
    form {
        width: 80%;
    }
}


@media screen and (max-width: 580px) {

    p {
        font-size: 1rem;
    }



}

@media screen and (max-width: 480px) {

    .contact-heading h2 {
        max-width: 90%;}

    .contact-heading p {
        font-size: 0.8rem;
    }

    .card img {
        width: 60px;
        height: 60px;
    }

    .card {
        padding: 1rem;
    }


    .wrapper {
        padding: 2rem 0;
    }

    .wrapper .container {
        padding: 0 2rem;
    }

    .container .experiences-grid {
        margin: 0.5rem;
    }

    form {
        width: 100%;
        margin: 0 1rem;
    }
}
</style>