<template>
  <div id="app">
    <el-button type="primary" @click="openDiag = true">Welcome</el-button>
    <el-dialog :visible.sync="openDiag">
      <HelloWorld msg="My frist App" />
      <!-- 添加props步骤1 v-blind和设定名称，然后在data里设定初始值，-->
    <div>
      <input type="text" v-model="sendTreat">
    </div>
    <!-- // 添加component步骤4: 在 template 里添加 -->
    <!-- 添加props步骤2 v-blind和设定名称，然后在data里设定初始值，-->
    <Lixie :treat="sendTreat"/>
    </el-dialog> 
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
// 步骤1: 在components文件夹里新建文件，文件名第一个字母必须大写，如LiFristVue.vue。
// 步骤2: 在 script 里 import 文件，可以定义为任何名称,如：import Lixie from "./components/LiFristVue.vue";。
import Lixie from "./components/LiFristVue.vue";
// 步骤3: 在 export default 的 components里添加，名称与import的名称一致
export default {
  name: "app",
  components: {
    HelloWorld,
    Lixie
  },
  data: function() {
    return {
      // 添加props 步骤3:设定data, 然后在child component里接收
      sendTreat: "Raw Hide",
      openDiag: false,
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
