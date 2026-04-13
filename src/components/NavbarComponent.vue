<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue'
import { RouterLink, useRoute } from 'vue-router'
import Logo from '@/assets/img/logo.png'

const fixedNavbar = ref<boolean>(false);
const actualRoute = ref<string>('');
const route = useRoute();

const onScroll = () => {
    fixedNavbar.value = window.scrollY > 56
}

onMounted(() => {
    window.addEventListener('scroll', onScroll)
    actualRoute.value = route.name as string;
    console.log(actualRoute.value)
})

onUnmounted(() => {
    window.removeEventListener('scroll', onScroll)
})
</script>

<template>
    <header>
        <div :class="['container-fluid d-none d-xl-block bg-green', { 'd-none': fixedNavbar }]">
            <div class="container">
                <div class="row justify-content-between py-3">
                    <div class="col-lg-auto">
                        <a href="https://wa.me/5514996880711" class="text-light text-decoration-none fw-semibold">
                            <font-awesome-icon icon="fa-brands fa-whatsapp" class="text-principal" />
                            +55 14 99688-0711
                        </a>
                        <a href="mailto:contato@nataliamathiasergo.com.br"
                            class="text-light text-decoration-none fw-semibold ms-4">
                            <font-awesome-icon icon="fa-solid fa-envelope" class="text-principal" />
                            contato@nataliamathiasergo.com.br
                        </a>
                    </div>
                    <div class="col-lg-auto">
                        <span class="text-light">
                            <font-awesome-icon icon="fa-solid fa-clock" class="text-principal" />
                            Segunda a Sexta: 8h às 18h | Sábado: 8h às 12h
                        </span>
                        <span class="text-light ms-4">
                            <font-awesome-icon icon="fa-solid fa-location-dot" class="text-principal" />
                            Bauru e Região - SP
                        </span>
                    </div>
                </div>
            </div>
        </div>
        <nav :class="['navbar navbar-expand-lg bg-light shadow', { 'fixed-top': fixedNavbar }]" data-bs-theme="light">
            <div class="container py-1">
                <a class="navbar-brand fw-bold fs-3" href="#">
                    <img :src="Logo" alt="Logo do site" height="50">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                    <ul class="navbar-nav fw-bold">
                        <li class="nav-item ms-lg-2">
                            <RouterLink :class="['nav-link', { 'active': actualRoute === 'home' }]" to="/">Início
                            </RouterLink>
                        </li>
                        <li class="nav-item ms-lg-2">
                            <RouterLink :class="['nav-link', { 'active': actualRoute === 'sobre' }]" to="/sobre">Sobre
                            </RouterLink>
                        </li>
                        <li class="nav-item ms-lg-2">
                            <RouterLink :class="['nav-link', { 'active': actualRoute === 'servicos' }]" to="/servicos">
                                Serviços</RouterLink>
                        </li>
                        <li class="nav-item ms-lg-2">
                            <RouterLink :class="['nav-link', { 'active': actualRoute === 'contato' }]" to="/contato">
                                Contato</RouterLink>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>