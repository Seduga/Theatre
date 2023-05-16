<template>
  <div class="container">
    <div class="text">КОНТАКТНАЯ ИНФОРМАЦИЯ</div>
    <div class="line"><img src="@/assets/Line 2.png" alt="" /></div>

    <a class="link">
      <img src="@/assets/instagram--active.png" alt="instagram" />
    </a>
    <a class="link"><img src="@/assets/fbsmall.png" alt="facebook" /></a>
    <a class="link"><img src="@/assets/vksmall.png" alt="vk" /></a>
    <a class="link"><img src="@/assets/Ytsmall.png" alt="YouTube" /></a>
  </div>
</template>
<script>
export default {
  name: "sideBar",
  data() {
    return {};
  },
};
</script>
<style scoped>
/* Стили для блоков */
.container {
  position: fixed;
  top: 0;
  height: 100vh;
  min-height: 1045px;
  width: 150px;
  font-family: "Open Sans";
  font-weight: 700;
  font-style: bold;
  background-color: rgba(51, 51, 51, 0.75);
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* ....................................................................... */

/* Стили для внутренностей блока */
.text {
  margin: 0 auto;
  color: white;
  writing-mode: vertical-rl;
  margin-top: 400px;
  transform: rotate(180deg);
}
.link {
  border: 0;
  background: local;
  padding: 30px;
}
.line {
  height: 50px;
  margin-bottom: 20px;
  margin-top: 40px;
}

/* ....................................................................... */

/* Медиа запросы */

/* Небольшие ноутбуки и большие планшеты */
@media (max-height: 1250px) {
  .text {
    /* margin-top: 250px; */
  }
  .link {
    padding: 30px;
  }
  .line {
    margin-bottom: 20px;
    margin-top: 30px;
  }
}
@media (max-height: 1125px) {
  .text {
    margin-top: 180px;
  }
}
/* Мобильные устройства */
@media (max-width: 1025px) {
  .container {
    display: none;
  }
}
</style>
