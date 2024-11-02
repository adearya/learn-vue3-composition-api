<script setup>
import RefReactiveToRefs from './components/RefReactiveToRefs.vue'
import Methods from './components/Methods.vue'
import ComputedGetterSetter from './components/ComputedGetterSetter.vue'
import WatchEffect from './components/WatchEffect.vue';
import Watch from './components/Watch.vue';
import Props from './components/Props.vue';

import { ref, reactive } from "vue";

const label = ref("Biodata");
const user = reactive({
  name: "Ade Arya Bimantara"
});

const changeName = () => {
  user.name = "Joya Octaviana";
};
</script> 
 
<template> 
  <Props :label="label" :user="user" :changeName="changeName" /> 
</template>