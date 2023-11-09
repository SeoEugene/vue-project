# vue를 이용한 포트폴리오 사이트 만들기
 Vue는 가볍고 유연한 구조를 가지고 있으며, 다른 라이브러리나 프레임워크와 쉽게 통합할 수 있습니다.
 1. 컴포넌트 기반 아키텍처: Vue는 컴포넌트라는 작은 조각들로 애플리케이션을 구성합니다. 각 컴포넌트는 자체 상태와 뷰를 가지며, 재사용 가능하며 관리하기 쉽습니다.

 2. 반응형 데이터 바인딩: Vue는 데이터와 뷰를 양방향으로 연결할 수 있습니다. 데이터가 변경되면 자동으로 화면이 업데이트됩니다. 이를 통해 개발자는 복잡한 DOM 조작을 최소화하고 코드를 간단하게 유지할 수 있습니다.

 3. 디렉티브: Vue는 HTML 요소에 특별한 속성을 추가하여 동적으로 요소를 조작하도록 지원합니다. 예를 들어, v-for, v-if, v-bind, v-on과 같은 디렉티브를 사용하여 템플릿과 데이터 간의 상호 작용을 제어할 수 있습니다.

 ex) * 골뱅이는 root를 뜻함
<script setup>
    import { headerNav } from "@/constants/index"
</script>
...
<li v-for="(nav, key) in headerNav" key="key">
    <a href="nav.url">{{ nav.title }}</a>
</li>

 4. 라우팅 및 상태 관리: Vue Router와 Vuex와 같은 공식 라이브러리를 사용하여 라우팅 및 상태 관리를 손쉽게 처리할 수 있습니다.

 5. 커뮤니티 및 에코시스템: Vue는 활발한 커뮤니티와 다양한 플러그인 및 라이브러리 생태계를 가지고 있어 개발자들이 다양한 기능을 확장하고 공유할 수 있습니다.

## vue 설치
`npm init vue@latest`
Ok to proceed? (y) y

Vue.js - The Progressive JavaScript Framework

√ Project name: ... vue-project
√ Add TypeScript? ... <span style="color:blue">No</span> / Yes
√ Add JSX Support? ... No / <span style="color:blue">Yes</span>
√ Add Vue Router for Single Page Application development? ... No / <span style="color:blue">Yes</span>
√ Add Pinia for state management? ... <span style="color:blue">No</span> / Yes
√ Add Vitest for Unit Testing? ... <span style="color:blue">No</span> / Yes
√ Add an End-to-End Testing Solution? » No
√ Add ESLint for code quality? ... No / <span style="color:blue">Yes</span>
√ Add Prettier for code formatting? ... No / <span style="color:blue">Yes</span>
`cd vue-project`
` npm install`
`npm run format   `

## vue 실행
` npm run dev `

## git 세팅
echo "# vue-project" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SeoEugene/vue-project.git
git push -u origin main

## git push
git add .
git commit -m "첫 커밋"
git push origin main

* 트러블 슈팅
<details>
<summary>Whitespace error</summary>
유닉스 시스템에서는 한 줄의 끝이 LF(Line Feed)로 이루어지는 반면,
윈도우에서는 줄 하나가 CR(Carriage Return)와 LF(Line Feed), 즉 CRLF로 이루어지는데
Git이 이 둘 중 어느 쪽을 선택할지 혼란해 생기는 오류

`git config --global core.autocrlf true // 시스템 전체에 적용`
`git config core.autocrlf true // 해당 프로젝트에만 적용`
이렇게 하게되면 개발자가 git에 코드를 추가했을 때는 CRLF를 LF로 변환해주고,
git의 코드를 개발자가 조회할 때는 LF를 CRLF로 변환해준다고 한다.
</details>

## install
gsap 설치 : `npm install gsap`
sass 설치 : `npm install sass`
lenis 설치 : `npm install @studio-freight/lenis`

## vue 파일구조
main.js -> App.vue -> HomeView.vue -> components의 뷰파일들

1. index.html
 <div id="app"></div>
  <script type="module" src="/src/main.js"><script>
2. src

 1) components (vue파일)

 2) router (js파일)

 3) views (vue파일)
    HomeView.vue
    <script setup>
        import SkipSection from '../components/SkipSection.vue';
        import HeaderSection from '../components/HeaderSection.vue';
        import IntoroSection from '../components/IntoroSection.vue';
        import SkillSection from '../components/SkillSection.vue';
        import SiteSection from '../components/SiteSection.vue';
        import PortSection from '../components/PortSection.vue';
        import ContactSection from '../components/ContactSection.vue';
        import FooterSection from '../components/FooterSection.vue';
    </script>

<template>
  <SkipSection />
  <HeaderSection />
  <main id="main" role="main">
    <IntoroSection />
    <SkillSection />
    <SiteSection />
    <PortSection />
    <ContactSection />
  </main>
  <FooterSection />
</template>

 4) App.vue
    <script setup>
        import { RouterView } from "vue-router"
    </script>
    <template>
        <RouterView />
    </template>

 5) main.js
    * 스타일도 여기에 import/ react는 확장자를 안써도 되지만 vue는 확장자까지 import할 때 필요하다!
    import "./assets/scss/style.scss"

    import { createApp } from 'vue'
    import App from './App.vue'
    import router from './router'

    const app = createApp(App)

    app.use(router)

    app.mount('#app')



## 배포
`npm run build`
`git add .`
`git commit -m "두번째 커밋"`
`git push origin main`
