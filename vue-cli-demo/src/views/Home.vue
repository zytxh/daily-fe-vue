<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  },
  mounted() {
    window.history.pushState({name: 'home-pushstate'}, null, window.location.href);
    window.onpopstate = function(e) {
      console.log(e)
    }
  },
};
</script>
