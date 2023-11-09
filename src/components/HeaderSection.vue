<script setup>
import { headerNav } from "@/constants/index"
</script>

<template>
    <header id="header" role="banner">
        <div class="header__inner">
            <div class="header__logo">
                <a href="#">portfolio<em>developer</em></a>
            </div>
            <nav class="header__nav" role="navigation" area-label="메인 메뉴" :class="{ show: isNavVisible }">
                <ul>
                    <li v-for="(nav, key) in headerNav" :key="key">
                        <a :href="nav.url" @click="scrollLink($event)">{{ nav.title }}</a>
                    </li>
                </ul>
            </nav>
            <div class="header__nav__mobile" id="headerToggle" aria-controls="primary" role="button"
                :aria-expanded="isNavVisible.toString()" @click="toggleMobileMenu">
                <span></span>
            </div>
        </div>
    </header>
    <!-- //header -->
</template>

<script>
export default {
    data() {
        return {
            isNavVisible: false,
        };
    },
    methods: {
        toggleMobileMenu() {
            this.isNavVisible = !this.isNavVisible;
        },
        scrollLink(event) {
            event.preventDefault();

            const targetId = event.target.getAttribute("href");
            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                targetElement.scrollIntoView({ behavior: "smooth" });
            }
        },
    },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Questrial&display=swap');

#header {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    z-index: 10000;
    background-color: rgb(128, 128, 128);
    font-family: 'Questrial', sans-serif;
    color: #2b3642;
    font-size: 1.7rem;
}

.header__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem;
}

.header__inner:hover {
    background-color: #fff;
}

.header__logo {}

.header__logo a:hover {
    color: #2b3642;
}

.header__nav {}

.header__nav li {
    display: inline;
}

.header__nav li a {
    display: inline-block;
    padding: 0.3rem 1rem;
    font-weight: 300;
    position: relative;
}

.header__nav li a::before {
    content: '';
    width: calc(100% - 30px);
    height: 1px;
    background-color: rgba(246, 255, 253, 1);
    position: absolute;
    left: 15px;
    bottom: 5px;
    transform: scaleX(0);
    transition: all 0.3s;
}

.header__nav li a:hover::before {
    transform: scaleX(1);
    color: #92d4c0;
}

.header__nav li a:hover {
    color: #92d4c0;
}

.header__nav__mobile {
    width: 40px;
    height: 40px;
    cursor: pointer;
    display: none;
}

.header__nav__mobile span {
    display: block;
    width: 40px;
    height: 2px;
    background-color: #92d4c0;
    margin-top: 19px;
    position: relative;
}

.header__nav__mobile span::before {
    content: '';
    width: 40px;
    height: 2px;
    background-color: #92d4c0;
    position: absolute;
    right: 0;
    top: 6px;
    transition: width 0.3s;
}

.header__nav__mobile span::after {
    content: '';
    width: 40px;
    height: 2px;
    background-color: #92d4c0;
    position: absolute;
    left: 0;
    bottom: 6px;
    transition: width 0.3s;
}

@media (max-width: 800px) {
    .header__nav {
        display: none;
    }

    .header__nav.show {
        display: block;
    }

    .header__nav.show ul {
        display: block;
        position: absolute;
        top: 68px;
        right: 0;
        background-color: rgba(246, 255, 253, 0.6);
        z-index: 10000;
        min-width: 159px;
        padding: 20px 0;
    }

    .header__nav.show li {
        display: block;
        text-align: right;
    }

    .header__nav.show li a {
        display: inline-block;
        padding: 10px;
    }

    .header__nav.show+.header__nav__mobile span::before {
        width: 20px;
    }

    .header__nav.show+.header__nav__mobile span::after {
        width: 20px;
    }

    .header__nav__mobile {
        display: block;
    }
}
</style>