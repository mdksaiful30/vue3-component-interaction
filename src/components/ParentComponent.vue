<script setup>
import ChildComponent from './ChildComponent.vue';
import { ref } from 'vue';

defineProps({
  message: String,
});
// defineEmits(['messageEmitted']);

const message = ref('');
const receivedMessage = ref('');

const handleMessageEmitted = (message) => {
  receivedMessage.value = message;
};
</script>

<template>
  <div class="p-4">
    <h1 class="text-2xl font-bold mb-4">Parent Component</h1>
    <ChildComponent :message="message" @messageEmitted="handleMessageEmitted" />
    <p class="mt-4">Received message from ChildComponent: <span class="bg-fuchsia-600 text-red-50">{{ receivedMessage }}</span></p>
  </div>
</template>

<style scoped>

</style>



