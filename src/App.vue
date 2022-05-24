<template>
  <div class="">
    <Botones />
  </div>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import Botones from "./components/Botones";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
    Botones,
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
