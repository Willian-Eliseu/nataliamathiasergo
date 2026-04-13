<script setup lang="ts">
import Layout from '@/layouts/DefaultLayout.vue'
import natalia from '@/assets/img/nataliaMathias.png'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

const dataList = <any[]>[
    { id: 1, icon: 'fa-solid fa-eye', title: 'Visão', content: 'Ser referência em ergonomia, movimento e qualidade de vida, impactando positivamente empresas e pessoas através de um trabalho humano, técnico e transformador.' },
    { id: 2, icon: 'fa-solid fa-heart', title: 'Propósito', content: 'Promover saúde, bem-estar e qualidade de vida através da ergonomia e do movimento, ajudando pessoas e empresas a viverem com mais equilíbrio, consciência corporal e prevenção.' }
];

const posGraduacoes = <any[]>[
    { id: 1, title: 'Treinamento Personalizado' },
    { id: 2, title: 'Saúde da Mulher Premium' },
    { id: 3, title: 'Avaliação Física e Funcional do Idoso' },
    { id: 4, title: 'Saúde da Mulher – Abordagem Multidisciplinar' },
    { id: 5, title: 'MBA em Ergonomia, Saúde e Bem-Estar' },
    { id: 6, title: 'Ginástica Laboral' }
];

const cursosList = <any[]>[
    { id: 1, title: 'Montagem de Treinamentos em Ergonomia' },
    { id: 2, title: 'Avaliação Física e Prescrição para Idosos' },
    { id: 3, title: 'Avaliação Básica do Movimento' },
    { id: 4, title: 'Estudos aplicados em ergonomia e funcionalidade' },
    { id: 5, title: 'Formação de Consultores em Ergonomia (FCE) – Método Débora Dengo' }
];
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
                                Natalia Mathias | Ergonomia & Movimento
                            </h1>
                            <p class="text-light fs-5">
                                Uma marca construída com propósito, conhecimento e cuidado real com as pessoas.
                            </p>
                        </div>
                    </div>
                </div>
            </section>

            <!-- currículo -->
            <section class="">
                <div class="container py-5">
                    <div class="row">
                        <!-- esquerda - congelar ao rolar a página -->
                        <div class="col-lg-4 mb-3" v-reveal="'bottom'">
                            <div class="p-4 rounded-4 bg-green mb-4 shadow">
                                <div class="row">
                                    <div class="col">
                                        <img :src="natalia" alt="Natalia Mathias"
                                            class="img-fluid rounded-circle w-75 d-block mx-auto border border-principal border-3">
                                    </div>
                                </div>
                                <div class="row">
                                    <p class="fs-4 text-center text-light fw-semibold mb-0">
                                        Natalia A F Mathias
                                    </p>
                                    <p class="text-center text-light">
                                        Educadora Física / Ergonomista
                                    </p>
                                </div>
                            </div>
                            <div class="p-4 rounded-4 bg-light border border-1 border-principal">
                                <p class="ff-bree fs-5 text-green">
                                    GRADUAÇÕES
                                </p>
                                <ul class="list-unstyled">
                                    <li v-reveal="'right'">
                                        <font-awesome-icon icon="fa-solid fa-user-graduate" class="text-green" />
                                        Educação Física (Bacharelado e Licenciatura)
                                    </li>
                                    <li v-reveal="'right'">
                                        <font-awesome-icon icon="fa-solid fa-user-graduate" class="text-green" />
                                        Pedagogia
                                    </li>
                                </ul>
                                <hr>
                                <p class="ff-bree fs-5 text-green">
                                    PÓS-GRADUAÇÕES
                                </p>
                                <ul class="list-unstyled mb-4">
                                    <li v-reveal="'right'" v-for="v in posGraduacoes" :key="v.id">
                                        <font-awesome-icon icon="fa-solid fa-graduation-cap" class="text-green" />
                                        {{ v.title }}
                                    </li>
                                </ul>
                                <hr>
                                <p class="ff-bree fs-5 text-green">
                                    CURSOS
                                </p>
                                <ul class="list-unstyled">
                                    <li v-reveal="'right'" v-for="v in cursosList" :key="v.id">
                                        <font-awesome-icon icon="fa-solid fa-book" class="text-green" />
                                        {{ v.title }}
                                    </li>
                                </ul>
                            </div>
                        </div>

                        <div class="col-lg-8">
                            <h2 class="text-principal ff-bree" v-reveal="'bottom'">
                                Minha História
                            </h2>
                            <p class="" v-reveal="'bottom'">
                                Sou Natalia Mathias, profissional de Educação Física com formação completa (Bacharelado
                                e Licenciatura), também graduada em Pedagogia, com uma trajetória construída sobre o
                                cuidado com pessoas em diferentes fases da vida.
                                <br>
                                Minha atuação é guiada pela união entre conhecimento técnico e sensibilidade humana,
                                desenvolvendo estratégias que respeitam a individualidade de cada pessoa e a realidade
                                de cada empresa.
                                <br>
                                Ao longo da minha formação, busquei me especializar profundamente para oferecer um
                                atendimento completo, seguro e eficaz.
                            </p>

                            <div class="row mb-3">
                                <div class="col-lg-6 mb-3" v-reveal="'bottom'" v-for="data in dataList" :key="data.id">
                                    <div class="p-4 rounded-4 bg-light hover-up-wb">
                                        <div class="row">
                                            <div class="col-auto align-self-center">
                                                <font-awesome-icon :icon="data.icon"
                                                    class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                                            </div>
                                            <div class="col align-self-center">
                                                <p class="ff-bree fs-5 text-principal mb-0">
                                                    {{ data.title }}
                                                </p>
                                            </div>
                                        </div>
                                        <p class="mb-1">
                                            {{ data.content }}
                                        </p>
                                    </div>
                                </div>
                            </div>

                            <p class="fs-4 text-principal ff-bree" v-reveal="'bottom'">
                                Valores
                            </p>

                            <ul class="list-unstyled mb-4">
                                <li class="mb-1" v-reveal="'right'">
                                    <font-awesome-icon icon="fa-solid fa-circle-check" class="text-green" />
                                    Cuidado com as pessoas: Cada atendimento é único e pensado com respeito à
                                    individualidade.
                                </li>
                                <li class="mb-1" v-reveal="'right'">
                                    <font-awesome-icon icon="fa-solid fa-circle-check" class="text-green" />
                                    Excelência técnica: Atuação baseada em conhecimento científico e atualização
                                    constante.
                                </li>
                                <li class="mb-1" v-reveal="'right'">
                                    <font-awesome-icon icon="fa-solid fa-circle-check" class="text-green" />
                                    Comprometimento real: Entrega com responsabilidade, ética e propósito.
                                </li>
                                <li class="mb-1" v-reveal="'right'">
                                    <font-awesome-icon icon="fa-solid fa-circle-check" class="text-green" />
                                    Clareza e proximidade: Comunicação simples, humana e acessível.
                                </li>
                                <li class="mb-1" v-reveal="'right'">
                                    <font-awesome-icon icon="fa-solid fa-circle-check" class="text-green" />
                                    Transformação através do movimento: Acreditamos no movimento como ferramenta de
                                    mudança física e emocional.
                                </li>
                            </ul>

                            <div class="p-4 bg-green rounded-4 mb-4" v-reveal="'bottom'">
                                <p class="text-principal ff-bree fs-4">
                                    Minha abordagem
                                </p>
                                <p class="text-light">
                                    Cada pessoa e cada empresa possuem necessidades específicas. Por isso, meu trabalho
                                    é baseado em escuta, análise e personalização.
                                    <br>
                                    Desenvolvo programas de ergonomia e ginástica laboral que vão além do básico — com
                                    foco em prevenção, desempenho, bem-estar e resultados reais.
                                    <br>
                                    Mais do que entregar um serviço, meu compromisso é garantir que cada cliente
                                    compreenda o processo, aplique as orientações e sinta, na prática, os benefícios no
                                    dia a dia.

                                </p>
                            </div>

                            <p class="text-center">
                                <a href="mailto:contato@nataliamathiasergo.com.br"
                                    class="btn btn-default btn-lg px-4 py-2 rounded-3 mb-3 mb-lg-0">
                                    <font-awesome-icon icon="fa-solid fa-file-lines" />
                                    Solicitar Orçamento
                                </a>
                                <a href="https://wa.me/5514996880711"
                                    class="btn btn-default btn-lg px-4 py-2 rounded-3 ms-lg-3">
                                    <font-awesome-icon icon="fa-brands fa-whatsapp" />
                                    Falar no WhatsApp
                                </a>
                            </p>
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