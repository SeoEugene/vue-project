<script setup>
import { skillText } from "@/constants/index"
</script>

<template>
    <section id="skill">
        <div class="skill__inner">
            <div class="skill__title">
                <h2>chanllenge <em>나의 도전</em></h2>
            </div>
            <div class="skill__desc">
                <div v-for="( text, index) in skillText" key="index">
                    <span>{{ index + 1 }}</span>
                    <h3>{{ text.title }}</h3>
                    <p>
                        {{ text.desc }}
                    </p>
                </div>
            </div>
        </div>
    </section>
    <!-- //skill -->
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Questrial&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Montserrat:wght@100;200;300;400;500;600;700;800;900&family=Nanum+Myeongjo:wght@400;700;800&display=swap');

.skill__inner {
    width: 100%;
    padding: 16px;
    display: flex;
    justify-content: space-between;
    background-color: rgb(128, 128, 128);
}

.skill__title {
    position: sticky;
    top: 70px;
    left: 0;
    /* height: 500px; */
    height: 100vh;
    width: 50%;
    border-right: 0.4vw solid #2b3642;
}

.skill__title h2 {
    height: 85px;
    border-bottom: 0.4vw solid #2b3642;
    font-weight: 4vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: 'Abril Fatface', serif;
    font-size: 3.8rem;
    color: #2b3642;
}

.skill__title em {
    font-size: 0.8rem;
    font-weight: 400;
    font-family: 'Questrial', sans-serif;
}

.skill__desc {
    width: 50%;
    font-family: 'Questrial', sans-serif;
    color: #2b3642;
}

.skill__desc>div {
    margin-bottom: 200px;
}

.skill__desc>div:last-child {
    margin-bottom: 50px;
}

.skill__desc span {
    font-family: 'Abril Fatface', serif;
    font-size: 4rem;
    margin-left: 20px;

}

.skill__desc h3 {
    font-size: 2rem;
    font-family: 'Questrial', sans-serif;
    text-decoration: underline;
    text-underline-offset: 0.2em;
    margin-left: 40px;
    padding-bottom: 5px;
}

.skill__desc p {
    margin-left: 40px;
    padding: 10px;
    line-height: 1.8;
}

@media (max-width: 1000px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        border-right: none;
    }

    .skill__desc {
        width: 100%;
        font-size: 2vw;
    }
}

@media (max-width: 800px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
    }

    .skill__desc h3 {
        font-size: 1.5rem;
    }

    .skill__desc {
        font-size: 1rem;
    }
}
</style>