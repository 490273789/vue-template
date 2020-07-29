<!--
 * @Author: your name
 * @Date: 2020-07-28 19:08:20
 * @LastEditTime: 2020-07-29 13:57:33
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: /vue-template/src/views/Home.vue
-->
<template>
  <div class="home">
    <div id="mse"></div>
    <button @click="initPlayer">play</button>
  </div>
</template>

<script>
// @ is an alias to /src
import Player from 'xgplayer'
export default {
  name: 'Home',
  data() {
    return {
      player1: null
    }
  },
  methods: {
    initPlayer() {
      let id = document.querySelector('#mse')
      console.log(id)
      let player = new Player({
        id: 'mse',
        // url: "http://vcdn.e-eduspace.com/6c3c55c2bd834bca8663eac976f3d90c/6c3c55c2bd834bca8663eac976f3d90c.m3u8"
        url: 'http://7vil13.com2.z0.glb.qiniucdn.com/XSASP0534.mp4'
      })
      this.player1 = player
    }
  }
}
</script>
<style lang="scss" scope>
.home {
  width: 100%;
  height: 100%;
}
</style>
