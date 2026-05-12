<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';

const showingNav = ref(false);

const navLinks = [
    { label: 'Home', href: '/' },
    { label: 'Features', href: '#features' },
    { label: 'About', href: '#about' },
    { label: 'Contact', href: '#contact' },
];
</script>

<template>
    <nav class="border-b border-gray-100 bg-white dark:border-gray-700 dark:bg-gray-800">
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
            <div class="flex h-16 justify-between">
                <div class="flex items-center">
                    <Link href="/">
                        <ApplicationLogo class="block h-9 w-auto fill-current text-gray-800 dark:text-gray-200" />
                    </Link>
                    <div class="hidden space-x-8 sm:-my-px sm:ms-10 sm:flex">
                        <Link
                            v-for="link in navLinks"
                            :key="link.label"
                            :href="link.href"
                            class="inline-flex items-center px-1 pt-1 text-sm font-medium leading-5 text-gray-500 transition duration-150 ease-in-out hover:text-gray-700 focus:outline-none dark:text-gray-400 dark:hover:text-gray-300"
                        >
                            {{ link.label }}
                        </Link>
                    </div>
                </div>

                <div class="-me-2 flex items-center sm:hidden">
                    <button
                        @click="showingNav = !showingNav"
                        class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 transition duration-150 ease-in-out hover:bg-gray-100 hover:text-gray-500 focus:bg-gray-100 focus:text-gray-500 focus:outline-none dark:text-gray-500 dark:hover:bg-gray-900 dark:hover:text-gray-400 dark:focus:bg-gray-900 dark:focus:text-gray-400"
                    >
                        <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                            <path
                                :class="{ hidden: showingNav, 'inline-flex': !showingNav }"
                                stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M4 6h16M4 12h16M4 18h16"
                            />
                            <path
                                :class="{ hidden: !showingNav, 'inline-flex': showingNav }"
                                stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M6 18L18 6M6 6l12 12"
                            />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <div :class="{ block: showingNav, hidden: !showingNav }" class="sm:hidden">
            <div class="space-y-1 pb-3 pt-2">
                <Link
                    v-for="link in navLinks"
                    :key="link.label"
                    :href="link.href"
                    class="block border-l-4 border-transparent py-2 pe-4 ps-3 text-base font-medium text-gray-500 transition duration-150 ease-in-out hover:border-gray-300 hover:text-gray-700 focus:outline-none dark:text-gray-400 dark:hover:border-gray-600 dark:hover:text-gray-300"
                >
                    {{ link.label }}
                </Link>
            </div>
        </div>
    </nav>
</template>
