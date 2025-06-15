<template>
  <div>
    <MenuItem 
      v-for="item in daftarMenu" 
      :key="item" 
      :nama="item" 
      @pilihMenu="emitMenu"
    />
  </div>
</template>

<script setup>
import MenuItem from './MenuItem.vue'
import { defineEmits } from 'vue'

const daftarMenu = ['Nasi Goreng', 'Mie Ayam', 'Sate Ayam']
const emit = defineEmits(['tambahPesanan'])

function emitMenu(menu) {
  emit('tambahPesanan', menu)
}
</script>