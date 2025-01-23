<template>
 <div>
  <Header></Header>
  <Main></Main>
  <Tools></Tools>
  <NewComerTools></NewComerTools>
  <Carousel></Carousel>
  <Mail></Mail>
 </div>
 <Footer></Footer>
	
</template>
<script setup>
import Header from './components/Header/Header.vue'
import Main from './components/Main/Main.vue';
import Tools from './components/ToolsSection/Tools.vue';
import NewComerTools from './components/NewComerTools/NewComerTools.vue';
import Carousel from './components/Carousel/Carousel.vue';
import Mail from './components/MailModal/Mail.vue';
import Footer from './components/Footer/Footer.vue';
</script>
<style scoped lang="scss">
div {
  width: 80%;
	margin: 0 auto;
}
</style>
