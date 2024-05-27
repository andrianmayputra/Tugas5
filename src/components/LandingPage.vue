<template>
  <q-page-container>
    <q-page>
      <navbar-component></navbar-component>
      <div id="home">
        <carousel-component></carousel-component>
      </div>
      <div id="products" class="q-pa-md row justify-around">
        <card-component
          v-for="(product, index) in products"
          :key="index"
          :image="product.image"
          :title="product.title"
          :price="product.price"
          class="q-mb-md"
        ></card-component>
      </div>
      <div id="contact" class="q-pa-md">
        <contact-form-component></contact-form-component>
      </div>
      <footer-component></footer-component>
    </q-page>
  </q-page-container>
</template>

<script>
import NavbarComponent from './NavbarComponent.vue';
import CarouselComponent from './CarouselComponent.vue';
import CardComponent from './CardComponent.vue';
import FooterComponent from './FooterComponent.vue';
import ContactFormComponent from './ContactFormComponent.vue';

export default {
  name: 'LandingPage',
  components: {
    NavbarComponent,
    CarouselComponent,
    CardComponent,
    FooterComponent,
    ContactFormComponent,
  },
  data() {
    return {
      products: [
        {
          image: 'public/images/sepatufutsal1.jpeg',
          title: 'Futsal Shoes 1',
          price: 'Rp.499.000',
        },
        {
          image: 'public/images/sepatu.jpeg',
          title: 'Futsal Shoes 2',
          price: 'Rp.599.000',
        },
        {
          image: 'public/images/futsal.jpeg',
          title: 'Futsal Shoes 3',
          price: 'Rp.450.000',
        },
      ],
    };
  },
};
</script>

<style scoped>
.product-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 20px;
}
</style>
