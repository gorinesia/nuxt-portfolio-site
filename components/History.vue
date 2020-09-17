<template>
  <div id="history">
    <v-container fluid>
      <v-card
        width="100vw"
        class="pa-4"
      >
        <v-card-title
          class="justify-center display-1 font-italic"
        >
          History
        </v-card-title>

        <!-- タイムラインコンポーネント -->
        <v-timeline>
          <!-- タイムラインアイテム（経歴項目）、v-for:data(years)の要素分項目繰り返し、small:中央のDotのサイズを小さく -->
          <v-timeline-item
            v-for="(year, i) in years"
            :key="i"
            :color="year.color"
            small
          >
            <!-- タイムラインの項目の方向を反転(opposite)、年数(year.year)とその色(year.color)を指定 -->
            <template v-slot:opposite>
              <span :class="`title font-weight-bold ${year.color}--text`" v-text="year.year"></span>
            </template>
            <!-- 項目のタイトル（year.title）テキスト(year.content)を指定 -->
            <div class="py-4">
              <h2 :class="`title font-italic mb-4 ${year.color}--text`">{{ year.title }}</h2>
              <div>
                {{ year.content }}
              </div>
            </div>
          </v-timeline-item>
        </v-timeline>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    // 経歴の項目データ
    years: [
      {
        color: 'cyan',
        year: '2008~12',
        title: '愛知学院大学',
        content: '柔道部。3年の秋に退部。'
      },
      {
        color: 'green',
        year: '2012~13',
        title: '世界一周',
        content: '自由を求めて世界一周一年間の旅へ。'
      },
      {
        color: 'pink',
        year: '2015~17',
        title: 'アフリカ旅',
        content: 'アフリカ大陸縦断。妻となる奈々と出会う。'
      },
      {
        color: 'amber',
        year: '2018/11/07',
        title: '結婚',
        content: '一生一緒に旅をする生涯の伴侶が出来る。'
      },
      {
        color: 'orange',
        year: '2020/04~',
        title: 'プログラミング学習',
        content: 'これからの人生のことを考え、プログラマーになることを決意。'
      }
    ]
  })
}
</script>
<style>
</style>
