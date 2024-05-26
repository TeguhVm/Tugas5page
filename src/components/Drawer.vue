<template>
    <q-drawer v-model="drawerOpen" show-if-above side="left" bordered>
      <!-- drawer content -->
    </q-drawer>
  </template>
  
  <script>
  export default {
    name: 'Drawer',
    props: {
      modelValue: Boolean
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
  