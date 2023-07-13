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
  <footer>
    footer

  </footer>
</template>

<style scoped>

</style>