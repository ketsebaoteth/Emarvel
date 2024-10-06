<script setup>
import { gsap } from 'gsap';
import { onMounted, ref } from 'vue';
import {
  Select,
  SelectContent,
  SelectGroup,
  SelectItem,
  SelectLabel,
  SelectTrigger,
  SelectValue,
} from '@/components/ui/select'

const search = ref(null);

onMounted(() => {
    const searchElement = search.value;

    searchElement.addEventListener('mouseenter', () => {
        gsap.to(searchElement, { width: '300px', duration: 0.2, ease: "back.out(1.7)" });
    });

    searchElement.addEventListener('mouseleave', () => {
        gsap.to(searchElement, { width: '288px', duration: 0.2, ease: "back.out(1.7)" }); // Adjust width to match initial width
    });
});
</script>

<template>
    <div class="w-screen h-[100px] flex place-items-center px-16 gap-3">
        <h1 class="font-main font-[800] text-[20px]">EMARVEL</h1>
        <input ref="search" type="text" class="search w-72 h-12 rounded-2xl px-3 font-main font-bold text-sm ml-auto outline-none" placeholder="Search Products">
        <img src="./icons/search.svg" alt="" class="ml-[-55px] z-10">
        <div class="navbtns">
            <img src="./icons/fav.svg" alt="">
        </div>
        <div class="navbtns">
            <img src="./icons/cart.svg" alt="">
        </div>
        <div class="sampleProfile w-12 h-12 rounded-full cursor-pointer">

        </div>
        <!--Language Select-->
        <Select>
            <SelectTrigger class="w-20">
                <SelectValue placeholder="En" class="font-main text-textmain font-bold"></SelectValue>
            </SelectTrigger>
            <SelectContent>
                <SelectGroup>
                    <SelectItem value="English">En</SelectItem>
                    <SelectItem value="Amharic">Am</SelectItem>
                    <SelectItem value="Oromigna">Or</SelectItem>
                </SelectGroup>
            </SelectContent>
        </Select>
    </div>
</template>

<style lang="scss" scoped>
    .sampleProfile{
        background-image: url("./icons/sampleprofile.jpg");
        background-size: cover;
        background-position: center center;
        background-repeat: no-repeat;
    }
    .search{
        transition: 0.2s ease-in-out;
        &::placeholder{
            @apply text-textmain;
        }
        @apply pr-10;
    }
    .navbtns {
        @apply w-12 h-12 rounded-full bg-background flex place-items-center justify-center cursor-pointer;
    }
</style>