<script>
import headerComponent from './components/headerComponent.vue'
import mainComponent from './components/mainComponent.vue'
import footerComponent from './components/footerComponent.vue'

export default{
  data(){
    return{
      name: 'hello'
    }
  },
  methods:{
    getImgPath: function(imgPath){
      return new URL (imgPath, import.meta.url).href;
    }
  },
  components:{
    headerComponent,
    mainComponent,
    footerComponent,
  }
}
</script>

<template>
  <!-- <div class="container"> -->
    <headerComponent />
    <mainComponent />
    <footerComponent />
  <!-- </div> -->
</template>

<style lang="scss">
@use 'assets/scss/main.scss' as *;
// .container{
//   margin: auto;
//   max-width: 1000px;
// }
// *{
  
//     padding: 0;
//     margin: 0;
//     box-sizing: border-box;
//     font-family: Arial, Helvetica, sans-serif;
// }
</style>
