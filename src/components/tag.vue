<script setup>
import { IconX } from '@tabler/icons-vue';
import { ref } from 'vue';

const props = defineProps({
    taglist: Object
});


</script>

<template>
    <div v-for="(tag, tagindex) in props.taglist" :key="tagindex" :class="{'bg-pageBackground border-2 border-white':tag.active}" class="min-w-min px-5 gap-2 h-12 bg-background rounded-2xl flex place-items-center justify-center cursor-pointer tag" @click="tag.active=true">
        <h1 class="text-textmain font-main font-[800] text-[15px] text-nowrap">{{tag.name}}</h1>
        <div v-if="tag.active" class=" w-6 h-6 rounded-full flex place-items-center justify-center" @click.stop="tag.active=false">
            <IconX stroke="2" color="black" class="w-5 h-5"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>