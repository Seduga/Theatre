<template>
    <div id="background" >
    <div id="content" ref="content">
        <pageContent
        
        />
    </div>
    </div>
</template>
<script>
import VueScrollTo from "vue-scrollto";
import pageContent from './thirdPage/content.vue';
export default{
    data(){
        return{

        }
    },
    components: {
        pageContent,
    },
    methods: {
    scrollToContent() {
      VueScrollTo.scrollTo(this.$refs.content, 800);
    },
  },
}
</script>

<style scoped>
#background{
    margin:0;
    padding: 0;
    background-color: #3a3939;
    height: max-content;
    

}
/* @media(max-width: 1045px){
  #background{
    height: 900px;
  }
} */

</style>