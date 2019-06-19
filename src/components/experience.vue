<template>
  <div class="expcontent">
    <img src="../assets/exp.jpeg" :style="{height:expHeight}">
    <div class="midcontent">
      <span class="myexperience">My Experience</span>
      <div class="exp-container animated flipInX">
        <div class="line">
          <img :src="imgsrc" @mouseenter="changeimg" @mouseleave="recover" :class="inAndOut">
          <div class="exp-point">
            <div class="point-content">
              <div class="point"></div>
              <div class="timePoint1">
                <span>June, 2018</span>
                <div class="exp-desc">
                  <h4>Tickitin Experience LLC</h4>
                  <p style="color: green;">Front-end Developer, UI Designer</p>
                  <h6>Proven track recrd of being part of the successful delivery of projects
                    across the entire web application life cycle: concept, design, build, deploy, test, launch and maintain.
                    Finally helped Tickitin Gain traction and proceed to a higher funding stage.</h6>
                </div>
              </div>
            </div>
            <div class="point-content" style="top: 20px">
              <div class="point"></div>
              <div class="timePoint1">
                <span>Mar, 2017</span>
                <div class="exp-desc">
                  <h4>EBay</h4>
                  <p style="color: green;">Online Merchant</p>
                  <h6>I source and photograph items, post, and optimize listings for Search engine optimization,
                    ship item domestically, and internationally, handle customer service issue,
                    manage inventory, hire help and promote listings through various social media platform.</h6>
                </div>
              </div>
            </div>
            <div class="point-content" style="top: 40px">
              <div class="point"></div>
              <div class="timePoint1">
                <span>Feb, 2017</span>
                <div class="exp-desc">
                  <h4>Brooklyn College</h4>
                  <p style="color: green;">Bachelor's Degree in Computer Science</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'experience',
  props: ['expHeight'],
  data () {
    return {
      imgsrc: './static/img/t-n.png',
      inAndOut: ''
    }
  },
  methods: {
    changeimg () {
      this.inAndOut = 'inRotate'
      var that = this
      setTimeout(function () {
        that.imgsrc = './static/img/t-2.jpeg'
      }, 100)
    },
    recover () {
      this.inAndOut = 'outRotate'
      var that = this
      setTimeout(function () {
        that.imgsrc = './static/img/t-n.png'
      }, 100)
    }
  }
}
</script>
<style scoped>
.expcontent {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
.expcontent img {
  width: 100%;
  position: absolute;
}
.myexperience {
  position: relative;
  top: -50px;
  color: aliceblue;
  font-size: 30px;
  background-color: rgba(129, 129, 129, 0.5);
  cursor: pointer;
}
.midcontent {
  width: 80%;
  height: 70%;
  text-align: center;
}
.exp-container {
  position: relative;
  top: -50px;
  width: 100%;
  height: 100%;
  text-align: initial;
}
.inRotate {
  box-shadow: 0 0 32px rgb(128, 128, 128);
  animation:inRotate 0.2s;
}
.outRotate {
  box-shadow: 0 0 32px rgb(128, 128, 128, 0);
  animation: outRotate 0.2s;
}
@keyframes inRotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
@keyframes outRotate {
  from {
    transform: rotate(360deg);
  }
  to {
    transform: rotate(0deg);
  }
}
.line {
  position: relative;
  top: 20%;
  left: 26%;
  width: 10px;
  height: 80%;
  background-color: rgba(104, 104, 104, 0.699);
}
.line img {
  width: 120px;
  height: 120px;
  position: relative;
  top: -120px;
  left: -55px;
  border-radius: 50%;
  border: 10px solid rgba(129, 129, 129, 0.5);
}
.exp-point {
  position: absolute;
  top: 10%;
  left: -12px;
  width: 35px;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.point-content {
  position: relative;
}
.point {
  margin: 0 auto;
  width: 25px;
  height: 25px;
  background-color: rgb(180, 180, 180);
  border-radius: 50%;
  cursor: pointer;
}
.point:hover {
  border: 5px solid white;
  box-shadow: 0 0 8px white;
  transition: all 0.3s linear;
}
.timePoint1 {
  position: relative;
  top: -15px;
  left: -130px;
  width: 150px;
  height: 5px;
  border-radius: 5px;
  background-color: rgba(165, 42, 42, 0.479);
}
span {
  margin-top: 10px;
  position: absolute;
  padding: 10px;
  font-family: Georgia, serif;
  font-size: 20px;
  background-color: rgba(180, 180, 180, 0.699);
  border-radius: 10px;
}
.exp-desc {
  font-family: Arial, Helvetica, sans-serif;
  position:relative;
  top: -40px;
  left: 250px;
  width: 800px;
  color: rgb(212, 212, 212);
  position: absolute;
  cursor: pointer;
  overflow: hidden;
  margin-top: 20px;
}
.exp-desc:hover {
  color: greenyellow;
  transition: all 1s;
}
.exp-desc h4 {
  padding: 0;
  margin: 0;
}
.exp-desc p {
  padding: 0;
  margin: 0;
  width: 80%;
}
.exp-desc h6 {
  padding: 0;
  margin: 0;
  width: 80%;
}
</style>
