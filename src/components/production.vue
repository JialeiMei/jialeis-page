<template>
  <div class="procontent">
    <img src="../assets/work.jpeg" :style="{height:proHeight}">
    <div class="pro-slider animated flipInX">
      <span class="display-4 hh" style="display: flex; margin-left: 40px">Project</span>

      <div class="swiperbg">
        <swiper :options="swiperOption">
          <swiper-slide><img src="../assets/Nike.png"><span>Rebuild Nike Web Application</span></swiper-slide>
          <swiper-slide><img src="../assets/Desktop-HD.png"><span>Rebuild Netfilx Web Application</span></swiper-slide>

          <swiper-slide>
            <img src="../assets/walkthrough.gif"><span>User Walkthrough IOS Application</span>
          </swiper-slide>

          <swiper-slide>
            <img src="../assets/parallax.gif"><span>Parallax Web Application</span>
          </swiper-slide>

          <swiper-slide>
            <img src="../assets/wedding.gif"><span>Build Wedding Web Application</span>
          </swiper-slide>

        </swiper>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'production',
  props: ['proHeight'],
  data () {
    return {
      swiperOption: {
        effect: 'cube',
        cubeEffect: {
          slideShadows: true,
          shadow: true,
          shadowOffset: 120,
          shadowScale: 0.6
        },
        speed: 1000,
        loop: true,
        autoplay: {
          delay: 3000,
          disableOnInteraction: false
        }
      }
    }
  }
}
</script>
<style scoped>
.procontent {
  width: 100%;
  height: 100%;
  display: block;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
.pro-slider .hh {
  position: absolute;
  top: 0;
  left: 0;
  font-family: Georgia, serif;
  color: black;
  font-size: 40px;
  border-radius: 10px;
  background-color: rgba(180, 180, 180, 0.699);
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

}
.procontent img {
  position: absolute;
  z-index: -1;
  width: 100%;
}
.pro-slider {
  width: 60%;
  height: 80%;
  display: flex;
  justify-content: center;
  align-items: center;

}
.swiperbg {
  height: 70%;
  width: 75%;
}
.swiper {
  width: 100%;
  height: 100%;
}
.swiper-slide img{
  height: 100%;
  width: 100%;
}
span {
  position: absolute;
  top: 100%;
  left: 30%;
  padding: 20px;
  color: rgba(153, 153, 153, 0.699);
}
</style>
