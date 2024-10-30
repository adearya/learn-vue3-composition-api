<script setup>
import { ref, watchEffect } from "vue";

const counter = ref(0);

const add = () => {
  counter.value++;
};

watchEffect(() => {
  console.log(counter.value);
})

</script>

<template>
<h1>Counter</h1>
<p>Counter {{ counter }}</p>
<button @click="add">Add</button>
</template>