<template>
  <div class="container">
    <nav>
      <a
        @click="emitScrollToContent('content1')"
        class="nav"
        @mouseenter="setActiveElem(1)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 1 }"
        >ГЛАВНАЯ</a
      >

      <a
        @click="emitScrollToContent('content2')"
        class="nav"
        @mouseenter="setActiveElem(2)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 2 }"
        >О ТЕАТРЕ</a
      >
      <a
      @click="emitScrollToContent('content3')"
        class="nav"
        @mouseenter="setActiveElem(3)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 3 }"
        >НАШИ ПОСТАНОВКИ</a
      >
      <a
        class="nav"
        @mouseenter="setActiveElem(4)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 4 }"
        >ПАРТНЕРЫ ТЕАТРА</a
      >
      <a
        class="nav"
        @mouseenter="setActiveElem(5)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 5 }"
        >КОНТАКТЫ</a
      >

      <a
        id="phone"
        @mouseenter="setActiveElem(6)"
        @mouseleave="setActiveElem(0)"
        :class="{ 'hover-btn': activeElem === 6 }"
        >+7 (---) (---) (--) (--)</a
      >
    </nav>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeElem: 0,
    };
  },
  components: {},
  methods: {
    setActiveElem(id) {
      this.activeElem = id;
    },
    emitScrollToContent(contentId) {
      this.$emit("scrollToContent", contentId);
    },
  },
};
</script>
<style scoped>
/* Общие стили для блока с навигацией */
.container {
  font-family: "Open Sans";
  font-weight: 700;
  line-height: 25px;
  border: 0;
  color: white;
  white-space: nowrap;
  background: local;
  position: fixed;
  display: flex;
  width: 90%;
  left: 10%;
  height: 15%;
  align-items: center;
}
nav {
  margin: 0 auto;
}

/* ....................................................................... */




/* Кнопки навигации */
.nav {
  line-height: 25px;
  margin-left: 63px;
  font-size: 18px;
  margin-top: 2%;
}
#phone {
  margin-top: 2%;
  margin-left: 10%;
  text-align: left;
  font-size: 18px;
}


/* ....................................................................... */



/* Эффекты */
.hover-btn {
  transition: all 0.5s;
  text-decoration: underline 2px goldenrod;
}
/* Для больших мониторов */
@media (min-width: 1650px) {
}



/* ....................................................................... */






/* Небольшие мониторы и ноутбуки */
@media (max-width: 1650px) {
  .nav {
    margin-left: 30px;
  }
}


/* ....................................................................... */


/* Ноутбуки и маленькие мониторы */
@media (max-width: 1400px) {
  .container {
    max-width: 900px;
    /* max-height: 300px; */
  }
  .nav {
    margin-left: 30px;
    font-size: 16px;
  }
}

/* ....................................................................... */


/* отключение навигации для компьютеров и перемещение номера телефона */
@media (max-width: 1110px) {
  .nav {
    display: none;
  }
  #phone {
    font-size: 22px;
    position: flex;
    margin-top: 5%;
    margin-left: 90%;
  }
}
/* ....................................................................... */
</style>
