<template>
  <div class="backdrop" @click.self="closePopUp">
    <div class="popup">
      <h1>Today is {{ currentDate() }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}.${
        current.getMonth() + 1
      }.${current.getFullYear()}`;
      return date;
    },
    closePopUp() {
      this.$emit("close");
    },
  },
};
</script>

<style>
.popup {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  position: absolute;
  background: rgba(0, 0, 0, 0.3);
  width: 100%;
  height: 100%;
}
.popup h1 {
  color: rgb(20, 220, 137);
}
</style>
