<template>
  <AppHeader v-bind:appTitle="msg" v-on:change="changeMsg" />
  <div>
    <h1>안녕하세요</h1>
    <h2>{{ msg }}</h2>
  </div>
  <button @click="showAlert">Alert!</button>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  components: {
    AppHeader,
  },
  data() {
    return {
      msg: "메세지 입니다.",
    };
  },
  methods: {
    showAlert() {
      alert("hi");
    },
    changeMsg() {
      this.msg = "변경 완료";
    },
  },
};
</script>

<style scoped></style>
