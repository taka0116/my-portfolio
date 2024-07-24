<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <h3>Skills</h3>
      </v-col>
      <v-col v-for="(skill, index) in skills" :key="index" cols="12" md="4">
        <v-card>
          <v-card-title>{{ skill.name }}</v-card-title>
          <v-card-subtitle>{{ skill.description }}</v-card-subtitle>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'SkillsSection',
  data() {
    return {
      skills: [
        { name: 'Rails', description: 'Ruby,Javascript,HTML,CSS' },
        { name: 'React', description: 'Javascript,HTML,CSS' },
        { name: 'Vue', description: 'Javascript,HTML,CSS' },
        { name: 'WordPress', description: 'PHP,HTML,CSS' }
      
      ]
    }
  }
}
</script>

<style scoped>
h3 {
  color: aliceblue;
}
</style>
