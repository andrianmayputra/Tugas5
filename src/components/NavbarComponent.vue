<template>
  <q-header elevated>
    <q-toolbar>
      <q-toolbar-title>
        FutsalStore
      </q-toolbar-title>

      <q-btn flat label="Home" @click="scrollTo('home')" />
      <q-btn flat label="Products" @click="scrollTo('products')" />
      <q-btn flat label="Contact" @click="scrollTo('contact')" />
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  name: 'NavbarComponent',
  methods: {
    scrollTo(section) {
      const element = document.getElementById(section);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>
  
  <style scoped>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
  }
  
  .navbar .logo {
    font-size: 24px;
    font-weight: bold;
  }
  
  .navbar .nav-links {
    list-style: none;
    display: flex;
  }
  
  .navbar .nav-links li {
    margin-left: 20px;
  }
  
  .navbar .nav-links a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }
  </style>
  