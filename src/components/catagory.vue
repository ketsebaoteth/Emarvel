<script setup>
import { IconChevronRight } from '@tabler/icons-vue';
import tag from './tag.vue';
import { ref } from 'vue';

let tags = ref([
    {
        name: "Gadgets",
        active: true
    },
    {
        name: "Clothing",
        active: false
    },
    {
        name: "Books",
        active: false
    },
    {
        name: "Furniture",
        active: false
    },
    {
        name: "Electronics",
        active: false
    },
    {
        name: "Accessories",
        active: false
    },
    {
        name: "Toys",
        active: false
    },
    {
        name: "Stationary",
        active: false
    },
    {
        name: "Home Appliances",
        active: false
    },
    {
        name: "Kitchen Appliances",
        active: false
    },
    {
        name: "Sports",
        active: false
    },
    {
        name: "Fitness",
        active: false
    },
    {
        name: "Health",
        active: false
    },
    {
        name: "Beauty",
        active: false
    },
    {
        name: "Grocery",
        active: false
    },
    {
        name: "Automobile",
        active: false
    },
    {
        name: "Pets",
        active: false
    },
    {
        name: "Services",
        active: false
    },
    {
        name: "Education",
        active: false
    },
    {
        name: "Entertainment",
        active: false
    },
    {
        name: "Travel",
        active: false
    },
    {
        name: "Real Estate",
        active: false
    },
    {
        name: "Jobs",
        active: false
    },
    {
        name: "Others",
        active: false
    }
])


</script>

<template>
    <div class="h-scroll-area flex w-[100vw] h-16 place-items-center px-10 gap-3 overflow-x-scroll">
        <div class="w-48 min-w-48 rounded-2xl h-12 bg-background flex place-items-center justify-center gap-2 cursor-pointer">
            <h1 class="text-textmain font-main font-[800] text-[15px]">All Catagories</h1>
            <IconChevronRight stroke="2" color="black"/>
        </div>
        <tag :taglist="tags" />
    </div>
</template>

<style lang="scss" scoped>
    .h-scroll-area{
        &::-webkit-scrollbar{
            display: none;
        }
    }
    .tag{
        &:hover{
            @apply w-36;
        }
    }
</style>