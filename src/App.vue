<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="" @click="onClickHandle">点击按钮</div>
    <div>显示HelloWorld组件的内容</div>
    <HelloWorld v-if="isShow" msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
const HelloWorld = () => import(/* webpackChunkName: "HelloWorld" */ './components/HelloWorld.vue')

export default {
  name: 'App',
  data() {
    return {
      isShow: false
    }
  },
  components: {
    HelloWorld
  },
  methods: {
    onClickHandle() {
      this.isShow = true
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
