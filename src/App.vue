<!-- src/App.vue -->
<template>
  <div class="cv-page">
    <MenuBar />
    <IntroSection />
    <ImageSection />
    <AboutMeSection />
    <Resume />
    <MainContent />
  </div>
</template>

<script lang="ts">
import MenuBar from './components/MenuBar.vue';
import IntroSection from './components/IntroSection.vue';
import ImageSection from './components/ImageSection.vue';
import AboutMeSection from './components/AboutMeSection.vue'; 
import Resume from './components/ResumeSection.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    MenuBar,
    IntroSection,
    ImageSection,
    AboutMeSection, 
    Resume,
    MainContent
  }
}
</script>

<style src="./assets/main.css"></style>
