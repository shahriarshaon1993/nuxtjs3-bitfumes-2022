<template>
    <div>
        <h1>iPhone {{ name }}</h1>
    </div>
</template>

<script setup>
    const route = useRoute();
    
    const name = computed(() => {
        return route.params.name;
    });
</script>