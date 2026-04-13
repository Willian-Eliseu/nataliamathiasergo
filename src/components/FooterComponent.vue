<script setup lang="ts">
import LogoFooter from '@/assets/img/white_logo.png'

</script>

<template>
    <footer class="bg-green text-white">
        <div class="container py-3">
            <div class="row py-3">
                <div class="col-md-6 col-lg-3 mb-3 mb-lg-0 align-self-center p-3">
                    <img :src="LogoFooter" alt="Logo do site" class="img-fluid w-100" />
                </div>
                <div class="col-md-6 col-lg-3 mb-3 mb-lg-0 p-3">
                    <h5 class="fw-bold">Entre em contato</h5>
                    <p class="mb-1">
                        <a href="tel:+14996880711" class="text-white text-decoration-none">
                            +55 14 99688-0711
                        </a>
                    </p>
                    <p class="mb-1">
                        <a href="mailto:contato@nataliamathiasergo.com.br" class="text-white text-decoration-none">
                            contato@nataliamathiasergo.com.br
                        </a>
                    </p>
                    <p class="mb-1">Bauru - SP, Brasil</p>
                </div>
                <div class="col-md-6 col-lg-3 mb-3 mb-lg-0 p-3">
                    <h5 class="fw-bold">Horário de Atendimento</h5>
                    <p class="mb-1">Segunda a Sexta: 8h às 18h</p>
                    <p class="mb-1">Sábado: 8h às 12h</p>
                    <p class="mb-1">Domingo: Fechado</p>
                </div>
                <div class="col-md-6 col-lg-3 mb-3 mb-lg-0 p-3">
                    <h5 class="fw-bold">Redes Sociais</h5>
                    <p class="mb-1">
                        <a href="https://www.instagram.com/nataliamathias.ergo" target="_blank"
                            rel="noopener noreferrer" class="text-white text-decoration-none">
                            <font-awesome-icon icon="fa-brands fa-instagram" size="lg" class="text-principal" />
                        </a>

                        <a href="https://www.linkedin.com/in/namathias/" target="_blank" rel="noopener noreferrer"
                            class="text-white text-decoration-none ms-1">
                            <font-awesome-icon icon="fa-brands fa-linkedin" size="lg" class="text-principal" />
                        </a>
                    </p>
                </div>
            </div>
            <div class="row py-3 justify-content-between">
                <div class="col-md-auto">
                    <p class="mb-0">&copy; Natalia Mathias Ergo 2026 - Todos os direitos reservados</p>
                </div>
                <div class="col-md-auto">
                    <p class="mb-0">
                        Desenvolvido por
                        <a href="mailto:w.eliseu@gmail.com" target="_blank" rel="noopener noreferrer"
                            class="text-white fw-semibold text-decoration-none">NovaWeb</a>
                    </p>
                </div>
            </div>
        </div>
    </footer>
</template>