<template>
  <div id="navb">
      <img src="../assets/logo.png" alt="" class="logo">
      <div class="svg">
      <Icons name="rocket" class="active"/>
      <Icons name="domain"/>
      <Icons name="account"/>
      <Icons name="safe"/>
      <Icons name="tune"/>
      </div>
  </div>
</template>

<script>
import Icons from './Icons.vue'

export default {
    name: 'navbar',
    components: {
        Icons
    }
}
</script>

<style>
    #navb{
        height: 100vh;
        position: fixed;
        padding: 25px 20px;
        background: #010C25;
        z-index: 100;
        widows: 20%;
    }
    .logo{
        height: 32px;
        width: 28px;
        margin-bottom: 100px;
        margin-left: 10px;
    }
    .svg{
        line-height: 50px;
        text-align: center;
    }
    .active{
        background: #5285F2;
        padding: 5px 10px;
        border-radius: 8px;
    }
</style>