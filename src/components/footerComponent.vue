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
        ],
        linkSocial:[
            {   
                img: 'src/assets/img/footer-facebook.png',
                href:''
            },
            {   
                img: 'src/assets/img/footer-periscope.png',
                href:''
            },
            {   
                img: 'src/assets/img/footer-pinterest.png',
                href:''
            },
            {   
                img: 'src/assets/img/footer-twitter.png',
                href:''
            },
            {   
                img: 'src/assets/img/footer-youtube.png',
                href:''
            },
        ]
    }
  },
  methods:{
    getImgPath: function(imgPath){
      return new URL (`../assets/img/${imgPath}`, import.meta.url).href;
    }
  },
}
</script>

<template>
  <footer>
        <section class=footer-top>
            <div class="container">
                <div class="row cards">
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
                </div>
            </div>
        </section>
        <section class="footer-jumbo-links pos-relative">
            <div class="container">
                <div class="row align-center">
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
                                        sites
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
                    <div class="pos-absolute img">
                        <img src="src/assets/img/dc-logo-bg.png" alt="">
                    </div>
                    <!-- <div class="col-auto"></div> -->
                </div>
            </div>
        </section>
        <section class="footer-bottom">
            <div class="container">
                <div class="row align-center space-between">
                    <div class="button">
                        <a href="#/">
                            sign-up now
                        </a>
                    </div>
                    <div class="row align-center social-links">
                        <h4>
                            follow us
                        </h4>
                        <ul class="row align-center">
                            <li v-for="(element,i) in linkSocial">
                                <div class="img">
                                    <a href="">
                                        <img :src="element.img" alt="">
                                    </a>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    <!-- </div> -->
  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main.scss' as *;
@use '../assets/scss/debugger.scss' as *;
@use '../assets/scss/variables.scss' as *;
@use '../assets/scss/utilities.scss' as *;
$bottom-footer: #303030;
footer{
    .footer-top{
        background-color: $main-color;
        .cards{
                background-color: $main-color;
                padding: 40px 20px;
                cursor: pointer;
            .col-25{
                width: calc(100% / 5);
                padding: 10px;
                // @include debug-one;
                .card{
                    // @include debug-two;
                    padding: 5px;
                    .img{
                        height: 45px;
                    }
                    .title{
                        padding-left: 10px;
                        text-transform: uppercase;
                        font-size: 0.85rem;
                        }
                    }
            }
        }

    }
    // .img{
    //     height: 100%;
    //     right: 60px;
    //     img{
    //         object-fit: cover;
    //     }
    // }
    .cards{
        background-color: $main-color;
        padding: 40px 20px;
        cursor: pointer;
        .col-25{
            width: calc(100% / 5);
            padding: 10px;
            // @include debug-one;
            .card{
                // @include debug-two;
                // height: 60px;
                padding: 5px;
                .img{
                    
                    height: 45px;
                }
                .title{
                    padding-left: 10px;
                    text-transform: uppercase;
                    font-size: 0.85rem;
                }
            }
        }
    }
    .footer-jumbo-links{
        // @include debug-two;
        // height: 100px;
        padding: 20px;
        background-image: url('src/assets/img/footer-bg.jpg');
        color: $secondary-text-color;
        .col-4{
            // @include debug-one;
            // height: 60px;
            h4{
                color: white;
                text-transform: uppercase;
                margin: 5px 0;
            }
            // .col-4{
            //     padding: 0 10px;
            // }
            .col-4:nth-of-type(2){
                margin: 0 20px;
            }
        }
        li{
            // list-style-type: none;
            font-size: 0.85rem;
            text-transform: capitalize;
        }
        // a{
        //     text-decoration: none;
        //     color: inherit;
        // }
        .img{
        height: 100%;
        right: 60px;
        img{
            object-fit: cover;
        }
    }
    }
    .footer-bottom{
        background-color: $bottom-footer;
        padding: 20px;
        // @include debug-two;
        // li{
        //     list-style-type: none;
        // }
        .button a{
            display: inline-block;
            padding: 10px;
            border: 3px solid $main-color;
            text-transform: uppercase;
            font-size: 0.85rem;
            color: $main-text-color;
        }
        .social-links{
            li{
                display: inline-block;
                padding: 10px;
            }
            h4{
                text-transform: uppercase;
                color: $main-color;
            }
        }
    }
}
</style>