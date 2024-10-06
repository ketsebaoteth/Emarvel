<script setup>
import { IconChevronRight } from '@tabler/icons-vue';
</script>

<template>
    <div class="flex w-screen h-16 place-items-center px-10 gap-3">
        <div class="w-48 rounded-2xl h-14 bg-background flex place-items-center justify-center gap-2 cursor-pointer">
            <h1 class="text-textmain font-main font-[800] text-[15px]">All Catagories</h1>
            <IconChevronRight stroke="2" color="black"/>
        </div>
        <div class="searchicon z-30 w-12 h-12 flex place-items-center justify-center bg-pageBackground rounded-2xl ml-1">
            <img src="./icons/search.svg" alt="">
        </div>
        <input type="text" class="w-72 h-14 bg-background rounded-2xl ml-[-65px] pl-16 outline-none placeholder-textmain placeholder:font-bold placeholder:font-main placeholder:text-textmain" placeholder="search for a product">
    </div>
</template>

<style lang="scss" scoped>

</style>