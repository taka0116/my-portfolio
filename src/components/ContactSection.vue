<template>
  <v-container id="contact-section">
    <v-row>
      <v-col>
        <h3>お問い合わせ</h3>
        <v-text-field label="n62.kono.takayuki@gmail.comにメールを送信する" v-model="email"></v-text-field>
        <v-btn @click="sendEmail">送信</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      email: ''
    }
  },
  methods: {
    sendEmail() {
      window.location.href = `mailto:your-email@example.com?subject=Portfolio Contact&body=From: ${this.email}`;
    }
  }
}
</script>

<style scoped>
#contact-section {
  color: aliceblue;
}
</style>
