<template>
    <q-drawer v-model="drawerOpen" side="right" bordered>
      <q-card>
        <q-card-section class="row items-center">
          <q-card-title class="text-h6">Daftar Pesanan</q-card-title>
          <q-btn flat dense round icon="close" class="self-end" @click="$emit('toggle-cart')" />
        </q-card-section>
        <q-list bordered separator>
          <q-item v-for="(item, index) in cart" :key="index">
            <q-item-section>{{ item.name }}</q-item-section>
            <q-item-section side class="text-right">{{ item.price }}</q-item-section>
          </q-item>
        </q-list>
      </q-card>
    </q-drawer>
  </template>
  
  <script>
  export default {
    name: 'Cart',
    props: {
      modelValue: Boolean,
      cart: Array
    },
    computed: {
      drawerOpen: {
        get() {
          return this.modelValue
        },
        set(val) {
          this.$emit('update:modelValue', val)
        }
      }
    }
  }
  </script>
  