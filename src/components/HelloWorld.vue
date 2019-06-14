<template>
<!-- template 里面只能有一个element, 比如说这里只有一个div(也可以是font,header...) -->
  <div class="hello">
    <!-- 这里的msg是parent（App.vue）里定义的信息 -->
    <h1>{{ msg }}</h1>
    <p>{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: function () {
    return {
      content: "This is our first Vue APP using Vue CLI"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
