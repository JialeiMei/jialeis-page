<template>
  <div class="bottomcontent">
    <img src="../assets/last.jpeg" :style="{height:bottHeight}">
    <div class="midcontent animated flipInX">

      <div class="content text-center">
        <h1 class="myh1 shake-opacity shake-constant"><span style="color: white">CONTACT</span> ME</h1>

        <div class="line"></div>
        <h4 class="myh4">If you like my work and have some cool project to work on, just send me direct message or contact me through social sites listed below</h4>
        <div class="line"></div>
        <div class="myconnect">
          <a href="https://github.com/JialeiMei" target="_blank" class="iconfont" id="github" data-toggle="tooltip" data-placement="bottom" :title="github">&#xe709;</a>
          <a href="https://www.linkedin.com/in/jialeimei/" class="iconfont" id="linkedin" data-toggle="tooltip" data-placement="bottom" :title="linkedin" data-html="true">&#xe65c;</a>
          <a href="https://www.facebook.com/kelly.mei.12" class="iconfont" id="facebook" data-toggle="tooltip" data-placement="bottom" :title="facebook" data-html="true">&#xe6d9;</a>
          <a href="https://www.instagram.com/kellymeiii/" target="_blank" class="iconfont" id="instagram" data-toggle="tooltip" data-placement="bottom" :title="instagram">&#xe664;</a>
          <a href="https://dribbble.com/kellymeiii" target="_blank" class="iconfont" id="dribbble" data-toggle="tooltip" data-placement="bottom" :title="dribbble">&#xe70a;</a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'bottomotherthing',
  props: ['bottHeight'],
  data () {
    return {
      github: 'Github',
      facebook: 'facebook',
      linkedin: 'linkedin',
      dribbble: 'dribbble',
      instagram: 'instagram'
    }
  }
}
</script>
<style scoped>
.bottomcontent {
  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bottomcontent img {
  width: 100%;
  position: absolute;
  z-index: -1;
}
.midcontent {
  width: 480px;
  height: 380px;
}
.mytopborder {
  position: relative;
  left: 230px;
  width: 250px;
  height: 150px;
  border-top: 10px solid rgba(255, 116, 36, 0.808);
  border-right: 10px solid rgba(255, 116, 36, 0.808);
}
.mybottomborder {
  position: relative;
  top: 35%;
  width: 100%;
  height: 100px;
  border: 10px solid rgba(255, 116, 36, 0.808);
  border-top: none;
}
.content {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  height: 80%;
  color: black;
}

.line {
  width: 100%;
  height: 5px;
  background: linear-gradient(to right, #EEF1EF ,#000000, #000000, #EEF1EF);
}
.myh4 {
  font-size: 25px;
  padding: 0 39px;
  padding-top: 15px;
  font-family: Arial, Helvetica, sans-serif;

}
.myh1 {
  padding: 0;
  margin: 0;
  font-family: Georgia, serif;
  font-size: 60px;
}
.myconnect {
  width: 110%;
  position: relative;
  right: 48px;
}
a {
  text-decoration: none;
  color: black;
}
.iconfont {
  margin-left: 50px;
  font-size: 40px;
  cursor: pointer;
}
.myconnect a:nth-child(1):hover {
  color: rgb(65, 65, 65);
}
.myconnect a:nth-child(2):hover {
  color: rgb(13, 161, 0);
}
.myconnect a:nth-child(3):hover {
  color: rgb(0, 132, 255);
}
.myconnect a:nth-child(4):hover {
  color: rgb(118, 0, 165);
}
.myconnect a:nth-child(5):hover {
  color: rgb(197, 13, 0);
}
</style>
