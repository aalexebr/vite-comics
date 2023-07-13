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
            
        ],
        navDcComics:[
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
                title :'videos',
                link : ''
            },
            {
                title :'news',
                link : ''
            },
        ],
        navShop:[
                {
                    title :'shop DC',
                    link : ''
                },
                {
                    title :'shop DC collectibles',
                    link : ''
                },
        ],
        navDC:[
                {
                    title :'terms of use',
                    link : ''
                },
                {
                    title :'privacy policy (new)',
                    link : ''
                },
                {
                    title :'ad choices',
                    link : ''
                },
                {
                    title :'advertising',
                    link : ''
                },
                {
                    title :'jobs',
                    link : ''
                },
                {
                    title :'subscriptions',
                    link : ''
                },
                {
                    title :'talent workshops',
                    link : ''
                },
                {
                    title :'CPSC certificates',
                    link : ''
                },
                {
                    title :'ratings',
                    link : ''
                },
                {
                    title :'shop help',
                    link : ''
                },
                {
                    title :'contact us',
                    link : ''
                },
        ],
        navSites:[
                {
                    title :'DC',
                    link : ''
                },
                {
                    title :'MAD magazine',
                    link : ''
                },
                {
                    title :'DC kids',
                    link : ''
                },
                {
                    title :'DC universe',
                    link : ''
                },
                {
                    title :'DC power visa',
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
  <footer>
    <section class="row cards">
        <div class="col-25"
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
    <section class="footer-jumbo-links row align-center">
        <div class="col-4">
            <div class="row">
                <div class="col-4">
                    <nav>
                        <h4>
                            dc comics
                        </h4>
                        <ul>
                            <li v-for="(element,index) in navDcComics">
                                <a href="#/">
                                {{ element.title }}  
                                </a>
                            </li>
                        </ul>
                    </nav>
                    <nav>
                        <h4>
                            shop
                        </h4>
                        <ul>
                            <li v-for="(element,index) in navShop">
                                <a href="#/">
                                {{ element.title }}  
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="col-4">
                    <nav>
                        <h4>
                            dc
                        </h4>
                        <ul>
                            <li v-for="(element,index) in navDC">
                                <a href="#/">
                                {{ element.title }}  
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="col-4">
                    <nav>
                        <h4>
                            dc
                        </h4>
                        <ul>
                            <li v-for="(element,index) in navSites">
                                <a href="#/">
                                {{ element.title }}  
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
        <div class="col-auto"></div>
    </section>
    <section class="footer-bottom">

    </section>
  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main.scss' as *;
@use '../assets/scss/debugger.scss' as *;
@use '../assets/scss/variables.scss' as *;

footer{
    .cards{
        background-color: $main-color;
        padding: 40px 20px;
        .col-25{
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
    .footer-jumbo-links{
        @include debug-two;
        // height: 100px;
        .col-4{
            @include debug-one;
            // height: 60px;
            h4{
                color: white;
                text-transform: uppercase;
                margin: 5px 0;
            }
            
        }
        li{
            list-style-type: none;
            font-size: 0.85rem;
            text-transform: capitalize;
        }
        a{
            text-decoration: none;
            color: inherit;
        }
    }
}
</style>