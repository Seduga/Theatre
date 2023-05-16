<template>
  <div id="page">
    <h1 id="title">О ТЕАТРЕ</h1>
    <div id="content">
      <div id="block1" ref="content">
        <h4 class="subtitle">Самый лучший театр СПБ</h4>
        <p id="description">{{ text }}</p>
      </div>
      <div id="block2">
        <h4 class="subtitle">НЕМНОГО О ЦИФРАХ</h4>
        <img class="pic" src="@/assets/armchair 1.png" alt="armchair" />
        <span class="stat"><span class="gold">1600</span> посадочных мест</span>
        <img class="pic" src="@/assets/theater 1.png" alt="theatre" />
        <span class="stat"><span class="gold">350</span> лет истории</span>
        <img id="theatrepic" src="@/assets/theatrePic.png" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import VueScrollTo from "vue-scrollto";
export default {
  name: "pageContent",
  data() {
    return {
      text: "Как свидетельствуют архивные документы, первое каменное здание Большого театра начали возводить в 1775 году по проекту Антонио Ринальди. В дальнейшем, после того как Ринальди упал с лесов и не мог лично наблюдать за ходом работ, Екатерина II поручила немецкому театральному декоратору и архитектору Людвигу Филиппу Тишбейну создать новый проект театра, который и был воплощён архитекторами Ф. В. фон Бауром и М. А. Деденёвым. Открытие его состоялось в 1783 году, хотя, основываясь на других свидетельствах, годом открытия можно считать 1784 год.",
    };
  },
  methods: {
    scrollToContent() {
      VueScrollTo.scrollTo(this.$refs.content, 1000);
    },
  },
};
</script>
<style scoped>
/* Блоки с контентом */
#page {
  margin: 0 auto;
  padding: 10px;
  margin-top: 0;
  color: white;
  font-family: "Open Sans";
  font-weight: 700;
}
#content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 60%;
  margin-right: 20%;
  margin-left: 20%;
}
#block1 {
  margin-top: 10%;
  display: flex;
  height: 100%;
  width: 40%;
  flex-direction: column;
}
#block2 {
  margin-top: 10%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 50%;
}

/* ....................................................................... */



img {
  height: 70px;
  width: 70px;
}
/* Текст в блоках */
#description {
  font-size: 14px;
  line-height: 21px;
  width: 100%;
}
.subtitle {
  font-size: 21px;
  font-style: bold;
  white-space: nowrap;
}

#title {
  margin-top: 10%;
  text-align: center;
  font-weight: 300;
}
#title::first-letter {
  color: goldenrod;
}
.stat {
  margin-bottom: 15px;
}

/* ....................................................................... */


/* Стили для изображений */
.pic {
  margin-bottom: 15px;
}
#theatrepic {
  position: absolute;
  left: 70%;
  margin-top: 1%;
  width: 350px;
  height: 292px;
}
/* ....................................................................... */

.gold {
  color: goldenrod;
}



/* Медиа-запросы */
@media (max-width: 1400px) {
  #theatrepic {
    display: none;
  }
  #content {
    font-size: 20px;
    width: 80%;
    margin-left: 15%;
  }
  #description {
    font-size: 18px;
  }

  #block1 {
    width: 55%;
  }
  #block2 {
    width: 37%;
  }
  /* ....................................................................... */
}
</style>
