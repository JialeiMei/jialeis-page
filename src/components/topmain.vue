<template>
  <div class="topmaincontent">
    <div class="bg-imgs animated flipInX">
      <swiper :options="swiperOption">
        <swiper-slide><img src="../assets/1.1.jpg" :style="{height:topHeight}"></swiper-slide>
        <swiper-slide><img src="../assets/1.2.jpg" :style="{height:topHeight}"></swiper-slide>
        <swiper-slide><img src="../assets/1.3.jpg" :style="{height:topHeight}"></swiper-slide>
        <swiper-slide><img src="../assets/1.4.jpg" :style="{height:topHeight}"></swiper-slide>
      </swiper>
    </div>
    <div class="somecontent">
      <div class="mid-content">
        <div class="card" @mouseenter="addcardAnimate"  @mouseleave="delcardAnimate" :class="cardani">
          <div class="particles">
            <vue-particles
              color="#7DF031"
              :particleOpacity="0.5"
              linesColor="#D5D5D5"
              :particlesNumber="80"
              shapeType="circle"
              :particleSize="5"
              :linesWidth="2"
              :lineLinked="true"
              :lineOpacity="0.4"
              :linesDistance="2"
              :moveSpeed="3"
              :hoverEffect="true"
              hoverMode="grab"
              :clickEffect="true"
              clickMode="push"
            >
            </vue-particles>
          </div>
          <div class="card-body text-center animated flip">
            <h1 class="card-title display-5" style="font-family: Georgia, serif; color: black">Welcome To <strong> Jialei's </strong>Portfolio</h1>
            <h3 class="card-text" style="font-family: Arial, Helvetica, sans-serif; color: black">I design and code beautifully simple things, and I love waht I do</h3>
            <p>Brooklyn, NY, 11220</p>
            <p>kelly_mei712@hotmail.com</p>
            <p>(646)460-0568</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'topmain',
  props: ['topHeight'],
  data () {
    return {
      swiperOption: {
        speed: 1000,
        setWrapperSize: true,
        effect: 'flip',
        loop: true,
        touchRatio: 0,
        autoHeight: true,
        autoplay: {
          delay: 4000,
          disableOnInteraction: false,
          waitForTransition: false
        }
      },
      cardani: ''
    }
  },
  methods: {
    addcardAnimate () {
      this.cardani = 'heartBeat'
    },
    delcardAnimate () {
      this.cardani = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.topmaincontent {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.particles {
  position: absolute;
  overflow: hidden;
  width: 100%;
  height: 100%;
  z-index: 1;
}
.swiper-slide img {
  width: 100%;
}
.bg-imgs {
  position: relative;
  z-index: -1;
}
.somecontent {
  position: absolute;
  top: 0px;
  z-index: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.mid-content {
  width: 60%;
}
.card {
  border: none;
  border-radius: 20px;
  background-color: rgba(255, 255, 255, 0);
  color: rgb(187, 187, 187);
}
.card:hover {
  box-shadow: 8px 12px 50px rgba(0, 0, 0, 0.842);
}
.card p{
  color: rgb(255, 255, 255);
  font-size: 16px;
  line-height: 12px;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
