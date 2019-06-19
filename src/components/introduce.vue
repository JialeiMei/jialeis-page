<template>
  <div class="introcontent">
    <div class="bg2-img"><img src="../assets/about.jpeg" :style="{height:introHeight}"></div>
    <div class="midcontent">
      <div class="card">
        <div class="card-body text-center animated flipInX">
          <h1 class="card-title"><img class="introimg" src="../assets/my.jpg"></h1>
          <br><br>
          <h3 class="card-text">
            Hi, My name is Jialei Mei, a girl who loves coding and designing.
            I currently have more than one years of hands-on experience efficiently coding websites and applications
            using modern <span style="text-decoration: underline;">HTML5, CSS3 and JavaScript with Vue.js framework</span> and
            designing the UI/UX mockups using <span style="text-decoration: underline;">Photoshop, Axura RP, Sketch and Flinto</span>.

          </h3>
          <br>
          <h3 class="card-text">

            Building state-of-the-art, easy to use, user-friendly websites and applications is truly a passion of mine
            and I am confident I would be an excellent addition to your organization.

            In addition to my knowledge base, I actively seek out new technologies and stay up-to-date on industry trends and advancements.
            This has allowed me to stay ahead of the curve and deliver exceptional work to all of my employers,
            including those I've worked for on a project basis.

            I have been really enjoying the part of my work and
            I am especially interested in bringing the experience I have gained as well as my commitment to efficiency to your company.</h3>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'introduce',
  props: ['introHeight']
}
</script>
<style scoped>
.introcontent {
  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bg2-img {
  position: absolute;
  display: block;
  width: 100%;
  z-index: -1;
}
.bg2-img img{
  width: 100%;
}
.midcontent {
  width: 75%;
}
.card {
  border: none;
  border-radius: 20px;
  background-color: rgba(255, 255, 255, 0);
}
.introimg {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  animation: rotate 10s linear infinite;
}
@keyframes rotate {
  from{
    transform: rotate(0deg);
  }
  to{
    transform: rotate(359deg);
  }
}
.introimg:hover {
  box-shadow: 0 0 16px rgb(255, 102, 0);
}
.card-text {
  font-size: 16px;
  color: white;
  font-family: Arial, Helvetica, sans-serif;

  justify-content: center;

  margin: auto;
}
</style>
