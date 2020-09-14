<template>
  <nav>
    <div id="myNav" class="overlay">
      <a class="closebtn" id="closebtn" @click="closeNav()">
        <img src="../assets/img/notus-meni-close.svg" alt="&times;" />
      </a>
      <img class="logo" src="../assets/img/Notus-logo-meni.svg" alt="NOTUS" />
      <div class="overlay-content">
        <a href="#task3" @click="closeNav()">TASK 3</a>
        <a href="#task4" @click="closeNav()">TASK 4</a>
        <a href="#task5" @click="closeNav()">TASK 5</a>
      </div>
    </div>
    <span class="hamburger" id="hamburger" @click="openNav()">
      <img class="logo" src="../assets/img/notus-meni.png" alt="&#9776;" />
    </span>
  </nav>
</template>

<script>
export default {
  name: "Menu",
  props: {},
  methods: {
    openNav() {
      document.getElementById("myNav").style.height = "100%";
      document.getElementById("hamburger").style.display = "none";
      document.getElementById("closebtn").style.display = "block";
    },
    closeNav() {
      document.getElementById("myNav").style.height = "0%";
      document.getElementById("hamburger").style.display = "block";
      document.getElementById("closebtn").style.display = "none";
    },
  },
};
</script>

<style scoped>
 .hamburger {
  cursor: pointer;
  top: 140px;
  left: 120px;
  position: absolute;
  z-index: 1;
}

.overlay {
  height: 0%;
  width: 100%;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  font-family: "Montserrat", sans-serif;
  background-color: #f89d36;
  overflow-y: hidden;
  transition: 0.5s;
  text-align: center;
}

.overlay-content {
  position: relative;
  top: 25%;
  left: 250px;
  width: 100%;
  text-align: left;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 60px;
  color: #ffffff;
  display: block;
  font-weight: bold;
  transition: 0.3s;
}

.overlay a:hover, .overlay a:focus {
  color: #f1f1f1;
}

.overlay .closebtn {
  position: absolute;
  top: 134px;
  left: 100px;
  cursor: pointer;
}

.overlay .logo {
  position: relative;
  top: 100px;
}

@media screen and (max-width: 450px) {
  .overlay {overflow-y: auto;}
  .overlay a {font-size: 30px}
  .overlay-content{
    left: 0;
    text-align: center;
  }
  .overlay .closebtn, .hamburger{
    top: 20px;
    left: 20px;
  }
  .overlay .logo {
    top: 80px;
  }
}
@media screen and (min-width: 1921px) {
  .hamburger {
    left: 500px;
  }
}
</style>
