<template>
  <h1>APP header</h1>
  <h2>{{ appTitle }}</h2>
  <button @click="changeTtile">변경</button>
</template>

<script>
export default {
  props: ["appTitle"],
  methods: {
    changeTtile() {
      this.$emit("change");
    },
  },
};
</script>

<style scoped></style>
