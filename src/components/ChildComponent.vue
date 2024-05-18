<template>
  <div class="child">
    <h2>Child Component</h2>
    <grand-child-component @grand-child-data="handleGrandChildData"></grand-child-component>
    <button @click="emitData" class="emit-button">Send Data to Parent</button>
    <slot :childMessage="childMessage"></slot>
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  name: 'ChildComponent',
  components: {
    GrandChildComponent,
  },
  data() {
    return {
      childMessage: 'Hello from Child Component',
    };
  },
  methods: {
    emitData() {
      this.$emit('child-data', 'Data from Child Component');
    },
    handleGrandChildData(data) {
      this.childMessage = data;
    },
  },
};
</script>

<style scoped>
.child {
  border: 2px solid #2196F3;
  padding: 20px;
  margin: 20px;
  text-align: center;
  border-radius: 10px;
  background-color: #e3f2fd;
}

.child h2 {
  color: #2196F3;
}

.emit-button {
  background-color: #2196F3;
  color: white;
  border: none;
  padding: 10px 20px;
  margin-top: 10px;
  cursor: pointer;
  border-radius: 5px;
}

.emit-button:hover {
  background-color: #1976D2;
}
</style>
