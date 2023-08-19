
<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  message: {
    type: String,
    required: true,
  },
});
const emitMessage = () => {
  const message = 'Hello from the child component!';
  emit('messageEmitted', message);
};

const emit = defineEmits(['inFocus', 'submit'])



</script>

<template>
  <div class="p-4 border rounded shadow">
    <h2 class="text-lg font-semibold">Child Component</h2>
    <p class="mt-2">{{ message }}</p>
    <button class="mt-4 bg-blue-500 text-white py-2 px-4 rounded" @click="emitMessage">Emit Message</button>
  </div>
</template>

<style scoped>

</style>

