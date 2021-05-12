
<template>
  <div class="registration-container">
    <Nav/>
    <div class="intro-container">
      <div class="title">Hello,</div>
      <p class="intro">這是一個校園心理健康服務的平台，
      在這裡你可以體驗到......</p>
      <div class="pic" id="p1"></div>
      <div class="pic" id="p2"></div>
      <div class="pic" id="p3"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Homepage",
  data() {
    return {
      region: "南部",
      city: "台南市",
      township: "東區",
      roomtype: "整層住家",
      cost: "3千-5千",
      Country: [
        { region: "北部", city: "台北市" },
        { region: "北部", city: "新北市" },
        { region: "北部", city: "基隆市" },
        { region: "北部", city: "桃園市" },
        { region: "北部", city: "新竹市" },
        { region: "北部", city: "新竹縣" },
        { region: "中部", city: "苗栗縣" },
        { region: "中部", city: "台中市" },
        { region: "中部", city: "彰化縣" },
        { region: "中部", city: "南投縣" },
        { region: "中部", city: "雲林縣" },
        { region: "南部", city: "嘉義市" },
        { region: "南部", city: "嘉義縣" },
        { region: "南部", city: "台南市" },
        { region: "南部", city: "高雄市" },
        { region: "南部", city: "屏東縣" },
        { region: "東部", city: "宜蘭縣" },
        { region: "東部", city: "花蓮縣" },
        { region: "東部", city: "臺東縣" },
        { region: "離島", city: "澎湖縣" },
        { region: "離島", city: "金門連江" },
      ],
      District: [
        { city: "台北市", township: "中山區" },
        { city: "台北市", township: "中正區" },
        { city: "台北市", township: "信義區" },
        { city: "台北市", township: "士林區" },
        { city: "台北市", township: "大同區" },
        { city: "台北市", township: "大安區" },
        { city: "台北市", township: "內湖區" },
        { city: "台北市", township: "文山區" },
        { city: "台北市", township: "北投區" },
        { city: "台北市", township: "松山區" },
        { city: "台北市", township: "南港區" },
        { city: "台北市", township: "萬華區" },

        { city: "桃園市", township: "桃園市" },
        { city: "桃園市", township: "八德區" },
        { city: "桃園市", township: "楊梅區" },
        { city: "桃園市", township: "龍潭區" },
        { city: "桃園市", township: "復興區" },
        { city: "桃園市", township: "大溪區" },
        { city: "桃園市", township: "平鎮區" },
        { city: "桃園市", township: "中壢區" },
        { city: "桃園市", township: "觀音區" },
        { city: "桃園市", township: "大園區" },
        { city: "桃園市", township: "蘆竹區" },
        { city: "桃園市", township: "龜山區" },
        { city: "桃園市", township: "新屋區" },

        { city: "台中市", township: "北屯區" },
        { city: "台中市", township: "東區" },
        { city: "台中市", township: "太平區" },
        { city: "台中市", township: "西屯區" },
        { city: "台中市", township: "大里區" },
        { city: "台中市", township: "潭子區" },
        { city: "台中市", township: "北區" },
        { city: "台中市", township: "中區" },
        { city: "台中市", township: "烏日區" },
        { city: "台中市", township: "南屯區" },
        { city: "台中市", township: "西區" },
        { city: "台中市", township: "沙鹿區" },
        { city: "台中市", township: "南區" },
        { city: "台中市", township: "龍井區" },
        { city: "台中市", township: "豐原區" },
        { city: "台中市", township: "大雅區" },
        { city: "台中市", township: "霧峰區" },
        { city: "台中市", township: "大肚區" },
        { city: "台中市", township: "梧棲區" },
        { city: "台中市", township: "清水區" },
        { city: "台中市", township: "大安區" },
        { city: "台中市", township: "后里區" },
        { city: "台中市", township: "石岡區" },
        { city: "台中市", township: "東勢區" },
        { city: "台中市", township: "和平區" },
        { city: "台中市", township: "新社區" },
        { city: "台中市", township: "神岡區" },
        { city: "台中市", township: "大甲區" },
        { city: "台中市", township: "外埔區" },

        { city: "台南市", township: "永康區" },
        { city: "台南市", township: "東區" },
        { city: "台南市", township: "中西區" },
        { city: "台南市", township: "北區" },
        { city: "台南市", township: "南區" },
        { city: "台南市", township: "安南區" },
        { city: "台南市", township: "善化區" },
        { city: "台南市", township: "新市區" },
        { city: "台南市", township: "安平區" },
        { city: "台南市", township: "新化區" },
        { city: "台南市", township: "麻豆區" },
        { city: "台南市", township: "西港區" },
        { city: "台南市", township: "山上區" },
        { city: "台南市", township: "安定區" },
        { city: "台南市", township: "歸仁區" },
        { city: "台南市", township: "左鎮區" },
        { city: "台南市", township: "玉井區" },
        { city: "台南市", township: "楠西區" },
        { city: "台南市", township: "南化區" },
        { city: "台南市", township: "仁德區" },
        { city: "台南市", township: "關廟區" },
        { city: "台南市", township: "龍崎區" },
        { city: "台南市", township: "官田區" },
        { city: "台南市", township: "佳里區" },
        { city: "台南市", township: "七股區" },
        { city: "台南市", township: "將軍區" },
        { city: "台南市", township: "學甲區" },
        { city: "台南市", township: "北門區" },
        { city: "台南市", township: "新營區" },
        { city: "台南市", township: "後壁區" },
        { city: "台南市", township: "白河區" },
        { city: "台南市", township: "東山區" },
        { city: "台南市", township: "六甲區" },
        { city: "台南市", township: "下營區" },
        { city: "台南市", township: "柳營區" },
        { city: "台南市", township: "鹽水區" },
        { city: "台南市", township: "大內區" },
      ],
    };
  },
  methods: {
    clickRegion: function () {
      this.city = " ";
      this.township = "";
      this.roomtype = "";
      this.cost = "";
    },
    clickCity: function () {
      this.township = "";
      this.roomtype = "";
      this.cost = "";
    },
    zeroCost: function () {
      this.cost = "";
    },
    logout() {
      this.$store.commit("setUserInfo", "", "");
      this.$router.push("/");
    },
    writeHabit() {
      this.$router.push("/LivingHabit");
    },
  },
};
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.homepage {
  border: 0;
  padding: 0;
  margin: 0;
  width: 100vw;
  height: 100vh;
  font-size: 10px;
  overflow-x: hidden;
  font-family: Noto Sans CJK TC;
  #navigation {
    width: 100vw;
    min-height: 7.5vh;
    max-height: 40vh;
    font-size: 1rem;
  }

  #condition {
    width: 100vw;
    min-height: 7.5vh;
    display: flex;
    flex-direction: row;
    font-size: 1rem;
  }

  .selected-condition {
    width: 75vw;
    position: relative;
    top: 3vh;
    left: 12.5vw;
    font-size: 1.5rem;
    display: flex;
    flex-direction: row;
    align-content: space-between;
    align-items: center;
  }
  .badge {
    margin-right: 2vw;
  }
}

#container {
  width: 75vw;
  position: relative;
  left: 12.5vw;
  top: 5vh;
  height: 75vh;
  display: flex;
  flex-direction: row;
  background-color: #cbb2a1;
  z-index: 10;
  font-family: Noto Sans CJK TC;
}
</style>
