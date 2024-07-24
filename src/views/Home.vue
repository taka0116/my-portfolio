<template>
  <v-container>
    <Profile />
    <Skills />
    <Works />
    <Contact />
  </v-container>
</template>

<script>
import Profile from '@/components/Profile.vue';
import Skills from '@/components/Skills.vue';
import Works from '@/components/Works.vue';
import Contact from '@/components/Contact.vue';

export default {
  name: 'Home',
  components: {
    Profile,
    Skills,
    Works,
    Contact
  }
}
</script>

<style scoped>
/* カスタムスタイルをここに追加 */
</style>
