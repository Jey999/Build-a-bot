<template>
  <div id="app">
    <main>
      <div class="home">
        <button @click="surprise()">surprise!</button>
      <rude style="visibility: collapse;" id="rude"/>
      <robot/>
    <HomePage />
    </div>
    </main>
  </div>
</template>

<script>
import HomePage from './home/HomePage.vue';
import robot from './components/robot.vue';
import rude from './components/hello.vue';

export default {
  name: 'App',
  components: {
    HomePage,
    robot,
    rude,
  },
  methods: {
    surprise() {
      if (document.getElementById('rude').style.visibility === 'collapse') {
        document.getElementById('rude').setAttribute('style', 'visibility:visible');
      } else if (document.getElementById('rude').style.visibility === 'visible') {
        document.getElementById('rude').setAttribute('style', 'visibility:collapse');
      }
    },
  },
};
</script>

<style>
body {
  background: linear-gradient(to bottom, #555, #999);
  background-attachment: fixed;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
main {
  margin: 0 auto;
  padding: 30px;
  background-color: white;
  width: 1024px;
  min-height:300px;
}
.home {
  text-align: center;
}
</style>
