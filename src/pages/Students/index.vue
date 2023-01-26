<script setup>
function register() {
  console.log();
}
</script>
<template>
  <form @submit="register">
    <input name="phone" placeholder="Phone" type="number" />
    <input name="name" placeholder="Name" type="text" />
    <input name="passport" placeholder="Passport" type="text" />
    <input name="pinfl" placeholder="PINFL" type="number" />
    <input name="birth" placeholder="Birth date" type="date" />
    <button type="submit">Register</button>
  </form>
</template>
<style></style>
