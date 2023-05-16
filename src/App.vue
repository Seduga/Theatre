<template>
  <div id="app">
    <navigationBar @scrollToContent="scrollToContent"></navigationBar>
    <sideBar></sideBar>
    <mobileInterface v-show="screenWidth <= 1024"></mobileInterface>
    <mainPage ref="content1"></mainPage>
    <aboutTheatre ref="content2"></aboutTheatre>
    <ourPerfomance ref="content3"></ourPerfomance>
  </div>
</template>

<script>
import mainPage from "./components/mainPage.vue";
import aboutTheatre from "./components/aboutTheatre.vue";
import navigationBar from "@/components/layout/navigationBar.vue";
import sideBar from "@/components/layout/side.vue";
import mobileInterface from "@/components/layout/mobileInterface.vue";
import ourPerfomance from "./components/ourPerfomance.vue";
export default {
  name: "App",
  data() {
    return {
      screenWidth: 0,
    };
  },
  created() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.screenWidth = window.innerWidth;
    },
    scrollToContent(contentId) {
      if (contentId === "content1") {
        this.$refs.content1.scrollToContent();
      } else if (contentId === "content2") {
        this.$refs.content2.scrollToContent();
      }
      else if( contentId === 'content3'){
        this.$refs.content3.scrollToContent();
      }
    },
  },
  components: {
    mobileInterface,
    sideBar,
    navigationBar,
    mainPage,
    aboutTheatre,
    ourPerfomance,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;700;800&display=swap");
</style>
