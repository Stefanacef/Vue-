<template>
  <ShowCurrentDate v-if="displayCurrentDate" @close="togglePopUp" />
  <button class="showtime-btn" v-if="!displayCurrentDate" @click="togglePopUp">
    Click me
  </button>
</template>

<script>
import ShowCurrentDate from "./components/ShowCurrentDate.vue";
export default {
  name: "App",
  components: { ShowCurrentDate },
  data() {
    return {
      displayCurrentDate: false,
    };
  },
  methods: {
    togglePopUp() {
      this.displayCurrentDate = !this.displayCurrentDate;
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
  margin-top: 60px;
}
.showtime-btn {
  background: rgb(241, 124, 124);
  width: 300px;
  height: 50px;
  font-size: 20px;
  border: transparent;
}
</style>
