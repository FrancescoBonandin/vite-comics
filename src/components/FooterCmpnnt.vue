<script>
import { shallowReactive } from 'vue';

export default {
    data(){
        return {
            buyComicsList:[
                {img:"buy-comics-digital-comics.png",
                 text:"digital comics"},
                {img:"buy-comics-merchandise.png",
                 text: "merchandise"},
                {img:"buy-comics-shop-locator.png",
                 text:"shop locator"},
                {img:"buy-comics-subscriptions.png",
                 text:"subscription"},
                {img:"buy-dc-power-visa.svg",
                 text:"power visa"}
            ],
                footerLinks:[
                    {name:"dc comics",
                     links:["characters","comics","movies",
                        "TV","games","videos", "news"]
                    },
                    {name:"shop",
                     links:["shop dc","shop dc collectibles"]
                    },
                    {name:"dc",
                     links:["terms of use","privacy policy",
                     "ad choices","advertising","jobs","subscriptions",
                     "talent workshop","CPSC certificates","ratings","shop help",
                     "contact us"]
                    },
                    {name:"sites",
                     links:["DC","MAD magazine","DC kids","DC universe", "DC power visa"]}
                ]

        }
    },
    methods:{

        getImgPath:function(imgPath){
            return new URL(imgPath,import.meta.url).href; 
        }
    }
}
</script>

<template>
    
    <section class="buy-comics">

        <div class="my-container">
        
            <ul>
                
                <li v-for="(listItem,i) in buyComicsList ">

                    <div class="img-container">
                        <img :src="getImgPath(`../assets/img/buy-comics/${listItem.img}`)" alt="">
                    </div>
                    
                    <div>
                        <a href="nogo">
                            
                            {{ listItem.text }}
                            
                        </a>
                    </div>
                    
                </li>
                
            </ul>

        </div>
    
    </section>

    
    <section class="jumbotron">

        <div class="img-container">

            <img src="../assets/img/dc-logo-bg.png" alt="">

        </div>
        
        <div class="my-container"> 

            <nav class="left-jumbo-nav">
                
                <div v-for="(linksBlock,i) in footerLinks">

                    <h4>
                        {{ linksBlock.name }}   
                    </h4>

                    <ul>

                        <li v-for="link in footerLinks[i].links">

                            <a href="nogo">
                                {{ link }}
                            </a>

                        </li>

                    </ul>

                </div>


            </nav>

        </div>
        
    </section>

    
    <section>
    
    </section>


</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;
.buy-comics{
    background-color: $dc-blue;
    
    color: white;

    ul{
        list-style: none;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        flex-grow: 0;
        
        li{
            display: flex;
            flex-wrap: wrap;
            flex-grow: 0;
            flex-shrink: 1;
            justify-content: center;
            align-items: center;
            max-width: calc(100% / 5);
            padding: 0.3rem;
            .img-container{
                height:2.5rem;
                margin-right: 0.3rem;
                img{
                    height: 100%;
                }
            }

            a,a:visited{
                color: inherit;
                text-decoration: none;
                text-transform: uppercase;
                font-size: small;
            }


        }
    }
}

.my-container{
    height: 100%;
}
.jumbotron{
    position: relative;
    height: 50vh;
    background-image: url(../assets/img/footer-bg.jpg);
    .img-container{
        position: absolute;
        top: 0;
        left: 0;
        overflow-y: hidden;
        height: 100%;       
        width: 100%; 
        img{
            position: absolute;
            left: 70%;
            top: 50%;
            transform: translate(-50%,-50%);
            height: 70vh;
        }
    }
    .left-jumbo-nav{
        width: 50%;
        max-height:100%;
        display:flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: flex-start;
        flex-wrap: wrap;
        flex-shrink: 1;
        flex-grow: 0;

        >div{
            max-width: calc(70% / 3);
            display:flex;
            flex-direction: column;
            flex-grow: 0;
            text-transform: capitalize;
            

            h4{
                color: white;
                margin: 0.5rem 0;
            }

            ul{
                list-style: none;
                padding-left: 0;
                font-size: small;

                li{ 
                    padding: 0.2rem;
                    a, a:visited{
                        color: $font-color-grey;
                    }
                }
            }
        }
    }
}

</style>