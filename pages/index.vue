<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        y
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
      </div>
      <div>
        <el-button round>圆形按钮</el-button>
        <el-button type="primary" round>主要按钮</el-button>
        <el-button type="success" round>成功按钮</el-button>
        <el-button type="info" round>信息按钮</el-button>
        <el-button type="warning" round>警告按钮</el-button>
        <el-button type="danger" round>危险按钮</el-button>
      </div>
    </div>
    <input type="text" v-model="inputVal" placeholder="二维码"/>
    <div id="qrcode"></div>
    <input type="button" @click="getqrcode" value="得到二维码"/>
  </section>
</template>

<script>

import Logo from '~/components/Logo.vue'
// import QRCode from 'qrcodejs2'
export default {
  data () {
    return {
      inputVal: ''
    }
  },
  components: {
    Logo
  },
  methods: {
    getqrcode () {
    //   console.log('我是输入框的值' + this.inputVal)
    //   let qrcode = new QRCode(document.getElementById('qrcode'), {
    //     width: 350,
    //     height: 350
    //   })
    //   qrcode.makeCode(this.inputVal)
    // }
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
#qrcode{
  width: 200px;
  height: 200px;
  border: 1px solid red
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
