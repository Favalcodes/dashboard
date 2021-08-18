<template>
  <div id="right">
      <div class="box3">
        <div class="d-flex justify-content-between">
          <div class="fam d-flex">
            <Icons name="family" class="icon" />
            <div class="txt">
              Family & Friends
            </div>
          </div>
          <div class="fam d-flex text-white">
            <font-awesome-icon icon="plus-circle" class="font"/>
            <div class="add">Add New</div>
          </div>
        </div>
        <div class="family d-flex justify-content-between">
          <div class="img">
            <img src="../assets/hanna.png" alt="">
            <p>Hanna</p>
            <span>Owner</span>
          </div>
          <div class="img">
            <img src="../assets/dad.png" alt="">
            <p>Dad</p>
            <span>Full Access</span>
          </div>
          <div class="img">
            <img src="../assets/mum.png" alt="">
            <p>Mum</p>
            <span>Full Access</span>
          </div>
          <div class="img">
            <img src="../assets/timothy.png" alt="">
            <p>Timothy</p>
            <span>Restricted</span>
          </div>
          <div class="img">
            <img src="../assets/jackson.png" alt="">
            <p>Jackson</p>
            <span>Full Access</span>
          </div>
        </div>
      </div>
      <div class="box4">
        <div class="d-flex justify-content-left">
          <Icons name="video" class="icon" />
          <div class="txt">
            Entrance
          </div>
        </div>
        <div class="vid">
          <div class="cam">
            <div class="live">
              <Icons name="live" class="circle"/>
              <h6>Live</h6>
            </div>
          </div>
          <h5>Main Entrance</h5>
          <div class="cam2">
            <div class="live">
              <Icons name="live" class="circle"/>
              <h6>Live</h6>
            </div>
          </div>
          <h5>Backyard</h5>
        </div>
      </div>
  </div>
</template>

<script>
import Icons from './Icons.vue'

export default {
    name: 'Right',
    components: {
      Icons
    }
}
</script>

<style>
  .box3{
    background: #00123A;
    height: 235px;
    border-radius: 32px;
    padding: 24px;
    width: 100%;
    margin-bottom: 32px;
  }
  .fam{
    height: 40px;
    justify-content: center;
    align-content: center;
    align-items: center;
  }
  .icon{
    background: #5285F2;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    text-align: center;
    padding: 7px;
    margin-right: 10px;
  }
  .txt{
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    font-size: 16px;
    font-weight: 600;
  }
  .font{
    margin-right: 5px;
    color: #90A0C2;
  }
  .add{
    color: #90A0C2;
    font-weight: 100;
  }
  .img{
    margin-top: 40px;
  }
  .img p{
    margin-bottom: 0;
    font-size: 12px;
    color: #fff;
    text-align: center;
    margin-top: 8px;
  }
  .img span{
    font-size: 10px;
    color: #616F8E;
    display: flex;
    justify-content: center;
    text-align: center;
  }
  .box4{
    background: #00123A;
    height: 698px;
    border-radius: 32px;
    padding: 24px;
    width: 100%;
  }
  .vid{
    margin-top: 40px;
  }
  .vid h5{
    color: #fff;
    margin-top: 16px;
    margin-bottom: 24px;
    font-size: 16px;
  }
  .vid h6{
    color: #fff;
    font-size: 16px;
    margin-bottom: 0;
  }
  .cam{
    width: 100%;
    height: 233px;
    background: linear-gradient(rgba(0, 18, 58, 0.3),rgba(0, 18, 58, 0.3)), url('../assets/entrance.png');
    background-size: cover;
    border-radius: 32px;
    padding: 16px;
  }
  .cam2{
    width: 100%;
    height: 233px;
    background: linear-gradient(rgba(0, 18, 58, 0.3),rgba(0, 18, 58, 0.3)), url('../assets/backyard.png');
    background-size: cover;
    border-radius: 32px;
    padding: 16px;
  }
  .live{
    display: flex;
    justify-content: flex-end;
    height: 24px;
    align-items: center;
  }
  .circle{
    height: 24px;
    display: flex;
    align-items: center;
    align-content: center;
    margin-right: 4px;
  }
</style>