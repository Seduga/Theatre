<template>
  <div>
    <button
      id="burger-button"
      v-if="!isContainerVisible"
      @click="getContainerVisible()"
    >
      ≡
    </button>
    <div id="container" v-else>
      <button id="close-button" @click="getContainerVisible()">×</button>
      <div class="navigation">
        <button class="btn">ГЛАВНАЯ</button>
        <button class="btn">О ТЕАТРЕ</button>
        <button class="btn">НАШИ ПОСТАНОВКИ</button>
        <button class="btn">ПАРТНЕРЫ ТЕАТРА</button>
        <button class="btn">КОНТАКТЫ</button>
      </div>
      <a id="facebook">
        <img src="@/assets/Facebook.png" alt="Facebook" />
      </a>
      <a id="insta">
        <img src="@/assets/instagram.png" alt="Instagram" />
      </a>
      <a id="yt">
        <img src="@/assets/Yt.png" alt="YouTube" />
      </a>
      <a id="vk">
        <img src="@/assets/Vk.png" alt="Vk" />
      </a>
    </div>
  </div>
</template>
<script>
export default {
  name: 'mobileInterface',
  data() {
    return {
      isContainerVisible: false,
      screenHeight: 0,
      smallPicVisible: false,
    };
  },
  // Метод для отображение навигации
  methods: {
    getContainerVisible() {
      this.isContainerVisible = !this.isContainerVisible;
    },
  },
};
</script>
<style scoped>
/* Стили для блоков */
#container {
  z-index: 100;
  position: fixed;
  top: 0;
  height: 120vh;
  min-height: 1045px;
  width: 300px;
  font-family: "Open Sans";
  font-weight: 700;
  font-style: bold;
  background-color: rgb(32, 32, 32);
  display: flex;
  flex-direction: column;
  overflow-y: scroll;
}
.navigation {
  position: relative;
  top: 280px;
  left: 15px;
  white-space: nowrap;
  display: flex;
  flex-direction: column;
  text-align: left;
}

/* ....................................................................... */

/* Стили для кнопок */

#close-button {
  border: 0;
  background: local;
  position: absolute;
  right: 20px;
  top: 18px;
  color: white;
  margin-top: 38px;
  font-size: 4em;
}
.btn {
  background: local;
  border: 0;
  font-family: "Open Sans";
  font-size: 24px;
  color: white;
  margin-top: 35px;
  margin-right: 37px;
  text-align: left;
  height: 33px;
}
#facebook {
  position: absolute;
  right: 220px;
  top: 734px;
}
#insta {
  position: absolute;
  right: 80px;
  top: 740px;
}
#yt {
  position: absolute;
  right: 210px;
  top: 880px;
}
#vk {
  position: absolute;
  right: 80px;
  top: 880px;
}
#burger-button {
  position: fixed;
  left: 10%;
  top: 5%;
  border: 0;
  background: local;
  align-items: center;
  font-size: 4em;
  color: white;
}
/* ....................................................................... */

@media(max-height : 925px){
  .navigation{
   top: 80px;
  }
  #facebook{
    top: 540px;
  }
  #insta{
    top: 690px;
  }
  #yt{
    top: 700px;
  }
  #vk{
    top: 550px;
  }
}
</style>
