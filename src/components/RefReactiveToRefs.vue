<script setup>
import { reactive, ref, toRefs } from "vue";

// ref untuk tipe data primitif
const message = ref("Halo dunia!");

// Berubah setelah 5 detik
setTimeout(() => {
  message.value = "Hai Ade!";
}, 5000)

// reactive untuk tipe data object
const user = reactive({
  name: "Arya",
  age: 23
})

// Berubah setelah 5 detik
setTimeout(() => {
  user.name = "Ade";
}, 5000)

// toRefs untuk mengubah reactive menjadi ref
const { name, age } = toRefs(user);
</script>

<template>
  <div>Pakai ref = {{ message }}</div>
  <div>Pakai reactive = Nama saya {{ user.name }} dan umur {{ user.age }}</div>
  <div>Pakai toRefs = Nama saya {{ name }} dan umur {{ age }}</div>
</template>
