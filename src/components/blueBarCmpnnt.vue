<script>

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

</style>