<template>
  <v-container class="works-section">
    <v-row>
      <v-col cols="12">
        <h3>Works</h3>
      </v-col>
      <v-col class="work-card" style="white-space: pre-wrap;" v-for="work in works" :key="work.name" cols="12" md="4">
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
          description: 'Rails App./投資トレードログアプリ\n・株式などの投資損益を投稿記録するアプリ。ユーザー機能で今週・今月などの期間損益表示、月間ランキング機能でユーザー同士が１位を競争。 ',
          link: 'https://tradelog-cmso.onrender.com'
        },
        {
          name: 'RecipeGacha',
          thumbnail: '/thumbnail/recipegacha-thumbnail.png',  
          description: 'React App/料理レシピ提案アプリ\n・料理のカテゴリを選択しボタンを押下するとレシピが出るアプリ。楽天レシピと連動しており、所要時間・予算も表示。',
          link: 'https://recipegacha.netlify.app'
        },
        {
          name: 'RicinseQuiz',
          thumbnail: '/thumbnail/licensequiz-thumbnail.png',  
          description: 'Vue App/資格試験クイズアプリ\n・興味のある資格試験クイズを選んで１０問チャレンジ。実用的な資格から趣向的な資格まで楽しみながら学べます。',
          link: 'https://ricense-quiz.netlify.app'
        },
        {
          name: 'TracaKanteidan',
          thumbnail: '/thumbnail/tracakanteidan-thumbnail.png',  
          description: 'WordPress Site/トレカ相場情報サイト\n・遊戯王などの高価格帯のトレカ相場をランキング形式で投稿更新されるサイト。遊戯王。ポケカ・ワンピ・DBの４種をラインナップ。',
          link: 'https://yugioh-kanteidan.com'
        },
        {
          name: 'FXQuest',
          thumbnail: '/thumbnail/fxquest-thumbnail.png',  
          description: 'WordPress Site/FXトレード情報サイト\n・FXトレーダーの為の攻略情報サイト。毎日の戦略情報投稿や毎週のトレード収支や手法など勝率アップにつながる内容が盛り沢山。',
          link: 'https://fxquest-strategy.com'
        },
        {
          name: 'Gokuraku',
          thumbnail: '/thumbnail/gokuraku-thumbnail.png',  
          description: 'Wix Site/リラクゼーションサロンサイト\n・仮想リラクゼーションサロンの予約サイト。セラピスト紹介やコースメニュー料金など、多方面のサービスに流用可能なサイト。',
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
