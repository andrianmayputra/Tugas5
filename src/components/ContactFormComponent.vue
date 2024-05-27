<template>
    <q-page padding>
      <q-form @submit.prevent="submitForm" @reset="resetForm">
        <q-input v-model="name" label="Name" outlined required></q-input>
        <q-input v-model="email" label="Email" type="email" outlined required></q-input>
        <q-input v-model="message" label="Message" type="textarea" outlined required></q-input>
        
        <div class="q-mt-md">
          <q-btn label="Submit" type="submit" color="primary" />
          <q-btn label="Reset" type="reset" color="secondary" flat />
        </div>
      </q-form>
    </q-page>
  </template>
  
  <script>
  export default {
    name: 'ContactFormComponent',
    data() {
      return {
        name: '',
        email: '',
        message: '',
      };
    },
    methods: {
      submitForm() {
        if (this.name && this.email && this.message) {
          alert(`Thank you for your message, ${this.name}!`);
          this.resetForm();
        } else {
          alert('Please fill out all fields.');
        }
      },
      resetForm() {
        this.name = '';
        this.email = '';
        this.message = '';
      },
    },
  };
  </script>
  
  <style scoped>
  .q-form {
    max-width: 600px;
    margin: 0 auto;
  }
  
  .q-btn {
    margin-right: 10px;
  }
  </style>
  