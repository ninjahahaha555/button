<template>
  <div id="app">
    <hr noshade="noshade" width="400" size="6">
    <HelloWorld msg="Comment Me" />
    <hr noshade="noshade" width="400" size="6">
    <div class="row">
      <div class="col-6">
        <img alt="Vue logo" src="./assets/earthtwo.jpg" class="bd-placeholder-img img-fluid" width="350" height="350"/>
        <h1>{{total1}}</h1>
        <CSButton @cc="sum" />
      </div>
      <div class="col-6">
        <img alt="Vue logo" src="./assets/earthsakura.jpg"  class="bd-placeholder-img img-fluid" width="350" height="350"/>
        <h1>{{total2}}</h1>
        <CSButton @cc="sum1" />
      </div>    
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import CSButton from "./components/CsButton";

export default {
  name: "App",
  components: {
    HelloWorld,
    CSButton,
  },

  data: function () {
    return {
      total1: 0,
      total2: 0,
    };
  },

  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },
    sum1(counterValue) {
      this.total2 = counterValue;
    },
  },
};
</script>

<style>
body{
  background-image: url("./assets/b6.jpg");
  background-attachment:fixed;
  background-repeat : no-repeat;
  background-position: 50% 0%;
}
#app {
  font-family: 'Russo One', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
