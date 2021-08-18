<template>
  <div id="app">
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
#app {
  overflow-x: hidden;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #010C25;
  height: 100vh;
  padding-right: 20px;
}
.righty{
  margin-left:
}
</style>
