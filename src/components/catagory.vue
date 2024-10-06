<script setup>
import { IconChevronRight } from '@tabler/icons-vue';

let tags = [
    "Gadgets",
    "Clothing",
    "Footwear",
    "Accessories",
    "Home Decor",
    "Furniture",
    "Stationary",
    "Books",
    "Toys",
    "Sports",
    "Fitness",
    "Health",
]
</script>

<template>
    <div class="flex w-[100vw] h-16 place-items-center px-10 gap-3 overflow-x-scroll">
        <div class="w-48 min-w-48 rounded-2xl h-14 bg-background flex place-items-center justify-center gap-2 cursor-pointer">
            <h1 class="text-textmain font-main font-[800] text-[15px]">All Catagories</h1>
            <IconChevronRight stroke="2" color="black"/>
        </div>
        <div class="w-32 min-w-32 h-14 bg-background rounded-2xl flex place-items-center justify-center" v-for="(tag,tagindex) in tags" :key="tagindex">
            <h1 class="text-textmain font-main font-[800] text-[17px]">{{tag}}</h1>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>