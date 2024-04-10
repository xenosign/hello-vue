<template>
  <form action="" @submit.prevent="submitForm">
    <div>
      <label for="userId">ID : </label>
      <input id="userId" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">PASSWORD : </label>
      <input id="password" type="text" v-model="password" />
    </div>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
import axios from "axios";
import { ref } from "vue";

export default {
  setup() {
    let username = ref("");
    let password = ref("");

    const submitForm = () => {
      const data = {
        username: username.value,
        password: password.value,
      };
      axios
        .post("https://jsonplaceholder.typicode.com/users", data)
        .then((res) => {
          console.log(res);
        });
    };

    return { username, password, submitForm };
  },
};
</script>

<style scoped></style>
