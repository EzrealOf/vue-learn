<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from './components/HelloWorld.vue'
export default {
  data() {
    return {
      num: 0,
      uname: "张三",
      msg: "<h2>标题</h2>",
      id: "d1",
      url: "https://miaosha.jd.com/#100007963995",
    };
  },
  methods: {
    changeUname: function () {
      this.uname = "李四";
    },
    changeColor: function () {
      this.id = "d2";
    },
  },
};
</script>

<template>
  <div>
    <p>{{ num }}</p>
    <p>{{ uname }}</p>
    <p v-once>{{ uname }}</p>
    <button @click="changeUname">changeUname</button>
    <p>{{ msg }}</p>
    <p v-html="msg"></p>
    <p v-bind:id="id">v-bind</p>
    <img v-bind:src="url" />
    <button @click="changeColor">改变颜色</button>
    <button @click="id = 'd1'">改变颜色</button>
    <p>
      {{ uname.split("").reverse().join("") }}
    </p>

    <p v-bind:id ="id+1"> v-bind绑定</p>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#d1 {
  color: red;
}
#d2 {
  color: green;
}
</style>
