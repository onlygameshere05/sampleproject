<script setup>
const footerLinks = {
    Product: ['Features', 'Pricing', 'Changelog'],
    Company: ['About', 'Blog', 'Careers'],
    Support: ['Documentation', 'Contact', 'Status'],
};
</script>

<template>
    <footer class="bg-white dark:bg-gray-800">
        <div class="mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-8">
            <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-4">
                <div>
                    <h3 class="text-sm font-semibold text-gray-900 dark:text-white">Product</h3>
                    <ul class="mt-4 space-y-3">
                        <li v-for="link in footerLinks.Product" :key="link">
                            <a href="#" class="text-sm text-gray-500 transition hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-900 dark:text-white">Company</h3>
                    <ul class="mt-4 space-y-3">
                        <li v-for="link in footerLinks.Company" :key="link">
                            <a href="#" class="text-sm text-gray-500 transition hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-900 dark:text-white">Support</h3>
                    <ul class="mt-4 space-y-3">
                        <li v-for="link in footerLinks.Support" :key="link">
                            <a href="#" class="text-sm text-gray-500 transition hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-900 dark:text-white">Legal</h3>
                    <ul class="mt-4 space-y-3">
                        <li><a href="#" class="text-sm text-gray-500 transition hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">Privacy Policy</a></li>
                        <li><a href="#" class="text-sm text-gray-500 transition hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="mt-12 border-t border-gray-200 pt-8 dark:border-gray-700">
                <p class="text-center text-sm text-gray-400 dark:text-gray-500">
                    &copy; {{ new Date().getFullYear() }} Laravel. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</template>
