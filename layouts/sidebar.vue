<template>
    <main class="user-layout bg-purple-300">
        <article class="sidebar">
            <p>Dashboard</p>
            <p>Settings</p>
        </article>
        <section>
            <!-- Here nuxt will replace page content -->
            <slot></slot>
        </section>
    </main>
</template>

<style>
.user-layout {
    display: flex;
}

.sidebar {
    display: flex;
    flex-direction: column;
}
</style>