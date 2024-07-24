<template>
  <v-container id="profile-section">
    <v-row>
      <v-col>
        <v-avatar size="100">
          <img src="/profile.png" alt="Profile Image" class="profile-img">
        </v-avatar>
        <h2>Takayuki Kono</h2>
        <p>投資系Webマーケターの河野貴幸です。</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ProfileSection'
}
</script>

<style scoped>
#profile-section {
  text-align: center;
  margin-top: 100px;
}

.profile-section {
  text-align: center;
}

.profile-img {
  width: 150px;
  height: auto;
  border-radius: 50%;
}

h2,p {
  color: aliceblue;
}
</style>
