<template>
  <div class="grand-child">
    <h3>Grand Child Component</h3>
    <button @click="emitData" class="emit-button">Send Data to Child</button>
  </div>
</template>

<script>
export default {
  name: 'GrandChildComponent',
  methods: {
    emitData() {
      this.$emit('grand-child-data', 'Hello from Grand Child Component');
    },
  },
};
</script>

<style scoped>
.grand-child {
  border: 2px solid #f44336;
  padding: 20px;
  margin: 20px;
  text-align: center;
  border-radius: 10px;
  background-color: #ffebee;
}

.grand-child h3 {
  color: #f44336;
}

.emit-button {
  background-color: #f44336;
  color: white;
  border: none;
  padding: 10px 20px;
  margin-top: 10px;
  cursor: pointer;
  border-radius: 5px;
}

.emit-button:hover {
  background-color: #d32f2f;
}
</style>
