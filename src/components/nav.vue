<script setup>

</script>

<template>
    <div class="w-screen h-[100px] flex place-items-center px-16 gap-4">
        <h1 class="font-main font-[800] text-[20px]">EMARVEL</h1>
        <input type="text" class="search w-72 h-12 rounded-2xl px-3 font-main font-bold text-sm ml-auto outline-none" placeholder="Search Products">
        <img src="./icons/search.svg" alt="" class="ml-[-60px] z-10">
        <div class="navbtns">
            <img src="./icons/fav.svg" alt="">
        </div>
        <div class="navbtns">
            <img src="./icons/cart.svg" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .search{
        transition: 0.2s ease-in-out;
        &::placeholder{
            @apply text-textmain;
        }
        @apply pr-10;
        &:hover{
            @apply w-[300px];
        }
    }
    .navbtns {
        @apply w-12 h-12 rounded-full bg-background flex place-items-center justify-center cursor-pointer;
    }
</style>