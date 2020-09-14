<template>
  <footer>
    <div class="rectangle">© 2019. Notus IT d.o.o.</div>
    <img src="../assets/img/Notus-logo-footer.svg" />
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};

</script>
<style scoped>
  footer{
    text-align: center;
    margin: 0 auto;
    max-width: 1920px;
    height: 200px;
    background: #081B2F 0% 0% no-repeat padding-box;
  }
  .rectangle{
    max-width: 1200px;
    height: 100px;
    background: #42BEB2 0% 0% no-repeat padding-box;
    margin: 0 auto;
    position: relative;
    top: -50px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #FFF;
    font: normal normal normal 18px/30px Montserrat;
  }
  @media screen and (max-width: 450px) {
    .rectangle{
      font-size: 15px;
    }
  }

</style>