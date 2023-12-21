<template>
    <nav>
        <ul class="flex px-10 sm:px-20 text-2xl whitespace-nowrap gap-10 sm:gap-20 overflow-x-scroll scrollbar-hide">
            <li v-for="title of genreList" :key="title" class="transition duration-300 hover:scale-125 hover:text-white active:text-red-500 ">
                <button> {{title}} </button>
            </li>
        </ul>
    </nav>
</template>
<script setup lang="ts">
    import request from "@/utils/request.ts"

    const genreList: string[] = [];

    Object.entries(request).forEach(([key, {title, url}]) => {
        genreList.push(title);       
    })
    console.log(request);
    
</script>