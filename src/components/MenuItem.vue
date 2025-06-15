<template>
  <div class="menu-card">
    <span>{{ nama }}</span>
    <button @click="pilih">Pilih</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  nama: String
})

const emit = defineEmits(['pilihMenu'])

function pilih() {
  emit('pilihMenu', props.nama)
}
</script>

<style scoped>
.menu-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 4px;
  margin-bottom: 8px;
}

button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
