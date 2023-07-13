<script>
</script>

<template>

<section class="my-container">

    
    <nav>
        
        <div class="img-container">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <ul class="nav-ul">

            <li>
                <a href="nogo">
                    characters
                </a>
            </li>

            <li>
                <a href="nogo">
                    comics
                </a>
            </li>

            <li>
               <a href="nogo">
                   movies
                </a> 
            </li>

            <li>
                <a href="nogo">
                    tv
                </a>
            </li>

            <li>
                <a href="nogo">
                    games
                </a>
            </li>

            <li>
                <a href="">
                    collectibles
                </a>
            </li>

            <li>
                <a href="nogo">
                    videos
                </a>
            </li>

            <li>
                <a href="nogo">
                    fans
                </a>
            </li>

            <li>
                <a href="nogo">
                    news
                </a>
            </li>

            <li>
                <a href="nogo">
                    shop
                </a>
            </li>
            
        </ul>
    </nav>

</section>

</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

.my-container{
    width: 1000px;

    nav{
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
        align-items: stretch;
        .img-container{
            width: 10%;
    
            img{
                width: 100%
            }
        }

        ul{
            list-style: none;
            flex-shrink: 0;
            flex-grow: 1;

            max-width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
           
            li{
                height: 100%;
                position: relative;
                display: flex;
                align-items: center;

                a, a:visited{
                    font-size: small;
                    display: block;
                    text-transform: uppercase;
                    color: $font-color-standard;
                    text-decoration: none;
                }

                &:hover{

                    &::after{
                    position: absolute;
                    top: calc(100% - 3px);
                    left:0;
                    content: '';
                    width: 100%;
                    border-bottom: 3px solid $dc-blue;

                    }  

                    a{
                        color: $dc-blue;
                    }
                }
            }
        }
    }
    
}



</style>