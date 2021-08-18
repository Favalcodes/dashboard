<template>
  <div id="left">
        <div class="overview">
          <h4 class="d-flex">Welcome Home, <span style="font-weight: 700">Hanna</span><Icons name="sun" /></h4>
          <p>Hope you had a great day at work today</p>
          <div class="down d-flex justify-content-between mt-4">
            <div class="temperature d-flex">
              <Icons name="drop" class="icon"/>
              <div class="text">
                <h5><strong>2&deg;C</strong></h5>
                <p>Temperature</p>
              </div>
            </div>
            <div class="temperature d-flex">
              <Icons name="thermo" class="icon"/>
              <div class="text">
                <h5><strong>48%</strong></h5>
                <p>Temperature</p>
              </div>
            </div>
          </div>
        </div>

        <b-row>
          <b-col col md="8">
            <div class="box">
              <div class="label d-flex">
                <h6>Power Consumption</h6>
                <span style="color: #90A0C2; font-weight: 100">Today <font-awesome-icon icon="caret-down"/></span>
              </div>
              <MyChart :height ="200" class="chart"/>
            </div>
          </b-col>
          <b-col>
            <div class="box">
              <h5 class="mb-4">Appliances</h5>
              <div class="icons">
                <div class="apply d-flex">
                  <Icons name="tv" class="icon"/>
                  <div class="text">
                    <h6>Television</h6>
                    <div class="form-check form-switch">
                      <input class="form-check-input" type="checkbox" id="flexSwitchCheckDefault" />
                    </div>
                  </div>
                </div>
                <div class="apply d-flex">
                  <Icons name="heater" class="icon"/>
                  <div class="text">
                    <h6>Heater</h6>
                    <div class="form-check form-switch">
                      <input class="form-check-input" type="checkbox" id="flexSwitchCheckDefault" checked/>
                    </div>
                  </div>
                </div>
                <div class="apply d-flex">
                  <Icons name="ice" class="icon"/>
                  <div class="text">
                    <h6>Air Condition</h6>
                    <div class="form-check form-switch">
                      <input class="form-check-input" type="checkbox" id="flexSwitchCheckDefault" />
                    </div>
                  </div>
                </div>
                <div class="apply d-flex">
                  <div class="icon">
                    <font-awesome-icon icon="lightbulb" class="bulb"/>
                  </div>
                  <div class="text">
                    <h6>Lights</h6>
                    <div class="form-check form-switch">
                      <input class="form-check-input" type="checkbox" id="flexSwitchCheckDefault" checked/>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </b-col>
        </b-row>
        <div class="box2">
          <div class="d-flex head">
            <Icons name="room" class="iconss" />
            <div class="text2 d-flex">
              <h5>Rooms</h5>
            </div>
          </div>
          <div class="carousel">
            <swiper ref="mySwiper" :options="swiperOption">
              <swiper-slide>
                <div class="slide1">
                  <div class="live">
                    <Icons name="live" class="circle"/>
                    <h6>Live</h6>
                  </div>
                </div>
                <p>Living Room</p>
              </swiper-slide>
              <swiper-slide>
                <div class="slide2">
                  <div class="faulty">
                    <h6>Camera Faulty</h6>
                  </div>
                </div>
                <p>Master Bedroom</p>
              </swiper-slide>
              <swiper-slide>
                <div class="slide3">
                  <div class="live">
                    <Icons name="live" class="circle"/>
                    <h6>Live</h6>
                  </div>
                </div>
                <p>Kitchen</p>
              </swiper-slide>
              <swiper-slide>
                <div class="slide4">
                  <div class="live">
                    <Icons name="live" class="circle"/>
                    <h6>Live</h6>
                  </div>
                </div>
                <p>Garage</p>
              </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
          </div>
        </div>
  </div>
</template>

<script>
import Icons from './Icons.vue'
import MyChart from './MyChart.vue'
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
    name: 'Left',
    components: {
      Icons,
      MyChart,
      Swiper,
      SwiperSlide
    },
    directives: {
      swiper: directive
    },
    data() {
      return {
        swiperOption: {
          slidesPerView: 3.1,
          spaceBetween: 50,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
          breakpoints: {
            1024: {
              slidesPerView: 3.1,
              spaceBetween: 0
            },
            768: {
              slidesPerView: 2.2,
              spaceBetween: 10
            },
            640: {
              slidesPerView: 2,
              spaceBetween: 5
            },
            320: {
              slidesPerView: 1.3,
              spaceBetween: 0
            }
          }
        }
      }
    }
}
</script>

<style>

  .overview{
    height: 235px;
    background: url('../assets/home.png');
    background-size: cover;
    background-repeat: no-repeat;
    padding: 40px;
    border-radius: 32px;
    margin-bottom: 32px;
  }
  .overview h4{
    font-size: 32px;
    align-items: center;
  }
  .overview p{
    font-size: 16px;
  }
  .down{
    width: 50%;
  }
  .icon{
    background: #5285F2;
    width: 48px;
    height: 48px;
    border-radius: 10px;
    text-align: center;
    padding: 10px;
    margin-right: 16px;
  }
  .iconss{
    background: #5285F2;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    text-align: center;
    padding: 7px 0;
    margin-right: 16px;
  }
  .down h5{
    font-size: 24px;
  }
  .text{
    line-height: 10px;
  }
  .text p{
    font-size: 14px;
  }
  .box{
    height: 317px;
    background: #00123A;
    border-radius: 32px;
    padding: 24px;
    color: #fff;
  }
  .chart{
    padding-top: 34px;
  }
  .label{
    justify-content: space-between;
    color: #fff;
  }
  .icons{
    height: 80%;
    overflow-y: scroll;
  }
  ::-webkit-scrollbar {
    width: 6px;
  }
  ::-webkit-scrollbar-track {
    background: #0D224D;
    border-radius: 5px; 
  }
  ::-webkit-scrollbar-thumb {
    background: #616F8E; 
    border-radius: 5px;
  }
  .apply{
    margin: 10px 0
  }
  .bulb{
    font-size: 24px;
  }
  .box2{
    background: #00123A;
    color: #fff;
    padding: 24px;
    height: 356px;
    border-radius: 32px;
    margin: 25px 0;
    width: 100%;
  }
  .head{
    height: auto;
  }
  .text2{
    justify-content: center;
    align-items: center;
  }
  .carousel{
    width: 100%;
    height: 200px;
    padding: 40px 0;
  }
  .slide1{
    background: linear-gradient(rgba(0, 18, 58, 0.3),rgba(0, 18, 58, 0.3)), url('../assets/living.png');
    height: 160px;
    width: 200px;
    border-radius: 32px;
    padding: 16px;
  }
  .slide2{
    background: linear-gradient(rgba(0, 18, 58, 0.8),rgba(0, 18, 58, 0.8)), url('../assets/bedroom.png');
    height: 160px;
    width: 200px;
    border-radius: 32px;
  }
  .slide3{
    background: linear-gradient(rgba(0, 18, 58, 0.3),rgba(0, 18, 58, 0.3)), url('../assets/kitchen.png');
    height: 160px;
    width: 200px;
    border-radius: 32px;
    padding: 16px;
  }
  .slide4{
    background: linear-gradient(rgba(0, 18, 58, 0.3),rgba(0, 18, 58, 0.3)), url('../assets/garage.jpg');
    background-size: cover;
    height: 160px;
    width: 200px;
    border-radius: 32px;
    padding: 16px;
  }
  .faulty{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
  }
  .carousel h6{
    margin-bottom: 0;
  }
  .carousel img{
    width: 200px;
    height: 160px;
    border-radius: 32px;
    position: relative;
  }
  .carousel p{
    margin-bottom: 0;
    margin-top: 16px;
    font-size: 16px;
    position: relative;
  }
  .carousel .swiper-pagination{
    position: relative;
    margin-top: 24px;
    margin-bottom: 24px;
  }
</style>