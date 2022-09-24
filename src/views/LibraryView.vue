<template>
  <div class="px-6 py-3">
    <div class="flex items-center justify-between">
      <h1 class="pl-2 text-2xl font-semibold text-white tracking-wider">Sua biblioteca</h1>
    </div>
    <div class="w-full flex flex-wrap">
      <div v-for="custom in customs" class="p-2 w-48 relative">
        <div class="absolute w-full h-full flex items-end justify-end p-8 opacity-0 hover:opacity-100 transition ease-in delay-100 mt-1.5">
          <div class="bg-green rounded-full h-10 w-10 flex items-center justify-center hover:cursor-pointer">
            <PlayIcon class="text-white text-2xl pl-0.5"/>
          </div>
        </div>
        <div class="bg-light w-full h-auto p-5 rounded-lg shadow">
          <img :src="custom.src" alt="" class="w-auto w-full shadow mb-2">
          <h1 class="text-sm font-semibold text-white tracking-wide">{{ custom.title }}</h1>
          <h2 class="text-xs text-lightest tracking-wide pb-5">{{ custom.artist }}</h2>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script setup>
import { ref } from 'vue';
import PlayIcon from '@/components/icons/Play.vue'

const customs = ref([
  {src: 'billie.png', title: 'Billie Eilish Radio', artist: 'Billie Eilish'},
  {src: 'dailymix3.png', title: 'Daily Mix 3', artist: 'Por Spotify'},
  {src: 'dailymix4.png', title: 'Daily Mix 4', artist: 'Por Spotify'},
  {src: 'dailymix5.png', title: 'Daily Mix 5', artist: 'Por Spotify'},
])


</script>