<template>
  <div id="page">
    <h1 id="title">
      <span :style="{ color: textColor }">НАШИ</span> ПОСТАНОВКИ
    </h1>
    <div id="content">
      <div id="subcontent">
        <div id="first" class="pic">
          <h1 class="top">ОСКАР 2020</h1>
          <p class="side">СЕНТЯБРЬ 2020</p>
        </div>

        <div id="second" class="pic">
          <button id="search">
            <span id="search-icon"><i class="fas fa-search"></i></span>
          </button>
        </div>

        <div id="third" class="pic">
          <h1 class="top">ЗОЛОТОЙ ГРОМОФОН</h1>
          <span class="side">ИЮЛЬ 2020</span>
        </div>

        <div id="fourth" class="pic">
          <h1 class="top">ЩЕЛКУНЧИК</h1>
          <span class="side">МАЙ 2020</span>
        </div>
      </div>
      <div id="reviews">
        <div>
          <h1 class="years">2018</h1>
          <h1 class="years">2019</h1>
          <h1 class="years">2020</h1>
        </div>
        <ul>
          <li v-for="star in stars" :key="star">
            <span class="star">&#x2605;</span>
          </li>
        </ul>
        <p>Лучший театр <br />по мнению театральных <br />критиков Парижа</p>
      </div>
    </div>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css"
    />
  </div>
</template>
<script>
export default {
  name: "pageContent",
  data() {
    return {
      textColor: "goldenrod",
      images: [
        { src: require("@/assets/firstSlide.png") },
        { src: require("@/assets/secondSlide.png") },
        { src: require("@/assets/thirdSlide.png") },
        { src: require("@/assets/fourthSlide.png") },
      ],
      stars: Array(5).fill(null),
    };
  },
  methods: {},
};
</script>
<style scoped>
/* Блоки с контентом */
#page {
  padding: 20px;
  margin-top: 0;
  color: white;
  font-family: "Open Sans";
  font-weight: 700;
}
#content {
  padding: 0;
  margin-left: 12%;
}
#subcontent {
  margin-top: 100px;
  padding: 0;
  overflow: hidden;
  display: flex;
  max-width: 1920px;
}
#reviews {
  position: relative;
  margin: 0 auto;
  margin-top: 150px;
  background-image: url(@/assets/bottomSlide.png);
  background: cover no-repeat;
  width: 1100px;
  height: 550px;
}
#reviews > div {
  display: list-item;
  list-style-type: none;
  width: 198px;
  position: absolute;
  left: 190px;
  top: 110px;
  color: goldenrod;
  font-size: 26px;
}
#first,
#second,
#third,
#fourth {
  display: flex;
  flex-direction: column;
  height: 550px;
  min-width: 420px;
}
#first {
  background-image: url(@/assets/firstSlide.png);
}
#second {
  background-image: url(@/assets/secondSlide.png);
}
#third {
  background-image: url(@/assets/thirdSlide.png);
}
#fourth {
  background-image: url(@/assets/fourthSlide.png);
}

/* ............................................. */

/* Стили для внутренностей блоков */
#reviews > ul {
  position: absolute;
  top: 171px;
  left: 410px;
  list-style-type: none;
  display: flex;
}
#reviews > ul > li {
  font-size: 30px;
  margin-left: 25px;
  color: goldenrod;
}
#reviews > p {
  position: absolute;
  top: 220px;
  left: 475px;
  font-size: 24px;
  line-height: 52px;
}
.side {
  transform: rotate(270deg);
  transform-origin: left;
  z-index: 1;
  font-size: 18px;
  height: max-content;
  width: max-content;
  white-space: nowrap;
  margin-left: 40px;
  margin-top: 400px;
}
.top {
  width: max-content;
  height: max-content;
  font-size: 24px;
  margin-top: 20px;
  margin-left: 40px;
}
#search {
  margin: 0 auto;
  margin-top: 225px;
  height: 100px;
  width: 100px;
  border-radius: 50%;
  background-color: goldenrod;
  border: 0;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3),
    -2px -2px 5px rgba(255, 255, 255, 0.3);
}
#search-icon {
  color: white;
  font-size: 30px;
}
#title {
  text-align: center;
  margin: 0 auto;
  font-weight: 300;
  margin-top: -10%;
}
/* ................................... */

/* Медиа-запросы */
@media (max-width: 1300px) {
  #reviews {
    margin-left: -18%;
    width: 100vw;
  }
}
</style>
