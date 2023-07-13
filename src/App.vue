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
  <headerComponent />
  <mainComponent />
  <footerComponent />
</template>

<style scoped>

</style>
