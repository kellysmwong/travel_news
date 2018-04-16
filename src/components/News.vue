<template>
  <div>
      <md-card v-for="news in newsList" :key="news.id">
          <md-card-header>
            <md-card-media>
              <img src="../assets/sample.jpg">
            </md-card-media>

            <md-card-header-text>
              <div class="md-title">{{news.title}}</div>
            </md-card-header-text>
          </md-card-header>

          <md-card-content>
            {{news.short_desc}}
          </md-card-content>

          <md-card-actions>
            <md-button :href="news.url" target="_blank">Detail</md-button>
          </md-card-actions>
      </md-card>
  </div>
</template>

<script>
export default {
  name: 'News',
  data () {
    return {
      newsList: [
{"id": "1", "title": "台中平民價手作冰品   多款自創芋圓粉圓粉粿", "short_desc": "台中有一間手作芋圓粉圓冰店默默打響名堂，「地芋添糖&包心粉圓專賣店」由一對夫妻經營，主打以安全簡單手作芋圓粉圓。店鋪售賣多款自創冰品，價格亦親民貼地，$40至$50台幣左右（約$11至$13港幣），每款冰品色彩豐富，夏天食更覺透心涼！", "tag": [], "post_date": "2018-04-11 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23500"},
{"id": "2", "title": "台灣7-11限定 宇治抹茶冰銅燒／藍莓馬卡龍", "short_desc": "美國雪糕店的COLD STONE Creamery在台灣一直受大家歡迎，更開了不少分店。除了門市大熱的雪糕商品外，近期還在台灣推出超人氣商品，「濃‧宇治抹茶冰銅燒」和「藍莓馬卡龍」，現在於台灣各大7-11和其他商店限量發售，吸引了不少人去掃貨。", "tag": [], "post_date": "2018-04-10 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23497"},
{"id": "3", "title": "森永抹茶牛奶糖雪糕批  台灣便利店有售", "short_desc": "在韓國開售以來就大受好評的抹茶雪糕批，現在在台灣的便利店都可以買。「森永抹茶牛奶糖雪糕三文治」超濃郁的抹茶雪糕，內餡再配上焦糖醬，味道特別，而且這個更是純海外限定，連日本都買不到的。", "tag": ["台灣", "便利店"], "post_date": "2018-04-13 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23495"},
{"id": "4", "title": "厚切牛肉山  首爾重量級燒牛丼飯 ", "short_desc": "在首爾麻浦區上水洞，有間近期大熱的牛丼飯飯堂「홍대개미」，每塊厚切牛片都是即燒，燒至六成熟，牛丼飯飯上的牛片堆得像座小山，還配有洋蔥片和埋藏了的芽菜，口感非常豐富，簡直是食肉獸的天堂。", "tag": [], "post_date": "2018-04-10 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23502"},
{"id": "5", "title": "日本西部發生6.1級地震 日氣象廳：未來一週注意強餘震", "short_desc": "遊日／居日人士注意！位於日本本州島的島根縣西部，於日本時間4月9日凌晨1時32分發生6.1級地震。島根縣及附近的居民均受影響。氣象廳表示，未來一週可能會有高達5級程度的餘震。請各位在日人士小心，尤其是地震後2～3日，做好預防措施，並且盡量避免前往該區。", "tag": ["日本", "島根", "地震"], "post_date": "2018-04-10 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23496"},
{"id": "6", "title": "名古屋城天守閣維修 四年半後再見！", "short_desc": "是次維修計劃預計需時4年半，將於2022年竣工。期間天守閣將關閉，禁止遊客進入。不過不代表我們完全看不到它，遊客還可以從天守閣的背面拍照留念。", "tag": ["日本", "觀光", "名古屋", "天守閣", "名古屋城"], "post_date": "2018-04-09 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23499"},
{"id": "7", "title": "XXL級海鮮宴 宿霧小島即場殺價現撈海鮮", "short_desc": "夏天快到，大家都想到水清沙幼的地方旅行，享受海天一色的景色。近年掀起到國外島嶼旅行的風氣，宿霧更是其中一個大家必去的藍色島嶼。宿霧周圍都有不同的小島，其中一個名為「資生堂島」，是陽光與海灘、水清沙幼的地方，除此之外，島上大大隻的生猛海鮮任你挑，可以即叫即食，還可以現場殺價搶購。", "tag": [], "post_date": "2018-04-13 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23503"},
{"id": "8", "title": "大阪環球影城5月新夜間巡遊 360度投影置身哈利波特、Minions電影場面", "short_desc": "環球影城又有新節目啦！由5月17日開始，環球影城將會推出全新夜間巡遊，採用「Projection Mapping」的浮空投影技術，於全長520米的巡遊路上投射出各種電影人物，360度圍繞大家，讓我們置身於電影場面之中，來一個前所未有的體驗！", "tag": ["日本", "大阪", "觀光", "USJ", "環球影城", "巡遊", "Harry Potter", "Minions", "Transformers", "侏羅紀公園", "玩樂"], "post_date": "2018-04-10 00:00:00", "url": "https://travel.ulifestyle.com.hk/news/detail/23501"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.md-card {
  width: 320px;
  margin: 4px;
  vertical-align: top;
  float: left;
}

.md-card-media {
  width: 100px;
  height: 100px;
  flex: 0 0 100px;
}
</style>
