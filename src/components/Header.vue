<template>
  <div class="w-full sticky top-0 py-4 px-6 flex items-center justify-between bg-dark">
    <div class="flex items-center">
      <button class="rounded-full bg-black w-8 h-8 text-white pl-0.5 mr-3">
        <BackArrowIcon/>
      </button>
      <button class="rounded-full bg-black w-8 h-8 text-white pl-1.5">
        <NextArrowIcon/>
      </button>
    </div>
    <div class="relative">
      <button @click="showDropdown = !showDropdown" class="bg-light rounded-full py-1 px-2 flex items-center">
        <img src="/userIcon.png" alt="my face" class="rounded-full h-6 w-6 mr-2"/>
        <p class="text-white font-semibold text-xs mr-3">Pedro Motta</p>
        <div v-if="showDropdown === false">
          <DownArrowIcon class="text-white"/>
        </div>
        <div v-else>
          <UpArrowIcon class="text-white"/>
        </div>
      </button>
      <div v-if="showDropdown === true" class="absolute bg-light w-full rounded mt-1">
        <button @click="showDropdown = false" class="w-full py-2 text-sm text-lightest text-white border-b border-white opacity-75 hover:opacity-100">Conta</button>
        <button @click="showDropdown = false" class="w-full py-2 text-sm text-lightest hover text-white border-b border-light opacity-75 hover:opacity-100">Sair</button>
      </div>
    </div>
  </div>
</template>

<script setup>
import BackArrowIcon from '@/components/icons/LeftArrow.vue'
import NextArrowIcon from '@/components/icons/RightArrow.vue'
import DownArrowIcon from '@/components/icons/DownArrow.vue'
import UpArrowIcon from '@/components/icons/UpArrow.vue'
import { ref } from 'vue'

const showDropdown = ref(false)
</script>