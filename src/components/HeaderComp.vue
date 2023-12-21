
import type HeaderItemVue from './HeaderItem.vue';
<template>
    <header class="flex flex-col-reverse sm:flex-row m-5 justify-between items-center">
        <ul class="flex flex-grow justify-evenly max-w-2xl">
            <HeaderItem v-for="link in links" :key="link.title" :title="link.title" :Icon="link.icon" />
        </ul>
        <img src="../assets/hulu.webp" alt="logo Hulu">
    </header>
</template>

<script setup lang="ts">
import HeaderItem  from "@/components/HeaderItem.vue"
import {
    HomeIcon,
    BoltIcon,
    CheckBadgeIcon,
    RectangleStackIcon,
    MagnifyingGlassIcon,
    UserIcon,
} from "@heroicons/vue/24/outline"
const links = [
    {title: "home", icon: HomeIcon},
    {title: "trending", icon: BoltIcon},
    {title: "verified", icon: CheckBadgeIcon},
    {title: "collections", icon: RectangleStackIcon},
    {title: "search", icon: MagnifyingGlassIcon},
    {title: "account", icon: UserIcon},

]
</script>