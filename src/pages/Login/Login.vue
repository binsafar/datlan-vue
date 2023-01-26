<script setup>
let showPassword = false;
let username = "";
let password = "";

function login() {
  if (username === "admin" && password === "admin") {
    console.log(username, password);
  } else return true;
}

const changePass = () => {
  showPassword = !showPassword;
  console.log(showPassword);
};
</script>

<template>
  <form @submit.prevent="login">
    <input
      v-model="username"
      name="username"
      type="text"
      placeholder="Username"
    />
    <div @click="changePass">
      <img src="../../assets/icons/eye.svg" />
    </div>
    <input
      v-model="password"
      name="password"
      :type="showPassword ? 'text' : 'password'"
      placeholder="Password"
      on-error="login()"
    />
    <button type="submit">Log in</button>
  </form>
</template>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  width: 400px;
  padding: 16px 32px;
  border: 1px solid #333;
  border-radius: 8px;

  margin: auto;
  margin-top: 20%;
}
input {
  height: 32px;
  outline: none;
  border: none;
  padding-left: 4px;
  margin-bottom: 16px;
  border-bottom: 1px solid #333;
}
button {
  height: 32px;
  border: none;
}
</style>
