<template>
  <div class="background">
    <div>
      <mainContent ref="content" />
    </div>
  </div>
</template>

<script>
import VueScrollTo from "vue-scrollto";
import mainContent from "./firstPage/content.vue";
export default {
  data() {
    return {};
  },
  methods: {
    scrollToContent() {
      VueScrollTo.scrollTo(this.$refs.content, 800);
    },
  },

  components: {
    mainContent,
  },
};
</script>
<style>
.background {
  background-image: url(@/assets/Rectangle\ 3.jpg);
  background-position: center center;
  background-size: cover;
  height: 100vh;
  width: 100%;
}
@media (max-width: 1045px) {
  .background {
    height: 900px;
  }
}

</style>
