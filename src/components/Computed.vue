<script setup>
import { ref, reactive, computed } from "vue";

const counter = ref(0);
const addNum = ref(0);

const add = () => {
  counter.value++;
};

const result = computed(() => {
  return counter.value + counter.value + addNum.value
});
</script>

<template>
<h1>Learn Computed</h1>

<p>Counter value = {{ counter }} and Even numbers = {{ result }}</p>

<button @click="add">Add Counter</button>
</template>