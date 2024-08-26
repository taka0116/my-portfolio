<template>
  <v-container class="works-section">
    <v-row>
      <v-col cols="12">
        <h3>Works</h3>
      </v-col>
      <v-col class="work-card" v-for="work in works" :key="work.name" cols="12" md="4">
        <img :src="work.thumbnail" :alt="work.name + ' Thumbnail'" class="work-thumbnail">
        <h3>{{ work.name }}</h3>
        <p>{{ work.description }}</p>
        <a :href="work.link" target="_blank">Visit</a>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'WorksSection',
  data() {
    return {
      works: [
        {
          name: 'TradeLog',
          thumbnail: '/thumbnail/tradelog-thumbnail.png',  
          description: 'Rails App./投資トレードログアプリ',
          link: 'https://tradelog-cmso.onrender.com'
        },
        {
          name: 'RecipeGacha',
          thumbnail: '/thumbnail/recipegacha-thumbnail.png',  
          description: 'React App/料理レシピ提案アプリ',
          link: 'https://recipegacha.netlify.app'
        },
        {
          name: 'RicinseQuiz',
          thumbnail: '/thumbnail/licensequiz-thumbnail.png',  
          description: 'Vue App/資格試験クイズアプリ',
          link: 'https://ricense-quiz.netlify.app'
        },
        {
          name: 'TracaKanteidan',
          thumbnail: '/thumbnail/tracakanteidan-thumbnail.png',  
          description: 'WordPress Site/トレカ相場情報サイト',
          link: 'https://yugioh-kanteidan.com'
        },
        {
          name: 'FXQuest',
          thumbnail: '/thumbnail/fxquest-thumbnail.png',  
          description: 'WordPress Site/FXトレード情報サイト',
          link: 'https://fxquest-strategy.com'
        },
        {
          name: 'Gokuraku',
          thumbnail: '/thumbnail/gokuraku-thumbnail.png',  
          description: 'Wix Site/リラクゼーションサロンサイト',
          link: 'https://taka0116ii.wixsite.com/my-site-8'
        }
        // 他のアプリケーション情報もここに追加
      ]
    }
  }
}
</script>

<style scoped>
.works-section {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

h3 {
  color: aliceblue;
}

.work-card {
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
  width: 300px;
  text-align: center;
}

.work-thumbnail {
  width: 300px;
  height: 300px;
  object-fit: cover;
  border-radius: 5px;
}

.work-card h3 {
  color: aliceblue;
  font-size: 1.2em;
  margin-top: 10px;
}

.work-card p {
  color: aliceblue;
  font-size: 1em;
  margin: 10px 0;
}

.work-card a {
  color: #007bff;
  text-decoration: none;
}

.work-card a:hover {
  text-decoration: underline;
}
</style>
