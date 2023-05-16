<template>
    <div class="layout">
      <Navigation></Navigation>
      <MobileSide></MobileSide>
      <Side></Side>
    </div>
  </template>
  <script>
 import Navigation from './firstPage/Navigation.vue';
 import MobileSide from './firstPage/MobileSide.vue';
 import Side from './firstPage/Side.vue';
  export default {
    components: {Navigation, MobileSide, Side },
  };
  </script>
  <style scoped>
  .layout{
    padding: 0;
    margin: 0;
    position: relative;
    top: 0;
  }
  </style>