



<script>

import HeaderCmpnnt from './components/HeaderCmpnnt.vue'
import MainCmpnnt from './components/MainCmpnnt.vue'
import FooterCmpnnt from './components/FooterCmpnnt.vue'

export default {
  components:{
    HeaderCmpnnt,
    MainCmpnnt,
    FooterCmpnnt,
  },
   data(){
      return{

      }
    }
  }
</script>

<template>

<header>
<HeaderCmpnnt/>
</header>

<main>
<!-- <MainCmpnnt/> -->
</main>

<footer>
<!-- <FooterCmpnnt/> -->
</footer>

</template>

<style lang="scss" >
@use './assets/scss/main' as *;
@import './assets/scss/partials/variables';

header{
  background-color: white;
}

main{
  min-height: 10vh;
  background-color:$content-bg;
}

footer{
  min-height: 60vh;
  background-color: $footer-bg;

}
</style>
