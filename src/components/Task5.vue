<template>
  <section id="task5">
    <div class="container-line">
      <div class="line"></div>
    </div>
    <h2>{{title}}</h2>
    <div class="container-text">
      <p>Quas enim kakaw Graeci appellant, vitia malo quam malitias nominare. Idem adhuc; Idemque diviserunt naturam hominis in animum et corpus. Istam voluptatem, inquit, Epicurus ignorat? Duo enim genera quae erant, fecit tria. 
        <span class="p-highlight">Ut proverbia non nulla veriora sint quam vestra dogmata</span> 
        An haec ab eo non dicuntur? Idcirco enim non desideraret, quia, quod dolore caret, id in voluptate est. Quoniam, si dis placet, ab Epicuro loqui discimus. Quid sequatur, quid repugnet, vident.
      </p>
    </div>
    <div class="container-rectangle">
      <div class="rectangle">Hover to have solid fill</div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Task5',
  props: {
    title: String
  }
};

</script>
<style scoped>
  section{
    text-align: center;
    padding-bottom: 230px;
    margin: 0 auto;
  }
  .container-line{
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .line{
    width:3px; 
    height:200px; 
    background-color:#081B2F; 
    top: -100px;
    position: relative;
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
  p span{
    color:#42BEB2;
    display: block;
    margin-top: 30px;
  }
  .container-rectangle{
    display:flex;
    justify-content: center;
  }
  .rectangle{
    border: #F89D36 solid 5px;
    width: 300px;
    height: 120px;
    display: flex;
    align-items: center;
    justify-content: center;
    font: normal normal bold 20px/24px Montserrat;
    color: #081B2F;
  }
   @media screen and (max-width: 450px) {
    h2{
      font-size: 45px;
      margin-top: -50px;
    }
    .container-text{
      margin: 50px 0;
      padding: 0 30px;
    }
    p{
      font-size: 15px;
    }
    .rectangle{
      font-size: 17px;
    }
    section{
      padding-bottom: 150px;
    }
  }

</style>