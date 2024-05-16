<template>
  <div>
    <button @click="sendData">Kirim Data ke Child</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['dataSent']);

const sendData = () => {
  emit('dataSent', 'Ini data dari GrandChildComponent');
};
</script>

<style scoped>
button {
  margin: 10px;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}
</style>
