<script setup>
import { siteText } from "@/constants/index"
</script>

<template>
    <section id="site">
        <div class="site__inner">
            <div class="site__title">
                Site Coding <em>나의 작업물</em>
            </div>

            <div class="site__wrap">
                <div class="site__item s1" v-for="(text, index) in siteText" key="index">
                    <span class="num">{{ index + 1 }}</span>
                    <div class="text">
                        <div>{{ text.text[0] }}</div>
                        <div>{{ text.text[1] }}</div>
                        <div>{{ text.text[2] }}</div>
                    </div>
                    <h3 class="title">
                        {{ text.title }}
                    </h3>
                    <div class="btn">
                        <a href="#">code : {{ text.code }}</a>
                        <a href="#">view : {{ text.view }}</a>
                    </div>
                    <div class="info">
                        <span>{{ text.info[0] }}</span>
                        <span>{{ text.info[1] }}</span>
                        <span>{{ text.info[2] }}</span>
                    </div>
                </div>
                <!-- //s1 -->

            </div>
            <!-- //site__wrap -->
        </div>
        <!-- //site__inner -->
    </section>
    <!-- //site -->
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Questrial&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Montserrat:wght@100;200;300;400;500;600;700;800;900&family=Nanum+Myeongjo:wght@400;700;800&display=swap');

.site__inner {
    padding: 16px;
    display: block;
    background-color: rgb(128, 128, 128);
    color: #2b3642;
}

.site__title {
    position: sticky;
    top: 80px;
    left: 0;
    width: 100%;
    height: 85px;
    border-bottom: 0.4vw solid rgb(128, 128, 128);
    ;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: 'Abril Fatface', serif;
    font-size: 3.8rem;
}

.site__title em {
    font-size: 0.8rem;
    font-weight: 300;
    font-family: 'Questrial', sans-serif;
}

.site__wrap {
    border-bottom: 3px solid #2b3642;
    ;

}

.site__item {
    padding-left: 20px;
    height: 70vh;
    flex-direction: column;
    position: sticky;
    top: 0;
    background-color: rgb(128, 128, 128);
    ;
}

.site__item .num {
    font-family: 'Abril Fatface', serif;
    font-size: 4rem;
}

.site__item .text {
    margin-top: 50px;
}

.site__item .title {
    font-size: 1.8rem;
    margin: 50px 0 20px 0;
}

.site__item.s1 {
    top: 180px;
    background-color: #9a9a9a;
}

.site__item.s2 {
    top: 200px;
    background-color: #b5b5b5;
}

.site__item.s3 {
    top: 220px;
    background-color: #d0d0d0;
}

.site__item.s4 {
    top: 240px;
    background-color: #ededed;
}

.site__item .btn {
    display: flex;
}

.site__item .btn a {
    display: flex;
    width: 50%;
    margin: 0 5px;
    border: 3px solid #2b3642;
    border-radius: 5px;
    padding: 10px 0;
    justify-content: center;
}

.site__item .info {
    display: block;
    margin-top: 50px;
}

.site__item .info span {
    display: flex;
    font-size: 18px;
}
</style>