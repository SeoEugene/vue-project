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
