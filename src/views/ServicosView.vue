<script setup lang="ts">
import Layout from '@/layouts/DefaultLayout.vue'

const serviceList = <any[]>[
    { id: 1, icon: 'fa-solid fa-file-circle-exclamation', pretitle: 'AEP', title: 'Avaliação Ergonômica Preliminar', content: 'Diagnóstico inicial do ambiente de trabalho que mapeia os principais riscos ergonômicos, orientando as próximas etapas de adequação com base em evidências concretas.' },
    { id: 2, icon: 'fa-solid fa-magnifying-glass-chart', pretitle: 'AET', title: 'Análise Ergonômica do Trabalho', content: 'Estudo técnico aprofundado da atividade real de trabalho, com laudo completo conforme exigido pela NR-17. O documento mais completo de ergonomia reconhecido pela legislação brasileira.' },
    { id: 3, icon: 'fa-solid fa-brain', pretitle: 'ARP', title: 'Avaliação de Riscos Psicossociais', content: 'Identificação e análise dos fatores psicossociais que afetam a saúde mental e o bem-estar dos colaboradores, com foco em prevenção e na promoção de um ambiente organizacional saudável.' },
    { id: 4, icon: 'fa-solid fa-chalkboard-user', pretitle: 'TREINAMENTOS', title: 'Treinamentos em Ergonomia', content: 'Capacitações práticas para equipes e gestores, com conteúdo adaptado ao setor e às atividades da empresa. Foco em aplicação real e reforço da cultura de prevenção.' },
    { id: 5, icon: 'fa-solid fa-microphone-lines', pretitle: 'PALESTRAS', title: 'Palestras Corporativas', content: 'Apresentações educativas e dinâmicas sobre ergonomia e saúde ocupacional. Ideais para SIPAT, semanas de saúde e eventos internos, com conteúdo personalizado para cada empresa.' },
    { id: 6, icon: 'fa-solid fa-person-walking', pretitle: 'GINÁSTICA LABORAL', title: 'Ginástica Laboral', content: 'Programas de atividade física realizados no próprio ambiente de trabalho. Previnem lesões, melhoram a postura e promovem o bem-estar físico e mental das equipes ao longo da jornada.' }
];
</script>

<template>
    <Layout>
        <main>
            <!-- hero section -->
            <section class="d-flex justify-content-center hero">
                <div class="container-fluid" id="hero"></div>
                <div class="container-fluid" id="inner-hero"></div>

                <div class="container py-5 align-content-center z-0" v-reveal="'bottom'">
                    <div class="row">
                        <div class="col-12">
                            <h1 class="text-principal display-4 ff-bree fst-italic">
                                Serviços de Ergonomia Especializados
                            </h1>
                            <p class="text-light fs-5">
                                Ergonomia levada a sério. Seis soluções técnicas, alinhadas à NR-17.
                                <br>
                                Atendemos em Bauru e Região.
                            </p>
                        </div>
                    </div>
                </div>
            </section>

            <!-- serviços disponíveis -->
            <section class="">
                <div class="container py-5">
                    <div class="row" v-reveal="'bottom'">
                        <p class="text-principal fs-5">
                            <font-awesome-icon icon="fa-solid fa-caret-right" />
                            Visão Geral
                        </p>
                        <p class="text-green ff-bree fs-1">
                            Conheça cada serviço disponível
                        </p>
                    </div>

                    <div class="row d-flex justify-content-center" v-reveal="'bottom'">
                        <div class="col-md-6 col-lg-4 mb-4" v-reveal="'bottom'" v-for="card in serviceList"
                            :key="card.id">
                            <div class="p-4 bg-light rounded-4 hover-up-wb" style="min-height: 240px;">
                                <div class="row mb-3">
                                    <div class="col-auto">
                                        <font-awesome-icon :icon="card.icon"
                                            class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                                    </div>
                                    <div class="col">
                                        <p class="ff-bree fs-5 text-principal mb-0">
                                            {{ card.pretitle }}
                                        </p>
                                        <p class="mb-1 fw-semibold">
                                            {{ card.title }}
                                        </p>
                                    </div>
                                </div>
                                <p class="mb-1">
                                    {{ card.content }}
                                </p>
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