<template>
  <div class="parent">
    <h1>Parent Component</h1>
    <child-component @child-data="handleChildData">
      <template v-slot:default="slotProps">
        <p class="slot-message">Data from Child: {{ slotProps.childMessage }}</p>
      </template>
    </child-component>
    <p v-if="parentMessage" class="parent-message">Message from Child: {{ parentMessage }}</p>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  name: 'ParentComponent',
  components: {
    ChildComponent,
  },
  data() {
    return {
      parentMessage: '',
    };
  },
  methods: {
    handleChildData(data) {
      this.parentMessage = data;
    },
  },
};
</script>

<style scoped>
.parent {
  border: 2px solid #4CAF50;
  padding: 20px;
  margin: 20px;
  text-align: center;
  border-radius: 10px;
  background-color: #f0f9f0;
}

.parent h1 {
  color: #4CAF50;
}

.parent-message {
  color: #d32f2f;
  font-weight: bold;
}

.slot-message {
  color: #2196F3;
  font-style: italic;
}
</style>
