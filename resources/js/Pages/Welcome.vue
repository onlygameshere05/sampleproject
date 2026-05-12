<script setup>
import { Head } from '@inertiajs/vue3';
import HomeHeader from '@/Components/HomeHeader.vue';
import HomeBody from '@/Components/HomeBody.vue';
import HomeFooter from '@/Components/HomeFooter.vue';
</script>

<template>
    <Head title="Welcome" />

    <div class="min-h-screen bg-gray-50 dark:bg-gray-900">
        <HomeHeader />
        <HomeBody />
        <HomeFooter />
    </div>
</template>
