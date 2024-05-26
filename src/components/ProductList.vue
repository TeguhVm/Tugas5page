<template>
    <div class="q-pa-md">
      <h1 class="text-h5">Daftar Produk</h1>
      <q-card v-for="(product, index) in products" :key="index" class="q-mb-md">
        <q-card-section>
          <q-item>
            <q-item-section>
              <img :src="product.image" alt="Product" class="product-image" />
            </q-item-section>
            <q-item-section>
              <q-card-title>{{ product.name }}</q-card-title>
              <q-card-text>{{ product.description }}</q-card-text>
              <q-card-text class="text-primary">{{ product.price }}</q-card-text>
              <q-btn @click="$emit('add-to-cart', product)" color="primary" label="Add to Cart" />
            </q-item-section>
          </q-item>
        </q-card-section>
      </q-card>
      <q-btn @click="addProduct" color="primary" label="Add Product" />
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductList',
    data() {
      return {
        products: [
          {
            name: 'Nike Sport',
            description: 'Flexibel,Tahan Api',
            price: 'Rp.1.000.000,00',
            image: 'https://i.pinimg.com/564x/ce/39/8f/ce398f1f238d57ac4946350de23e773f.jpg'
          },
          {
            name: 'Topi Gucci',
            description: 'Pelindung Sinar UV.',
            price: 'Rp.500.000,00',
            image: 'https://i.pinimg.com/564x/83/46/65/8346652b555cb14c01d263d5fed06d06.jpg'
          },
          {
            name: 'Sauvage Dior',
            description: 'Parfum Pemikat.',
            price: 'Rp.2.500.000,00',
            image: 'https://i.pinimg.com/564x/ec/b5/b1/ecb5b1adcb6e6064f70be01eb79c09b4.jpg'
          },
          {
            name: 'Sweater LV',
            description: 'Hangat Melebihi Pelukannya.',
            price: 'Rp.5.000.000,00',
            image: 'https://i.pinimg.com/736x/f3/ce/ca/f3cecadc7eea4affe07eaf0df58216f2.jpg'
          },
          {
            name: 'Celana Jeans xp',
            description: 'Style Jalanan.',
            price: 'Rp.10.000.000,00',
            image: 'https://i.pinimg.com/736x/28/76/50/287650860f445393793887f6d9757849.jpg'
          }
        ]
      }
    },
    methods: {
      addProduct() {
        this.products.push({
          name: 'New Product',
          description: 'This is a new product.',
          price: '$100',
          image: 'https://via.placeholder.com/100x100.png?text=New+Product'
        });
      }
    }
  }
  </script>
  
  <style scoped>
  .product-image {
    width: 100px;
    height: 100px;
    object-fit: cover;
  }
  </style>
  