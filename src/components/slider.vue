<script setup>
import { IconChevronRight, IconChevronLeft } from '@tabler/icons-vue';
</script>

<template>
    <div class="slider w-screen h-[400px] px-5 flex place-items-center">
        <div class="toleft">
            <IconChevronLeft stroke={2} />
        </div>
        <div class="bannerimg w-full h-[332px] bg-black rounded-2xl">
        </div>
        <div class="toright">
            <IconChevronRight stroke={2} />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.slider{
    .bannerimg{
        background-image: url("./icons/bannersample.png");

    }
    div{
        *{
            @apply w-12 h-12;
        }
    }
}

</style>