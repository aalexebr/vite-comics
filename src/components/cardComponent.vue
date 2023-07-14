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



