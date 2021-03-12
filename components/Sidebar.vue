<template>
    <aside class="h-screen sticky top-0 w-64 border-r border-gray-300">
        <div class="text-2xl text-right mt-10 mx-8">
            <NuxtLink class="text-teal-800" style="color: teal" to="/">Prima Putra</NuxtLink>
        </div>
        <nav class="mt-6 mx-8 text-right">
            <div class="my-4"><NuxtLink class="hover:text-teal-600 hover:underline" to="/about">About</NuxtLink></div>
            <div class="my-4"><NuxtLink class="hover:text-teal-600 hover:underline" to="/portfolio">Portfolio</NuxtLink></div>
            <div class="my-4"><NuxtLink class="hover:text-teal-600 hover:underline" to="/blog">Blog</NuxtLink></div>
        </nav>
    </aside>
</template>

<script>
export default {
    name: 'Sidebar'
}
</script>

<style>
.nuxt-link-active {
  color: red;
}
</style>