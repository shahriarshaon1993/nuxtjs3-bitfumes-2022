<template>
  <div>
    <p>Hello Index Page.</p>
    <button @click="moveToAbout">Take me to about page</button>
  </div>
</template>

<script setup>
  function moveToAbout() {
    navigateTo('about');
  }
</script>