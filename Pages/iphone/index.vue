<template>
    <div>
        <div class="grid grid-cols-4 gap-4 mt-10">
            <nuxt-link to="/iphone/iphone-12" class="shadow-lg text-center border rounded-lg p-5">
                <h1 class="mb-5">iPhione 12</h1>
                <div class="flex justify-center">
                    <img src="/images/iphn12.jpg" alt="iPhone 12" width="200">
                </div>
            </nuxt-link>

            <nuxt-link to="/iphone/iphone-12-pro" class="shadow-lg text-center border rounded-lg p-5">
                <h1 class="mb-5">iPhione 12 Pro</h1>
                <div class="flex justify-center">
                    <img src="/images/iphn12pro.jpg" alt="iPhone 12" width="200">
                </div>
            </nuxt-link>
        </div>
    </div>
</template>

<script setup>
    useHead({
        title: "Nuxt3 - iPhones"
    });
</script>