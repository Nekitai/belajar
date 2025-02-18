
<script lang="ts" setup>
const name = "Fajar Apriyadi";
const university = "Unitama";
const birthdate = "02-04-2002";
const NoHP = "081234567890";
const about = "Ini adalah paragraf tentang diriku. Saya adalah seseorang yang sedang belajar Nuxt 3 dan mengembangkan kemampuan saya dalam web development.";
const isDark = ref(false);

const toggleDarkMode = () => {
    isDark.value = !isDark.value;
};
definePageMeta({
    layout: 'page'
})
</script>

<template>
    <PagesContainer class="flex-1 items-center justify-between">
        <h1 class="flex-1  text-center dark:text-white text-3xl font-bold mb-4">About Me</h1>
        <div class="flex-1 text-center transition-transform transform hover:scale-105 duration-300 ease-in-out">
            <p class="text-lg">Name: {{ name }}</p>
            <p class="text-lg">University: {{ university }}</p>
            <p class="text-lg">Birthdate: {{ birthdate }}</p>
            <p class="text-lg">No. HP: {{ NoHP }}</p>
        </div>
    </PagesContainer>
</template>

<style scoped>

</style>