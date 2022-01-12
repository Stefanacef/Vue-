<template>
  <Button @click="toggleDisplayDate" :displayDate="displayDate" :text="text" />
</template>

<script>
import Button from "./components/Button.vue";
export default {
  name: "App",
  components: { Button },
  data() {
    return {
      text: "Click me",
      displayDate: false,
    };
  },
  methods: {
    toggleDisplayDate() {
      this.displayDate = !this.displayDate;
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
  justify-content: center;
  align-items: center;
}
</style>
