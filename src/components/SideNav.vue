<template>
  <div class="w-56 bg-black h-full flex-none">
    <div class="p-6">
      <img src="/spotifyLogo.png" class="h-10" alt="spotify logo" style="filter: brightness(0) invert(1);">
    </div>
    <div class="mx-2 mb-5">
      <button v-for="page in pages" @click="setID = page.id; router.push(page.id)" :class="`w-full text-sm font-semibold rounded px-3 py-2 flex items-center justify-start ${setID === page.id ? 'bg-light text-white': 'text-lightest'}`">
        <component v-bind:is="page.icon" class="mr-3"/>
        <p>{{ page.name }}</p>
      </button>
    </div>
    <div class="mx-5">
      <h1 class="mb-3 text-xs text-lightest tracking-widest uppercase">
        Playlists
      </h1>
      <button class="flex items-center justify-start opacity-75 hover:opacity-100 mb-2">
        <img src="/addNew.png" alt="add new" class="h-8 w-8 mr-3">
        <p class="text-sm text-white font-semibold">Criar Playlist</p>
      </button>
      <button class="flex items-center justify-start opacity-75 hover:opacity-100 mb-2">
        <img src="/favorites.png" alt="add new" class="h-8 w-8 mr-3">
        <p class="text-sm text-white font-semibold">Músicas Curtidas</p>
      </button>
      <div class="h-px w-full bg-light my-3"></div>
      <div class="w-full h-14 overflow-y-scroll">
        <p v-for="album in albums" class="text-lightest hover:text-white text-xs py-0.5">{{ album.name }}</p>
      </div>
      <button class="flex items-center justify-start text-lightest hover:text-white py-5">
        <DownloadIcon class="mr-3"/>
        <p class="text-sm font-semibold">Instalar App</p>
      </button>
      <img src="/playing.png" alt="playing" class="hide"/>
    </div>
  </div>
</template>

<script setup>
import { ref, shallowRef } from 'vue';

import HomeIcon from '@/components/icons/Home.vue'
import SearchIcon from '@/components/icons/Search.vue'
import BarChartIcon from '@/components/icons/ChartBar.vue'
import DownloadIcon from '@/components/icons/Download.vue'
import { useRouter } from 'vue-router'

const pages = shallowRef([
  {id: 'home', name: 'Início', icon: HomeIcon},
  {id: 'search', name: 'Buscar', icon: SearchIcon},
  {id: 'library', name: 'Sua Biblioteca', icon: BarChartIcon}
])

const setID = ref('home')

const albums = ref([
  {name: 'drive'},
  {name: 'zhu'},
  {name: 'All New Indie'},
  {name: 'Mellow'},
  {name: 'Classic Road Trip Songs'},
  {name: 'Lana Del Rey Radio'},
])

const router = useRouter()

</script>

<style scoped>
@media (max-height:750px) {
  .hide {
    display: none;
  }
}
</style>