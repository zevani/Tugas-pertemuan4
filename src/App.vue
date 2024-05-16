<template>
  <div id="app">
    <ParentComponent>
      <template v-slot>
        <h2>Ini adalah konten yang disisipkan melalui slot</h2>
      </template>
    </ParentComponent>
  </div>
</template>

<script setup>
import ParentComponent from './components/ParentComponent.vue';
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
