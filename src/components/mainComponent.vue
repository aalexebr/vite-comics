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
  <main>
    <h1>
        CONTENT
    </h1>
    <!-- <footer class="row">

    </footer> -->
  </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main.scss' as *;
@use '../assets/scss/debugger.scss' as *;
@use '../assets/scss/variables.scss' as *;
main:not(footer){
    background-color: black;
    color: white;
    padding: 20px 0 0 0;
    // footer{
    //   background-color: $main-color;
    //   height: 30px;
    // }
}

</style>