<script setup lang="ts">
import Layout from '@/layouts/DefaultLayout.vue'
import { ref } from 'vue';

const nome = ref('');
const empresa = ref('');
const email = ref('');
const celular = ref('');
const mensagem = ref('');

const handleSubmit = () => {
    const emailDestino = 'contato@nataliamathiasergo.com.br';
    const assunto = encodeURIComponent(`Contato Site: ${nome.value} - ${empresa.value}`);
    const corpoEmail = `Nome: ${nome.value}
                        Empresa: ${empresa.value}
                        E-mail de contato: ${email.value}
                        Celular: ${celular.value}
                        Mensagem: ${mensagem.value}`;

    const corpoEncoded = encodeURIComponent(corpoEmail);

    window.location.href = `mailto:${emailDestino}?subject=${assunto}&body=${corpoEncoded}`;
    alert('Redirecionando para seu aplicativo de email...');
}

</script>

<template>
    <Layout>
        <main class="">
            <!-- hero section -->
            <section class="d-flex justify-content-center hero">
                <div class="container-fluid" id="hero"></div>
                <div class="container-fluid" id="inner-hero"></div>

                <div class="container py-5 align-content-center z-0" v-reveal="'bottom'">
                    <div class="row">
                        <div class="col-12">
                            <h1 class="text-principal display-4 ff-bree fst-italic">
                                Vamos conversar sobre sua empresa?
                            </h1>
                            <p class="text-light fs-5">
                                Solicite um orçamento, tire dúvidas ou agende uma conversa.
                            </p>
                        </div>
                    </div>
                </div>
            </section>

            <section class="">
                <div class="container py-5">
                    <div class="row">
                        <div class="col-lg-7 align-self-center">
                            <div class="p-lg-4">
                                <p class="text-principal mb-0 fs-5">
                                    <font-awesome-icon icon="fa-solid fa-caret-right" />
                                    Contato
                                </p>
                                <p class="text-green fs-2 ff-bree">
                                    Solicite um orçamento
                                </p>
                                <p>
                                    Preencha o formulário abaixo. Entrarei em contato em breve!
                                </p>

                                <form @submit.prevent="handleSubmit">
                                    <div class="row">
                                        <div class="col-lg-6 mb-3">
                                            <div class="form-group">
                                                <label for="nome" class="text-green fw-semibold">Nome completo *</label>
                                                <input type="text" name="nome" id="nome" class="form-control"
                                                    v-model="nome" required>
                                            </div>
                                        </div>
                                        <div class="col-lg-6 mb-3">
                                            <div class="form-group">
                                                <label for="empresa" class="text-green fw-semibold">Empresa *</label>
                                                <input type="text" name="empresa" id="empresa" class="form-control"
                                                    v-model="empresa" required>
                                            </div>
                                        </div>
                                        <div class="col-lg-6 mb-3">
                                            <div class="form-group">
                                                <label for="email" class="text-green fw-semibold">E-mail *</label>
                                                <input type="email" name="email" id="email" class="form-control"
                                                    v-model="email" required>
                                            </div>
                                        </div>
                                        <div class="col-lg-6 mb-3">
                                            <div class="form-group">
                                                <label for="celular" class="text-green fw-semibold">Celular / WhatsApp
                                                    *</label>
                                                <input type="tel" name="celular" id="celular" class="form-control"
                                                    v-model="celular" required>
                                            </div>
                                        </div>
                                        <div class="col-12 mb-3">
                                            <div class="form-group">
                                                <label for="mensagem" class="text-green fw-semibold">Mensagem *</label>
                                                <textarea name="mensagem" id="mensagem" class="form-control" rows="5"
                                                    v-model="mensagem"
                                                    placeholder="Descreva brevemente o que sua empresa precisa ou qual serviço lhe interessa..."
                                                    required></textarea>
                                            </div>
                                        </div>
                                        <div class="col-12 d-grid">
                                            <button type="submit" class="btn btn-success">
                                                <font-awesome-icon icon="fa-solid fa-paper-plane" />
                                                Enviar mensagem
                                            </button>
                                        </div>
                                    </div>

                                </form>
                            </div>
                        </div>

                        <div class="col-lg-5 align-self-center">
                            <div class="p-4 rounded-4 bg-green mb-4 shadow">
                                <p class="text-light fs-5 ff-bree mb-3">
                                    Informações de contato
                                </p>
                                <div class="row mb-3">
                                    <div class="col-auto">
                                        <font-awesome-icon icon="fa-brands fa-whatsapp"
                                            class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                                    </div>
                                    <div class="col">
                                        <p class="ff-bree fs-5 text-principal mb-0">
                                            WhatsApp
                                        </p>
                                        <p class="mb-1">
                                            <a href="https://wa.me/5514996880711"
                                                class="text-light text-decoration-none">
                                                +55 (14) 99688-0711
                                            </a>
                                        </p>
                                    </div>
                                </div>
                                <hr class="thin-border-light">
                                <div class="row mb-3">
                                    <div class="col-auto">
                                        <font-awesome-icon icon="fa-brands fa-whatsapp"
                                            class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                                    </div>
                                    <div class="col">
                                        <p class="ff-bree fs-5 text-principal mb-0">
                                            Email
                                        </p>
                                        <p class="mb-1">
                                            <a href="mailto:contato@nataliamathiasergo.com.br"
                                                class="text-light text-decoration-none">
                                                contato@nataliamathiasergo.com.br
                                            </a>
                                        </p>
                                    </div>
                                </div>
                                <hr class="thin-border-light">
                                <div class="row mb-3">
                                    <div class="col-auto">
                                        <font-awesome-icon icon="fa-solid fa-clock"
                                            class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                                    </div>
                                    <div class="col">
                                        <p class="ff-bree fs-5 text-principal mb-0">
                                            Horário de Atendimento
                                        </p>
                                        <p class="mb-1 text-light">
                                            Segunda a Sexta: 8h às 18h
                                            <br>
                                            Sábado: 8h às 12h
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

        </main>
    </Layout>
</template>

<style scoped>
.hero {
    position: relative;
    min-height: 300px;
}

#hero {
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 70% 40%, #0f3d3626 0%, transparent 60%), radial-gradient(ellipse 60% 80% at 20% 80%, #c8a96e14 0%, transparent 60%), linear-gradient(145deg, #0f3d36 0%, #0c3d36 50%, #093f37 100%);
}

#inner-hero {
    position: absolute;
    inset: 0;
    background-image: linear-gradient(#ffffff06 1px, transparent 1px), linear-gradient(90deg, #ffffff06 1px, transparent 1px);
    background-size: 60px 60px;
}
</style>