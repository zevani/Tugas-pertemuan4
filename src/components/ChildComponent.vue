<template>
  <div>
    <h2>Komponen Anak</h2>
    <GrandChildComponent @dataSent="forwardData" />
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  components: {
    GrandChildComponent
  },
  methods: {
    forwardData(data) {
      this.$emit('dataSent', data);
    }
  }
}
</script>

<style scoped>
div {
  border: 1px solid #ddd;
  padding: 10px;
  margin: 10px;
}
</style>
