<template>
  <div id="app" :style="{height:myHeight}">
    <router-view :myHeight="myHeight"></router-view>
  </div>
</template>
<script>
import $ from 'jquery'
$(document).ready(function () {
  $('#github').tooltip()
  $('#facebook').tooltip()
  $('#linkedin').tooltip()
  $('#dribbble').tooltip()
  $('#instagram').tooltip()
  $('#pgithub').tooltip()
  $('#pfacebook').tooltip()
  $('#plinkedin').tooltip()
  $('#pdribbble').tooltip()
  $('#pinstagram').tooltip()
})
export default {
  name: 'App',
  data () {
    return {
      myHeight: document.documentElement.clientHeight + 'px'
    }
  },
  created () {
    try {
      setTimeout(function () {
        var loading = document.getElementById('loading')
        if (loading != null) {
          document.body.removeChild(loading)
        }
      }, 5000)
    } catch (e) {

    }
  },
  mounted () {
    const that = this
    window.onresize = () => {
      that.myHeight = `${document.documentElement.clientHeight}px`
    }
  }
}
</script>
<style>
html {
  overflow: hidden;
}
#app {
  width: 100%;
}
</style>
