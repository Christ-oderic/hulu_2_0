<template>    
    <li class="flex flex-col items-center cursor-pointer w-20 sm:w-20 hover:text-white group">
        <Icon class="h-8 mb-1 group-hover:animate-bounce" />
        <a href="#" class="uppercase opacity-0 group-hover:opacity-100">{{title}}</a>
    </li>
</template>

<script setup lang="ts">
import type { FunctionalComponent, HTMLAttributes, VNodeProps } from 'vue';

const props = defineProps<{
    title: String,
    Icon: FunctionalComponent<HTMLAttributes & VNodeProps, {}, any>,
}>();

</script>