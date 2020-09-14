<template>
  <section id="task3">
    <h2>{{title}}</h2>
    <div class="container-text">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duo Reges: constructio interrete. Ut aliquid scire se gaudeant? Illi enim inter se dissentiunt. Nec vero sum nescius esse utilitatem in historia, non modo voluptatem. Quamquam te quidem video minime esse deterritum.</p>
    </div>
    <div class="container-images">
    <div class="container-left">
        <img src="../assets/img/notus-task2-img4.jpg">
    </div>
    <div class="container-center">
        <img src="../assets/img/notus-task2-img1.jpg">
        <img src="../assets/img/notus-task2-img3.jpg">
    </div>
    <div class="container-right">
        <img src="../assets/img/notus-task2-img2.jpg">
    </div>
</div>
  </section>
</template>

<script>
export default {
  name: 'Task3',
  props: {
    title: String
  }
};

</script>
<style scoped>
  section{
    text-align: center;
    padding: 100px 0;
    margin: 0 auto;
  }
  h2{
    font: normal normal bold 60px/73px Montserrat;
    color: #081B2F;
    opacity: 1;
  }
  .container-text {
    display: flex;
    justify-content: center;
    margin: 80px 0;
  }
  p{
    text-align: center;
    font: normal normal normal 18px/30px Montserrat;
    letter-spacing: 0px;
    color: #5C5C5C;
    opacity: 1;
    width: 960px;
  }
  .container-images{
    display:flex; 
    align-items:center;
    justify-content: center;
    column-gap: 30px;
  }
  .container-center {
    display: grid;
    grid-row-gap: 30px;
  }

  @media screen and (max-width: 450px) {
    section{
      padding: 75px 0;
    }
    h2{
      font-size: 45px;
    }
    .container-text{
      padding: 0 30px;
       margin: 50px 0;
    }
    p{
      font-size: 15px;
    }
    .container-images{
      width: 100%;
      display: grid;
      row-gap: 30px;
    }
    img{
      width: 60%;
      margin: 0 auto;
    }
  }

</style>