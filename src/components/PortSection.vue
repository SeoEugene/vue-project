<script setup>
import { portText } from "@/constants/index"
</script>

<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                protfolio <em>작업물</em>
            </div>
            <div class="port__wrap">
                <div class="port__item p1" v-for="(text, index) in portText" key="index">
                    <span class="num">{{ text.num }}</span>
                    <a href="#">
                        <img :src="text.img" alt="포트폴리오0{{ index +1 }}">
                    </a>
                    <h3 class="title">{{ text.title }}</h3>
                    <p class="desc">
                        {{ text.desc }}
                    </p>
                    <div class="code">{{ text.code }}</div>
                    <div class="view">{{ text.view }}</div>
                </div>
                <!-- //p1 -->
            </div>
        </div>
    </section>
    <!-- //port -->
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 3),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: true,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>

<style lang="scss">
#port {
    width: 100%;
    height: 100vh;
    overflow: hidden;
    background-color: #817C91;

}

.port__inner {
    padding: 16px;
}

.port__title {
    width: 100%;
    height: 85px;
    border-bottom: 0.4vw solid #000;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: 'Abril Fatface', serif;
    font-size: 3.8rem;
    color: #000;
}

.port__title em {
    font-size: 0.8rem;
    font-weight: 400;
    color: #000;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
    margin-top: 50px;
}

.port__item {
    width: 500px;
    height: 70vh;
    margin-right: 25px;
}

.port__item:nth-child(odd) {
    background-color: #576176;
}

.port__item:nth-child(even) {
    background-color: #AA98A9;
}

.port__item .num {
    display: flex;
    width: 100px;
    font-size: 3rem;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
    justify-content: left;
    margin-left: 30px;
    margin-top: 20px;
}

.port__item img {
    width: calc(100% - 60px);
    height: 45%;
    margin: 15px 30px;
}

.port__item .title {
    margin: 0 auto;
    width: 80%;
    font-size: 24px;
    text-align: center;
    border-bottom: 2px solid #000;
    padding-bottom: 8px;
    position: relative;
}

.port__item .title::before {
    content: '';
    width: 100%;
    height: 2px;
    background-color: #000;
    position: absolute;
    left: 0;
    bottom: -6px;
}

.port__item .desc {
    margin-top: 20px;
    text-align: center;
}
</style>