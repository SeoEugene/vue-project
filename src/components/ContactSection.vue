<template>
    <section id="contact">
        <div class="contact__inner">
            <h2 class="contact__title">Contact</h2>

            <div class="contact__line" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>

            <div class="contact__text">
                <div class="text">
                    <div>
                        <div class="sns">Kakao</div>
                        <a href="#"> Eugene_s. </a>
                    </div>
                    <div>
                        <div class="sns">Mail</div>
                        <a href="#"> 97.eugene.s@gamil.com </a>
                    </div>
                    <div>
                        <div class="sns">Instagram</div>
                        <a href="#"> Yujin.s0322</a>
                    </div>
                    <div>
                        <div class="sns">Github</div>
                        <a href="#"> SeoEugene </a>
                    </div>
                    <div>
                        <div class="sns">Blog</div>
                        <a href="#"> SeoEugene </a>
                    </div>
                </div>
            </div>

            <div class="contact__line bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
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
</template>

<style lang="scss">
#contact {
    height: 100vh;
    background-color: #817C91;

}

.contact__inner {}

.contact__title {
    font-size: 9vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
    line-height: 0.88;
    letter-spacing: 0.1vw;
    z-index: 100;
    color: #1f1717;
}

.contact__line {
    display: block;
    width: 100%;
    color: #fff;

}

.contact__line .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: #1f1717;
    margin-bottom: 0.5vw;
}

.contact__line .line:nth-child(1) {
    height: 1px;
}

.contact__line .line:nth-child(2) {
    height: 2px;
}

.contact__line .line:nth-child(3) {
    height: 3px;
}

.contact__line .line:nth-child(4) {
    height: 4px;
}

.contact__line .line:nth-child(5) {
    height: 5px;
}

.contact__line .line:nth-child(6) {
    height: 6px;
}

.contact__line .line:nth-child(7) {
    height: 7px;
}

.contact__line.bottom {
    /* display: none; */
}

.contact__line.bottom .line:nth-child(1) {
    height: 7px;
}

.contact__line.bottom .line:nth-child(2) {
    height: 6px;
}

.contact__line.bottom .line:nth-child(3) {
    height: 5px;
}

.contact__line.bottom .line:nth-child(4) {
    height: 4px;
}

.contact__line.bottom .line:nth-child(5) {
    height: 3px;
}

.contact__line.bottom .line:nth-child(6) {
    height: 2px;
}

.contact__line.bottom .line:nth-child(7) {
    height: 1px;
}

.contact__text {
    /* background-color: #fff; */
    width: 100%;
    height: 37vh;
    padding: 10vw 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #1f1717;
    position: relative;
}

.contact__text .text {
    display: flex;
    /* border: 1px solid orange; */
    width: 90%;
}

.contact__text .text>div {
    width: 20%;
    height: 200px;
    color: #fff;
    font-size: 24px;
    padding: 20px;
    word-wrap: break-word
}

.contact__text .text .sns {
    /* border: 1px solid red; */
}

.contact__text .text>div:nth-child(1) .sns {
    color: #fff700;
    border-bottom: 2px solid #fff700;
}

.contact__text .text>div:nth-child(2) .sns {
    color: #b0e0e6;
    border-bottom: 2px solid #b0e0e6;
}

.contact__text .text>div:nth-child(3) .sns {
    color: #e0115f;
    border-bottom: 2px solid #e0115f;
}

.contact__text .text>div:nth-child(4) .sns {
    color: #7638fa;
    border-bottom: 2px solid #7638fa;
}

.contact__text .text>div:nth-child(5) .sns {
    color: #8db600;
    border-bottom: 2px solid #8db600;
}

.contact__text .text a {
    font-size: 15px;
}
</style>