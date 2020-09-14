<template>
  <div id="app">
    <LoadingPage />
    <Header />
    <Menu />
    <Task3 title="Task 3"/>
    <Carousel /> 
    <NotusMap class="map"/>
    <Task5 title="Task 5"/>
    <Footer/>
  </div>
</template>

<script>
import LoadingPage from './components/LoadingPage.vue'
import Header from './components/Header.vue'
import Menu from './components/Menu.vue'
import Task3 from './components/Task3.vue'
import Carousel from './components/Carousel.vue'
import NotusMap from './components/NotusMap.vue'
import Task5 from './components/Task5.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    LoadingPage,
    Header,
    Menu,
    Task3,
    Carousel,
    NotusMap,
    Task5,
    Footer
  },
  computed:{
  }
}
</script>

<style>
.map {
    height: 600px;
}
</style>
