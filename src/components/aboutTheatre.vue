<template>
  <div id="background" ref="content">
    <MainContent></MainContent>
  </div>
</template>
<script>
import MainContent from "./secondPage/content.vue";
import VueScrollTo from "vue-scrollto";
export default {
  data() {
    return {};
  },
  components: { MainContent },
  methods: {
    scrollToContent() {
      VueScrollTo.scrollTo(this.$refs.content, 1000);
    },
  },
};
</script>
<style scoped>
#background {
  margin: 0;
  padding: 0;
  background-color: #3a3939;
  height: 100vh;
}
@media (max-width: 1045px) {
  #background {
    height: 900px;
  }
}
</style>
