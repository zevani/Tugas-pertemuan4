<template>
    <div>
      <h1>Komponen Parent</h1>
      <p>Data dari GrandChild: {{ receivedData }}</p>
      <slot></slot>
      <ChildComponent @dataSent="handleData" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import ChildComponent from './ChildComponent.vue';
  
  const receivedData = ref('');
  
  const handleData = (data) => {
    receivedData.value = data;
  };
  </script>
  
  <style scoped>
  div {
    border: 1px solid #ddd;
    padding: 20px;
    margin: 20px;
  }
  </style>
  