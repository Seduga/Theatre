<template>
  <div class="container">
    <div class="text-container">
      <h1 class="title">БОЛЬШОЙ ТЕАТР</h1>
      <span class="text"> {{ text }}</span>
      <button
        id="btn"
        @mouseenter="hoverBtn = true"
        @mouseleave="hoverBtn = false"
        :class="{ 'hover-button': hoverBtn }"
      >
        АФИША
      </button>
    </div>
    <div class="poster">
      <img class="poster-image" src="@/assets/slider-container.png" alt="" />
      <div class="btns">
        <button
          class="arrow-btn1"
          @mouseenter="setActiveElem(1)"
          @mouseleave="setActiveElem(0)"
          :class="{ 'hover-btn2': activeElem === 1 }"
        >
          ←
        </button>
        <button
          class="btn-prev"
          @mouseenter="setActiveElem(2)"
          @mouseleave="setActiveElem(0)"
          :class="{ 'hover-btn2': activeElem === 2 }"
        >
          Пред
        </button>

        <button
          class="btn-next"
          @mouseenter="setActiveElem(3)"
          @mouseleave="setActiveElem(0)"
          :class="{ 'hover-btn2': activeElem === 3 }"
        >
          След
        </button>
        <button
          class="arrow-btn2"
          @mouseenter="setActiveElem(4)"
          @mouseleave="setActiveElem(0)"
          :class="{ 'hover-btn2': activeElem === 4 }"
        >
          →
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "mainContent",
  data() {
    return {
      text: "Большо́й теа́тр — петербургский театр, существовавший в 1784—1886 годах, с 1886 года — Петербургская консерватория. Первое постоянное в Санкт-Петербурге, крупнейшее в России и одно из крупнейших театральных зданий в Европе XVIII.",
      hoverBtn: false,
      activeElem: 0,
    };
  },
  methods: {
    setActiveElem(id) {
      this.activeElem = id;
    },
  },
};
</script>
<style scoped>
/* Стили для блоков */

.container {
  padding: 0;
  width: 800px;
  margin: 0 auto;
  font-family: "Open Sans";
  font-style: bold;
  font-size: 18px;
  color: white;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.poster {
  display: flex;
  flex-direction: column;
  margin-top: 35%;
}
.poster-image {
  height: 490px;
  width: 350px;
  display: flex;
  margin-left: 30%;
  margin-bottom: 10%;
}
.text-container {
  display: flex;
  width: 540px;
  flex-direction: column;
  margin-top: 35%;
}
.btns {
  position: relative;
  margin: 0 auto;
  height: 30px;
  width: 490px;
}
/* Стили для внутренностей блоков */

.text {
  display: flex;
  font-size: 16px;
}
button {
  font-size: 18px;
  font-family: "Open Sans";
  font-style: bold;
  color: #c4c4c4;
  border: 0;
  background: local;
}

.title {
  font-size: 64px;
  white-space: nowrap;
}
#btn {
  width: 160px;
  height: 50px;
  background-color: goldenrod;
  margin-top: 10%;
  text-align: center;
  font-family: "Open Sans";
  font-weight: 700;
  font-size: 18px;
}
/* Блок с кнопками ниже постера */
.btn-prev {
  position: absolute;
  top: 15%;
  left: 200px;
}
.btn-next {
  position: absolute;
  top: 15%;
  left: 360px;
}
.arrow-btn1 {
  font-size: 40px;
  position: absolute;
  left: 135px;
  top: -40%;
  background: local;
  border: 0;
  color: #c4c4c4;
}
.arrow-btn2 {
  font-size: 40px;
  color: #c4c4c4;
  position: absolute;
  left: 440px;
  top: -40%;
  background: local;
  border: 0;
}
/* Эффекты */
.hover-button {
  background-color: rgb(231, 185, 21);
  transition: all 1s;
  border: 1px solid black;
  color: black;
}
.hover-btn2 {
  transition: all 0.5s;
  color: #ffffff;
}
@media (max-width: 1400px) {
}
@media (max-width: 1300px) {
  .poster {
    display: none;
  }
  .container {
    margin-left: 20%;
  }
  .text-container {
    width: 100%;
  }
}
@media (max-width: 1000px) {
  .container {
    right: 10%;
    width: 80vw;
  }
  #btn {
    height: 50px;
    width: 160px;
    font-size: 22px;
  }
  .title {
    font-size: 64px;
    white-space: nowrap;
  }

  .text {
    font-size: 24px;
  }
}
</style>
