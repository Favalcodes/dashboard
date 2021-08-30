<template>
  <div id="app">
    <div class="desktop">
      <b-row>
      <b-col col md="1">
        <Navbar />
      </b-col>
      <b-col class="righty">
        <b-row>
          <Top />
        </b-row>
        <b-row>
          <b-col col md="8">
            <Left />
          </b-col>
          <b-col>
            <Right />
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    </div>
    <div class="mobile">
      <img src="./assets/oops.png" class="oops" alt="">
      <h3>Seems like you are using a MOBILE device, please change to a DESKTOP.</h3>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Top from './components/Top.vue'
import Left from './components/Left.vue'
import Right from './components/Right.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Top,
    Right,
    Left
  }
}
</script>

<style>
@font-face {
  font-family: "Proxima";
  src: url("./font/proxima.otf");
}
#app {
  overflow-x: hidden;
  font-family: "Proxima", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #010C25;
  height: 100vh;
  padding-right: 20px;
}
.mobile{
  display: none;
}
@media (max-width: 800px) {
  .desktop{
    display: none;
  }
  .mobile{
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
  padding: 8%;
}
.oops{
  position: relative;
  width: 70%;
  height: 40%; 
}
.mobile h3{
  position: relative;
  font-weight: 800px;
  color: #fff;
  text-align: center;
}
}

</style>
