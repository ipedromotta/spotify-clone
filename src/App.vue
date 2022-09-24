<template>
  <div class="bg-dark h-screen">
    <div class="flex" style="height: 88vh;">
      <SideNav/>
      <!-- main content -->
      <div class="w-full h-full relative overflow-y-auto">
        <Header/>
        <RouterView />
      </div>
    </div>
    <PlayBar/>
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
import SideNav from '@/components/SideNav.vue'
import PlayBar from '@/components/PlayBar.vue'
import Header from '@/components/Header.vue'

</script>
