<template>
  <div class="px-6 py-3">
    <div class="flex items-center justify-between">
      <h1 class="pl-2 text-2xl font-semibold text-white tracking-wider">Faça sua busca aqui...</h1>
    </div>
    <form @submit="onSubmit" class="mt-5">   
      <label for="default-search" class="mb-2 text-sm font-medium text-gray-300 sr-only">Search</label>
      <div class="relative">
          <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
              <svg aria-hidden="true" class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg>
          </div>
          <input type="search" id="default-search" class="block p-4 pl-10 w-full text-sm text-white bg-light rounded-lg border border-gray-600 focus:ring-green focus:border-green placeholder-gray-400" placeholder="Busque Músicas, Artistas..." required>
          <button type="submit" class="text-white absolute right-2.5 bottom-2.5 bg-green hover:bg-lightest focus:ring-4 focus:outline-none focus:ring-green font-medium rounded-lg text-sm px-4 py-2 border-none">Buscar</button>
      </div>
    </form>
    <div v-if="busca" class="border border-blue-300 shadow rounded-md p-4 max-w-sm w-full mx-auto mt-5">
      <div class="animate-pulse flex space-x-4">
        <div class="rounded-full bg-slate-700 h-10 w-10"></div>
        <div class="flex-1 space-y-6 py-1">
          <div class="h-2 bg-slate-700 rounded"></div>
          <div class="space-y-3">
            <div class="grid grid-cols-3 gap-4">
              <div class="h-2 bg-slate-700 rounded col-span-2"></div>
              <div class="h-2 bg-slate-700 rounded col-span-1"></div>
            </div>
            <div class="h-2 bg-slate-700 rounded"></div>
          </div>
        </div>
      </div>
    </div>
    <h1 class="pl-2 text-2xl font-semibold text-white tracking-wider mt-5 flex justify-center">
      {{ msg }}
    </h1>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const busca = ref(false)
const msg = ref('')

function onSubmit(evt){
  evt.preventDefault()
  msg.value = ''
  busca.value = true
  setTimeout(() =>{
    busca.value = false
    msg.value = 'Nenhum resultado encontrado'
  }, 2000)
}

</script>