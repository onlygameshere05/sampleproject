<script setup>
const features = [
    {
        title: 'Lightning Fast',
        description: 'Built on Laravel 13 with Inertia and Vue 3 for instant page transitions and a smooth single-page app experience.',
        icon: 'bolt',
    },
    {
        title: 'Secure by Default',
        description: 'Authentication and authorization out of the box with Laravel Sanctum, session-based auth, and CSRF protection.',
        icon: 'shield',
    },
    {
        title: 'Developer Friendly',
        description: 'Hot module replacement via Vite, expressive routing with Ziggy, and Pest PHP for delightful testing.',
        icon: 'code',
    },
    {
        title: 'Responsive Design',
        description: 'Tailwind CSS utility-first framework with dark mode support, accessible components, and mobile-first layouts.',
        icon: 'device',
    },
];

const heroIcons = {
    bolt: 'M13 10V3L4 14h7v7l9-11h-7z',
    shield: 'M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z',
    code: 'M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4',
    device: 'M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z',
};
</script>

<template>
    <div class="bg-gray-50 dark:bg-gray-900">
        <div class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
            <div class="text-center">
                <h1 class="text-4xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-5xl md:text-6xl">
                    Build Something Amazing
                </h1>
                <p class="mx-auto mt-6 max-w-2xl text-lg text-gray-500 dark:text-gray-400">
                    A modern Laravel starter kit powered by Inertia, Vue 3, and Tailwind CSS.
                    Fast, secure, and ready for production.
                </p>
                <div class="mt-10 flex items-center justify-center gap-4">
                    <a
                        href="https://laravel.com/docs"
                        class="rounded-md bg-gray-900 px-6 py-3 text-sm font-semibold text-white shadow-sm transition hover:bg-gray-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-gray-900 dark:bg-white dark:text-gray-900 dark:hover:bg-gray-200"
                    >
                        Get Started
                    </a>
                    <a
                        href="https://github.com/laravel/laravel"
                        class="rounded-md bg-white px-6 py-3 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 transition hover:bg-gray-50 dark:bg-gray-800 dark:text-white dark:ring-gray-600 dark:hover:bg-gray-700"
                    >
                        View on GitHub
                    </a>
                </div>
            </div>
        </div>

        <div id="features" class="mx-auto max-w-7xl px-4 pb-24 sm:px-6 lg:px-8">
            <div class="mx-auto max-w-2xl text-center">
                <h2 class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl">
                    Features
                </h2>
                <p class="mt-4 text-lg text-gray-500 dark:text-gray-400">
                    Everything you need to build modern web applications.
                </p>
            </div>

            <div class="mt-16 grid gap-8 sm:grid-cols-2 lg:grid-cols-4">
                <div
                    v-for="feature in features"
                    :key="feature.title"
                    class="rounded-lg bg-white p-8 shadow-sm ring-1 ring-gray-200 transition hover:shadow-md dark:bg-gray-800 dark:ring-gray-700"
                >
                    <div class="flex size-12 items-center justify-center rounded-lg bg-indigo-50 dark:bg-indigo-900/50">
                        <svg class="size-6 text-indigo-600 dark:text-indigo-400" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" :d="heroIcons[feature.icon]" />
                        </svg>
                    </div>
                    <h3 class="mt-6 text-lg font-semibold text-gray-900 dark:text-white">
                        {{ feature.title }}
                    </h3>
                    <p class="mt-2 text-sm text-gray-500 dark:text-gray-400">
                        {{ feature.description }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>
