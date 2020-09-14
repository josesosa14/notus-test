<template>
  <header>
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel" data-interval="false">
      <div id="carouselcontainer" class="carousel-inner" role="listbox" >
        <div class="carousel-item" :class="{ 'active': index === 1 }" v-for="(item, index) in carousel_images" :key="item" :style="{backgroundImage:`url(${item})`}"></div>
      </div>
    </div>
    <div class="container-elements">
      <img src="../assets/img/Notus-logo-main.png" class="logo" alt="LOGO" />
      <h2 class="title">Notus Front-end test</h2>
      <div class="indicators">
        <a
          class="carousel-control-custom-prev"
          href="#carouselExampleIndicators"
          role="button"
          data-slide="prev"
          @click="prev()"
        >
          <img src="../assets/img/prev.png" alt="prev" />
        </a>
        <div class="indicators-numbers">{{img_selected}}/{{carousel_images.length}}</div>
        <a
          class="carousel-control-custom-next"
          href="#carouselExampleIndicators"
          role="button"
          data-slide="next"
          @click="next()"
        >
          <img src="../assets/img/next.png" alt="next" />
        </a>
      </div>
    </div>
  </header>
</template>

<script>
import $ from 'jquery'
export default {
  created() {
  },
  data() {
    return {
      carousel_images: [
        require("../assets/img/notus-task1-img2.jpg"),
        require("../assets/img/notus-task1-img1.jpg"),
        require("../assets/img/notus-task1-img3.jpg")
      ],
      img_selected:1
    };
  },
  mounted(){
    
  },
  methods: {
    prev(){
      this.img_selected = $('div.active').index()==-1 ? $('div.active').index()+2 : $('div.active').index()+1;
    },
    next(){
      console.log("jose")
      this.img_selected = $('div.active').index()==-1 ? $('div.active').index()+2 : $('div.active').index()+1;
    }
  },
};

</script>
<style scoped>
header{
  max-width: 1920px;
  margin: 0 auto;
}
header .container-elements{
  position: relative;
  height: 100vh;
  min-height: 350px;
  text-align: center;
}
.logo {
  z-index: 1;
  position: relative;
  top: 100px;
}
.title {
  font: normal normal bold 60px/73px Montserrat;
  color: #fff;
  position: relative;
  z-index: 1;
  top: 300px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: absolute;
}
.carousel-item {
  height: 100vh;
  min-height: 350px;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  box-shadow: inset 0 0 0 1000px rgba(8, 27, 47, 0.7);
}
.carousel-control-custom-prev {
  left: 40%;
}
.carousel-control-custom-next {
  right: 40%;
}
.carousel-control-custom-next,
.carousel-control-custom-prev {
  transition: opacity 0.15s ease;
}
.indicators{
  position: absolute;
  bottom: 80px;
  z-index: 1;
  width: 100%;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-pack: center;
  justify-content: center;
  color: #fff;
  text-align: center;
}
.indicators-numbers{
  width: 5%;
  font: normal normal normal 16px/19px Montserrat;
}

@media (max-width: 450px) {
  .logo {
    top: 80px;
  }
  .title {
    font-size: 30px;
    top: 130px;
    padding: 0 10px;
  }
  .indicators-numbers{
    width: 15%;
  }
}
</style>