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
    main

  </main>
</template>

<style lang="scss" scoped>

</style>