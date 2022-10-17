<template>
    <div>
        <button @click="increment">Increment</button>
        <h1>{{ count }}</h1>
        <button @click="decrement">Decrement</button>
    </div>
</template>

<script setup>
    const count = ref(0);

    function increment() {
        count.value++;
    }

    function decrement() {
        count.value--;
    }
</script>

<style>

</style>