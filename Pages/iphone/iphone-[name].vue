<template>
    <div>
        <Head>
            <Title>Nuxt3 - iPhone {{ name }}</Title>
        </Head>
        <h1>iPhone {{ name }}</h1>
    </div>
</template>

<script setup>
    const route = useRoute();
    
    const name = computed(() => {
        return route.params.name;
    });

    // useHead({
    //     title: `Nuxt3 - iPhone ${route.params.name}`
    // });
</script>