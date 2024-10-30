<script setup>
import { ref, reactive, computed } from "vue";

const counter = ref(0);
const addNum = ref(0);

const add = () => {
  result.value = 10;
  counter.value++;
};

const result = computed({
  get: () => counter.value + addNum.value,
  set: (val) => (addNum.value = val),
});
</script>

<template>
<h1>Learn Computed</h1>

<p>Counter value = {{ counter }} and Even numbers = {{ result }}</p>

<button @click="add">Add Counter</button>
</template>