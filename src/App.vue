<!--
 * @Date: 2023-06-08 14:21:18
 * @LastEditors: z_jw96 948226125@qq.com
 * @LastEditTime: 2023-06-08 19:08:38
 * @FilePath: /webapp/src/App.vue
-->
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import axios from 'axios';
export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  mounted() {
    axios.get('/api', { params: {} }).then((res) => {
      console.log(res);
    });
  },
};
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
