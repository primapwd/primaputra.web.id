<template>
    <!-- Top Bar Nav -->
    <nav class="w-full h-16 py-6 bg-green-400 shadow">
        <div class="w-full h-auto items-center">

            <nav>
                <ul class="flex items-center justify-center font-bold text-sm text-white uppercase no-underline">
                    <li><a class="hover:text-teal-600 hover:underline px-4" href="/">Home</a></li>
                    <li><a class="hover:text-teal-600 hover:underline px-4" href="/about">About</a></li>
                    <li><a class="hover:text-teal-600 hover:underline px-4" href="/portfolio">Portfolio</a></li>
                    <li><a class="hover:text-teal-600 hover:underline px-4" href="/blog">Blog</a></li>
                </ul>
            </nav>

            <div class="flex items-center text-lg no-underline text-white pr-6">
                <a class="pl-6" href="#">
                    <i class="fab fa-twitter"></i>
                </a>
                <a class="pl-6" href="#">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>