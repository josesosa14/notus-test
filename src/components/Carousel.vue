<template>
   <section id="task4">
     <h2>Task 4</h2>
      <div class="carousel-container">
    <VueSlickCarousel  @init="onInitCarousel" v-bind="settings">
      <template #prevArrow="arrowOption">
        <div class="custom-arrow">
          {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
        </div>
      </template>
      <div v-for="item in images" :key="item"><img :src="item" /></div>
      
    </VueSlickCarousel>
    </div>
  </section>
 
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'

  export default {
    name: 'Carousel',
    components: { VueSlickCarousel },
    data(){
    return {
      images:[
        require("../assets/img/notus-task3-img1.jpg"),
        require("../assets/img/notus-task3-img2.jpg"),
        require("../assets/img/notus-task3-img3.jpg"),
        require("../assets/img/notus-task3-img4.jpg"),
      ],
      settings: {
        "dots": false,
        "infinite": false,
        "speed": 500,
        "slidesToShow": 3,
        "slidesToScroll": 1,
        "initialSlide": 0,
        "responsive": [
          {
            "breakpoint": 1024,
            "settings": {
              "slidesToShow": 3,
              "slidesToScroll": 3,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 600,
            "settings": {
              "slidesToShow": 2,
              "slidesToScroll": 2,
              "initialSlide": 2
            }
          },
          {
            "breakpoint": 480,
            "settings": {
              "slidesToShow": 1,
              "slidesToScroll": 1
            }
          }
        ]
      
      },
    }
  },
  methods: {
      onInitCarousel() {
        console.log('our carousel is ready')
      }
  }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  section{
    text-align: center;
    padding: 100px 0;
    margin: 0 auto;
    background: #081B2F;
    max-width: 1920px;
  }
  h2{
    font: normal normal bold 60px/73px Montserrat;
    color: #FFF;
    opacity: 1;
    margin-bottom: 80px;
  }
  .carousel-container{
    width:100%;
    display: flex;
    justify-content: center;
  }
  .slick-slider{
    width: 60%;
  }
  .slick-prev  {
    left: -85px;
  }

   @media screen and (max-width: 1366px) {
    .slick-slider{
      width: 70%;
    }
    .slick-prev  {
      left: -30px;
    } 
  }

  @media screen and (max-width: 450px) {
    section{
      padding: 75px 0;
    }
    h2{
      font-size: 45px;
    }
    .slick-slider{
      width: 75%;
    }
  }

</style> 
