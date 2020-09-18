<template>
  <div id="app">
    <HelloWorld :title="title" :font_size="font_size" :image_url="image_url" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      title: "Menu12",
      font_size: 30,
      image_url: "http://1001goroskop.ru/img/gadanie/derevo_zh/_derevo.jpg",
    };
  },
};
</script>

<style lang="scss">
</style>
