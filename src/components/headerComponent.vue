<script>

export default{
  data(){
    return{

    }
  },
  methods:{
    getImgPath: function(imgPath){
      return new URL (imgPath, import.meta.url).href;
    }
  },
}
</script>

<template>
  <header>
    header
  </header>
</template>

<style lang="scss"scoped>
@use '../assets/scss/debugger.scss' as *;
</style>
