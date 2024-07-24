<template>
  <v-app id="app">
    <v-main>
      <v-container id="wrapper">
        <h1>Kono's Portfolio</h1>
        <profile-section />
        <skills-section />
        <works-section />
        <contact-section />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import ProfileSection from './components/ProfileSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import WorksSection from './components/WorksSection.vue'
import ContactSection from './components/ContactSection.vue'

export default {
  name: 'App',
  components: {
    ProfileSection,
    SkillsSection,
    WorksSection,
    ContactSection
  }
}
</script>

<style>
@import '~vuetify/dist/vuetify.min.css';
#app {
  /* 背景色の設定 */
  background-color: #f0f0f0;
  /* 背景画像の設定 */
  background-image: url('/public/background.png'); /* 公開フォルダのパスも可 */
  background-size: cover;
  background-position: center;
  min-height: 100vh;
}

h1 {
  color: #f0f0f0;
  text-align: center;
}

#wrapper{
  padding-top: 50px;
}
</style>
