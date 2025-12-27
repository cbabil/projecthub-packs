<script setup lang="ts">
import { ref } from 'vue';

defineProps<{
  msg: string;
}>();

const count = ref(0);
</script>

<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
    <button type="button" @click="count++">Count is: {{ count }}</button>
    <p>Edit <code>components/HelloWorld.vue</code> to test HMR</p>
  </div>
</template>

<style scoped>
.hello {
  text-align: center;
}

button {
  font-size: 1rem;
  padding: 0.5rem 1rem;
  cursor: pointer;
}
</style>
