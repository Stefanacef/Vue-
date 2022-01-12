<template>
  <button class="show-date--btn">
    {{ !displayDate ? text : currentDate() }}
  </button>
</template>

<script>
export default {
  props: ["displayDate", "text"],
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}.${
        current.getMonth() + 1
      }.${current.getFullYear()}`;
      return date;
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
