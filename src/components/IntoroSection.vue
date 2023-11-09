<template>
    <section id="intro">
        <div class="intro__inner">
            <div class="intro__title">Web Portfolio using Vite</div>

            <div class="intro__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="intro__text">
                <div class="img"></div>
                <div class="text">
                    <p>Welcome to</p>
                    <p>my first web site,</p>
                    <p>enjoy</p>
                    <p>unique webdesign.</p>
                </div>
            </div>
            <div class="intro__lines bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>

        </div>
    </section>
    <!-- //intro -->
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Montserrat:wght@100;200;300;400;500;600;700;800;900&family=Nanum+Myeongjo:wght@400;700;800&display=swap');

#intro {
    height: 100vh;
    background-color: rgb(128, 128, 128);
}

.intro__inner {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1vw;
}

.intro__title {
    font-size: 9vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
    line-height: 0.88;
    letter-spacing: 0.1vw;
    z-index: 100;
    color: #2b3642;
}

.intro__lines {
    display: block;
    width: 100%;

}

.intro__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: #2b3642;
    margin-bottom: 0.5vw;
}

.intro__lines .line:nth-child(1) {
    height: 1px;
}

.intro__lines .line:nth-child(2) {
    height: 2px;
}

.intro__lines .line:nth-child(3) {
    height: 3px;
}

.intro__lines .line:nth-child(4) {
    height: 4px;
}

.intro__lines .line:nth-child(5) {
    height: 5px;
}

.intro__lines .line:nth-child(6) {
    height: 6px;
}

.intro__lines .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom {
    display: none;
}

.intro__lines.bottom .line:nth-child(1) {
    height: 7px;
}

.intro__lines.bottom .line:nth-child(2) {
    height: 6px;
}

.intro__lines.bottom .line:nth-child(3) {
    height: 5px;
}

.intro__lines.bottom .line:nth-child(4) {
    height: 4px;
}

.intro__lines.bottom .line:nth-child(5) {
    height: 3px;
}

.intro__lines.bottom .line:nth-child(6) {
    height: 2px;
}

.intro__lines.bottom .line:nth-child(7) {
    height: 1px;
}

.intro__text {
    /* background-color: #fff; */
    width: 100%;
    /* height: 37vh; */
    padding: 10vw 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #2b3642;
    position: relative;
}

.intro__text .img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-size: cover;
    background-position: center;
    width: 200px;
    height: 20vh;
    background-image: url(../assets/img/magazine2.jpg);
    border-radius: 50%;
}

.intro__text .text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.2);
}

.intro__text .text p {
    text-align: center;
    font-size: 2.6vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Nanum Myeongjo', serif;
    color: #92d4c0;
    text-decoration: underline;
}

@media (max-width: 1080px) {
    .intro__text .img {
        width: 150px;
        height: 15vh;
    }
}

@media (max-width: 800px) {
    .intro__inner {
        align-items: center;
        justify-content: center;
    }

    .intro__lines.bottom {
        display: block;
    }

    .intro__text .text {
        font-size: 30px;
    }

    .intro__text .text:nth-child(2) {
        /* filter: brightness(); */
    }

    .intro__text img {
        width: 300px;
        height: 300px;
    }

    .intro__lines.bottom {
        display: block;
    }
}
</style>