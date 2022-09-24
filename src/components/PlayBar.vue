<template>
  <div class="w-full flex items-center justify-between px-3 bg-light border-t border-dark" style="height: 12vh;">
    <div class="flex items-center">
      <div>
        <h1 class="text-sm text-white tracking-wide">
          Summer in the City - Remastered
        </h1>
        <h2 class="text-xs text-lightest tracking-wide">
          The Lovin' Spoonfull
        </h2>
      </div>
      <HeartIcon class="text-green mx-4 cursor-pointer"/>
      <ExpandIcon class="text-lightest hover:text-white cursor-pointer"/>
    </div>
    <div class="flex flex-col justify-center w-1/3 items-center">
      <div class="flex items-center">
        <ArrowLeftRight class="text-lightest hover:text-white mx-5 cursor-pointer"/>
        <BackwardIcon class="text-lightest hover:text-white cursor-pointer"/>
        <PlayCircleIcon class="text-lightest hover:text-white mx-5 cursor-pointer"/>
        <ForwardIcon class="text-lightest hover:text-white cursor-pointer"/>
        <ArrowRoundedIcon class="text-lightest hover:text-white mx-5 cursor-pointer"/>
      </div>
      <div class="w-full flex items-center mt-3">
        <p class="text-xs text-lightest mr-2">0:46</p>
        <div class="w-full h-1 bg-dark rounded-full flex items-center">
          <div class="h-1 rounded-full bg-green" style="width: 18%;"></div>
          <div class="h-3 w-3 bg-white rounded-full -ml-1 shadow cursor-pointer"></div>
        </div>
        <p class="text-xs text-lightest ml-2">2:58</p>
      </div>
    </div>
    <div class="flex items-center">
      <ListIcon class="text-lightest hover:text-white cursor-pointer"/>
      <DeviceIcon class="text-lightest mx-3 hover:text-white cursor-pointer"/>
      <VolumeIcon class="text-lightest hover:text-white cursor-pointer"/>
      <div class="w-20 bg-lightest rounded-full h-1 ml-1 hover:bg-white cursor-pointer"></div>
    </div>
  </div>
</template>

<script setup>
import HeartIcon from '@/components/icons/Heart.vue'
import ExpandIcon from '@/components/icons/Expand.vue'
import ListIcon from '@/components/icons/List.vue'
import DeviceIcon from '@/components/icons/Phone.vue'
import VolumeIcon from '@/components/icons/Volume.vue'
import ArrowRoundedIcon from '@/components/icons/ArrowRounded.vue'
import PlayCircleIcon from '@/components/icons/PlayCircle.vue'
import ForwardIcon from '@/components/icons/Forward.vue'
import BackwardIcon from '@/components/icons/Backward.vue'
import ArrowLeftRight from '@/components/icons/ArrowLeftRight.vue'
</script>