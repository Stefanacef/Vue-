<template>
  <button @click="updateTimeOnClick" class="show-time--btn">
    {{ displayTime }}
  </button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      displayTime: "Click me",
    };
  },
  methods: {
    currentTime() {
      const current = new Date();
      const time = current.toLocaleTimeString();
      this.displayTime = time;
    },
    updateTimeOnClick() {
      this.currentTime();
    },
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
  position: absolute;
  height: 100vh;
  width: 100vw;
  background: rgba(135, 136, 134, 0.384);
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.show-time--btn {
  background: rgb(241, 124, 124);
  width: 300px;
  height: 50px;
  font-size: 20px;
  border: transparent;
}
</style>
