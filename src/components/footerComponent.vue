<script>

export default{
  data(){
    return{
        cards:[
            {
                name:'digital comics',
                icon:'src/assets/img/buy-comics-digital-comics.png'
            },
            {
                name:'dc merhandise',
                icon:'src/assets/img/buy-comics-merchandise.png'
            },
            {
                name:'subscription',
                icon:'src/assets/img/buy-comics-subscriptions.png'
            },
            {
                name:'comic shop locator',
                icon:'src/assets/img/buy-comics-shop-locator.png'
            },
            {
                name:'dc power visa',
                icon:'src/assets/img/buy-dc-power-visa.svg'
            },
            
        ]
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
    <section class="row">
        <div class="col"
            v-for="(element,index) in cards">
            <div class="card row align-center">
                <div class="img">
                    <img :src="element.icon" :alt="element.name">
                </div>
                <div class="title">
                    {{element.name}}
                </div>
            </div>
        </div>
    </section>

  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main.scss' as *;
@use '../assets/scss/debugger.scss' as *;
@use '../assets/scss/variables.scss' as *;

footer{
    section{
        background-color: $main-color;
        padding: 40px 20px;
        .col{
            width: calc(100% / 5);
            padding: 10px;
            @include debug-one;
            .card{
                @include debug-two;
                // height: 60px;
                .img{
                    height: 40px;
                    margin-right: 10px;
                }
                .title{
                    text-transform: uppercase;
                    font-size: 0.85rem;
                }
            }
        }
    }
}
</style>