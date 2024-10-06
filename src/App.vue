
<script setup>
import { Button } from '@/components/ui/button'
import navbar from './components/nav.vue';
import slider from './components/slider.vue';
import infoarea from './components/infoarea.vue';
import catagory from './components/catagory.vue';
</script>

<template>
  <div class="bg-pageBackground h-[500vh] w-screen">
    <navbar />
    <slider />
    <infoarea />
    <catagory />
  </div>
</template>
