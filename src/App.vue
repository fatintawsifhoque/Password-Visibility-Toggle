<template>
  <div class="h-screen w-screen bg-fuchsia-200 flex justify-center items-center">
    <input :type="type" placeholder="Type your password" class="h-15 w-75 border rounded-lg pl-2" >
    <button @click="toggle"><i :class="icon" class="text-2xl relative right-20 cursor-pointer"></i></button>

    
    <div class="absolute bottom-6 text-center">
      <p class="text-gray-700 text-sm">Developed by</p>
      <a
        href="https://github.com/fatintawsifhoque"
        target="_blank"
        rel="noopener noreferrer"
        class="text-xl font-bold text-indigo-800 hover:text-indigo-600 transition"
      >
        Fatin Tawsif Hoque
      </a>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const type = ref('password')
const icon = ref('fa-solid fa-eye-slash')
const toggle = ()=>{
  if (type.value === 'password') {
    type.value = 'text'
      icon.value = 'fa-solid fa-eye'
  }
  else {
      type.value = 'password'
      icon.value = 'fa-solid fa-eye-slash'
    }
  }
</script>

<style scoped>
</style>