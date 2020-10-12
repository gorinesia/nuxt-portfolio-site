<template>
  <div id="profile">
    <v-container fluid>
      <v-card width="100vw">
        <v-card-title class="pa-5 justify-center display-1 font-italic">
          Profile
        </v-card-title>

        <v-row justify="center" align-content="center">
          <v-col cols="12" sm="5" md="5" align="center">
            <!-- justify: space-around横均等配置, align-content: center上下中央配置 -->
            <v-row justify="space-around" align-content="center" style="height:100%">
              <!-- v-avatar:アバター表示  -->
              <v-avatar width="80%" height="auto">
                <!-- objet-fit:cover 画像中央トリミング表示。static/imageに配置した画像を参照  -->
                <img src="/image/myPhoto.jpg" alt="AKI" style="object-fit: cover;">
              </v-avatar>
            </v-row>
          </v-col>
          <!-- レスポンシブ（スマホ(cols)：横いっぱい表示(MAX:12), PC・タブレット(sm,md):6/12） -->
          <v-col cols="12" sm="6" md="6">
            <!-- v-list:リスト表示、v-forでdataのobject(profiles)数分要素繰り返し描画  -->
            <v-list>
              <v-list-item v-for="profile in profiles" :key="profile.content">
                <v-list-item-content>
                  <!-- profileの中身（content）を表示。<v-icon>mdi-check</v-icon>でチェックアイコン表示  -->
                  <v-list-item-title><v-icon>mdi-check</v-icon> {{ profile.content }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    profiles: [
      { content: 'AKINORI SAKAKIBARA (さかきばら あきのり) ' },
      { content: '1989年愛知県生まれ' },
      { content: '旅人からWeb系エンジニア' },
      { content: 'プログラミングとブログ継続中' },
      { content: '旅とスノーボード狂' },
      { content: '妻と話すのが毎日の幸せ' },
      { content: 'バックパッカー歴5年' },
      { content: '真面目、誠実、行動力強め' },
      { content: 'やると決めたことには全力' },
      { content: '協調性もちつつ、人を引っ張る' },
      { content: '英語も勉強中' },
      { content: '現在無職' }
    ]
  })
}
</script>

<style>

</style>
