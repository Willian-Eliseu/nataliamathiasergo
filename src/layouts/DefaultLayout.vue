<script setup lang="ts">
import Navbar from '@/components/NavbarComponent.vue'
import Footer from '@/components/FooterComponent.vue'
</script>

<template>
    <Navbar />
    <div id="main-content">
        <slot />
    </div>
    <Footer id="site-footer" />
</template>

<style scoped>
#main-content {
    display: flex;
    flex-direction: column;
    min-height: calc(100dvh - 100px);
}

#site-footer {
    margin-top: auto;
}
</style>