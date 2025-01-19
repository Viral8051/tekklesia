<template>
    <div class="home-main">
      <navbar />
      <main-content/>
      <option-main/>
      <res-option-main/>
      <footer-content/>
    </div>    
</template>
<script>

import navbar from './nav'
import MainContent from './main-content'
import OptionMain from './option-main'
import ResOptionMain from './res-option-main'
import FooterContent from './footer-content'

export default{
    name:'home',
    components:{
        navbar,
        MainContent,
        OptionMain,
        ResOptionMain,
        FooterContent
    }
}
</script>

<style scoped>
.home-main{
    position: relative;
    
    width: 100%;
    font-weight: 400;
    background: #EDEDED;
}

</style>