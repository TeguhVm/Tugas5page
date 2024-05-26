<template>
    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="$emit('toggle-left-drawer')" />
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          Toko-Online-TeguhVm
        </q-toolbar-title>
        <q-btn dense flat round icon="shopping_cart" @click="$emit('toggle-cart')" />
      </q-toolbar>
      <q-tabs align="left">
        <q-route-tab to="/page1" label="Page One" />
        <q-route-tab to="/page2" label="Page Two" />
        <q-route-tab to="/page3" label="Page Three" />
      </q-tabs>
    </q-header>
  </template>
  
  <script>
  export default {
    name: 'Header',
  }
  </script>
  