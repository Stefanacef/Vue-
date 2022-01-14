<template>
  <button class="show-date--btn">
    {{ isDate ? (!displayDate ? text : currentDate()) : currentTime() }}
  </button>
</template>

<script>
export default {
  props: ["displayDate", "text", "isDate"],
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}.${
        current.getMonth() + 1
      }.${current.getFullYear()}`;
      return date;
    },
    currentTime() {
      const current = new Date();
      const time = current.toLocaleTimeString();
      return time;
    },
  },
};
</script>

<style>
.show-date--btn {
  background: rgb(241, 124, 124);
  width: 300px;
  height: 50px;
  font-size: 20px;
  border: transparent;
}
</style>
