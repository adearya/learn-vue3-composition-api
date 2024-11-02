<script setup>
defineProps({
  label: {
    type: String,
    default: "",
  },

  user: {
    type: Object,
    default: () => ({ name: '' })
  },

  changeName: {
    type: Function,
    required: true
  }
});
</script>

<template>
  <p>{{ label }} dari {{ user.name }}</p>
  <button @click="changeName">Change</button>
</template>