<script>

export default{
  data(){
    return{

        nav:[
            {
                title :'characters',
                link : ''
            },
            {
                title :'comics',
                link : ''
            },
            {
                title :'movies',
                link : ''
            },
            {
                title :'tv',
                link : ''
            },
            {
                title :'games',
                link : ''
            },
            {
                title :'collectibles',
                link : ''
            },
            {
                title :'videos',
                link : ''
            },
            {
                title :'fans',
                link : ''
            },
            {
                title :'news',
                link : ''
            },
            {
                title :'shop',
                link : ''
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
  <header >
    <div class="container">
        <div class="row align-center space-between"> 
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC">
            </div>
            <nav>
                <ul>
                    <li v-for="(element, i) in nav">
                        <a href="#/">
                            {{element.title}}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>    
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main.scss' as *;
@use '../assets/scss/debugger.scss' as *;
@use '../assets/scss/variables.scss' as *;
@use '../assets/scss/utilities.scss' as *;


header{
    padding: 5px;
   li{
    display: inline-block;
    padding: 5px;
    &:hover{
        border-bottom: 2px solid $main-color;
        color: $main-color;
    }
        a{
            display: inline-block;
            padding: 5px;
            text-transform: capitalize;
        }
    }
    
}
.logo{
    height: 60px;
}
</style>
