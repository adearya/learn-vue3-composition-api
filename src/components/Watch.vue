<script setup>
import { ref, watch } from "vue";

const counter = ref(0);

const add = () => {
  counter.value++;
};

watch(counter, (after, before) => {
  console.log(counter.value);
  console.log(after);
  console.log(before);
})

</script>

<template>
<h1>Counter</h1>
<p>Counter {{ counter }}</p>
<button @click="add">Add</button>
</template>