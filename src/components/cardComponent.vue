<script>

export default{
  props:{
    itemImg : String,
    itemTitle : String
  }
}
</script>

<template>
    <div class="card">
              <div class="img">
                <img :src="itemImg" alt="">
              </div>
              <div class="title">
                <span>
                  {{itemTitle}}
                </span>
              </div>
            </div>
</template>

<style lang="scss" scoped>
.img{
        height: 175px;
        margin-bottom: 10px;
        img{
          object-fit: cover;
        }
      }
</style>



