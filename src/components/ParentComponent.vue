<template>
  <div class="container">
    <h1>Daftar Menu</h1>
    <MenuList @tambahPesanan="tambahKePesanan" />

    <h2>Pesanan Anda:</h2>
    <ul class="pesanan-list">
      <li v-for="(item, index) in pesanan" :key="index">- {{ item }}</li>
    </ul>

    <SlotDisplay>
      <p>Tidak Pedas Yaaa bang.</p>
    </SlotDisplay>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import MenuList from './MenuList.vue'
import SlotDisplay from './SlotDisplay.vue'

const pesanan = ref([])

function tambahKePesanan(menu) {
  pesanan.value.push(menu)
}
</script>

<style scoped>
.container {
  max-width: 600px;
  margin: 20px auto;
  font-family: Arial, sans-serif;
  padding: 20px;
}

.pesanan-list {
  list-style-type: none;
  padding: 0;
  margin-top: 10px;
}
</style>
