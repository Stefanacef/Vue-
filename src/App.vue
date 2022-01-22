<template>
  <div class="h-screen w-screen bg-gray-300 grid content-center justify-center">
    <button
      @click="updateTimeOnClick"
      class="text-xl bg-red-400 py-3 px-4 rounded cursor-pointer w-64 text-white"
    >
      {{ displayTime }}
    </button>
  </div>
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
    updateTimeOnClick() {
      const current = new Date();
      const time = current.toLocaleTimeString();
      this.displayTime = time;
    },
  },
};
</script>
