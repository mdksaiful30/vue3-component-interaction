<script setup>
import ParentComponent from './components/ParentComponent.vue';
import { defineComponent } from 'vue';

defineComponent({
  components: {
    ParentComponent,
  },
});


</script>
<template>
  <div class="min-h-screen flex items-center justify-center">
    <ParentComponent />
  </div>
</template>



<style scoped>

</style>
