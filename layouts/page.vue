<script lang="ts" setup>
const menus = [
    { name: 'Home', path: '/' },
    { name: 'About', path: '/about' },
    { name: 'Contact', path: '/contact' },
]
</script>

<template>
    <div class="bg-grey-50 text-gray-900 dark:bg-gray-950 dark:text-gray-100 min-h-screen flex flex-col">
        <header class="border-b border-bg-grey-500/50 h-[68px] flex" >
            <PagesContainer class="flex-1 flex items-center justify-between">
                <NuxtLink to="/" class="text-lg font-bold">Nuxt</NuxtLink>
                    <div>
                        <nav>
                            <ul class="flex gap-4">
                                <li v-for="(menu, i) in menus" :key="i">
                                    <NuxtLink :to="menu.path" class="text-sm hover:text-primary">{{ menu.name }}</NuxtLink>
                                </li>
                            </ul>
                        </nav>
                    </div>
            </PagesContainer>
        </header>
        <main class="flex-1 flex">
            <slot />
        </main>
        <footer class="border-t border-bg-grey-500/50 h-[60px] flex">
            <PagesContainer class="flex-1 items-center justify-between">
                <div class="flex-1 text-center">
                    <span class="text-sm">&copy; 2024</span>
                </div>
            </PagesContainer>
        </footer>   
    </div>
</template>