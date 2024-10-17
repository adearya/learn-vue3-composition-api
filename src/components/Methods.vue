<script setup>
import { ref } from 'vue';

const counter = ref(0);

const add = () => {
  counter.value++;
};
</script>

<template>
  <div>{{ counter }}</div>
  <button @click="add">Add</button>
</template>
