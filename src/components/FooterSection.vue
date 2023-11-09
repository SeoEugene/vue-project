<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>Eugene's Web Portfolio</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div>
                        <div class="title">
                            <a href="#">Sign Up</a>
                        </div>
                        <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                    </div>
                    <div>
                        <div class="title">
                            <a href="#">GSAP</a>
                        </div>
                        <p class="desc">GSAP의 여러 효과를 볼 수 있습니다.</p>
                    </div>
                    <div>
                        <div class="title">
                            <a href="#">Animation</a>
                        </div>
                        <p class="desc">Animation 효과를 볼 수 있습니다.</p>
                    </div>

                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li>
                            <a href="https://webstoryboy.co.kr">
                                <img src="../assets/img/Mail.png" alt="메일">
                                <p>Mail</p>
                            </a>
                        </li>
                        <li>
                            <a href="https://github.com/SeoEugene/vite-project">
                                <img src="../assets/img/github.png" alt="깃허브">
                                <p>github</p>
                            </a>
                        </li>
                        <li>
                            <a href="https://webstoryboy.co.kr">
                                <img src="../assets/img/blog.png" alt="블로그">
                                <p>Blog</p>
                            </a>
                        </li>
                        <li>
                            <a href="https://webstoryboy.co.kr">
                                <img src="../assets/img/Instargram.png" alt="인스타그램">
                                <p>Instagram</p>
                            </a>
                        </li>
                        <li>
                            <a href="https://webstoryboy.co.kr">
                                <img src="../assets/img/kakao.png" alt="카카오톡">
                                <p>Kakao</p>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 Joy WEB<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
    <!-- //footer -->
</template>

<style lang="scss">
#footer {
    height: 100vh;
    background-color: #ffdddd;
}

.footer__inner {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1vw;
}

.footer__text {
    font-size: 9vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
    line-height: 0.88;
    letter-spacing: 0.1vw;
    z-index: 100;
    color: #1f1717;
    padding-bottom: 20px;
    border-bottom: 5px solid #1f1717;
}

.footer__info {
    display: flex;
    width: 100%;
    height: 650px;
}

.footer__info .left {
    margin: 10px;
    width: 50%;
    margin-top: 100px;
}

.footer__info .left .title {
    margin-left: 10px;
    font-size: 3vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
}

.footer__info .left .title:hover {
    color: #1f1717;
}

.footer__info .left .desc {
    margin-left: 10px;
    font-size: 18px;
}

.footer__info .right {
    margin: 10px;
    width: 50%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: 100px;
}

.footer__info .right ul {
    display: flex;
    flex-wrap: wrap;
}

.footer__info .right h3 {
    width: 100%;
    height: 80px;
    font-size: 3vw;
    text-transform: uppercase;
    font-weight: 400;
    font-family: 'Abril Fatface', serif;
}

.footer__info .right li {
    width: 130px;
    height: 130px;
    margin: 10px;
    display: block;
}

.footer__info .right li a {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;

}

.footer__info .right li img {
    width: 70%;
    height: 60%;
    margin: 0 auto;

}

.footer__info .right li p {
    width: 100%;
    height: 20%;
    text-align: center;
    line-height: 2;
    font-weight: 600;
}

.footer__right {
    width: 100%;
    text-align: center;
}

@media (max-width: 800px) {
    .footer__info .right li {
        width: 80px;
        height: 80px;
    }
}
</style>