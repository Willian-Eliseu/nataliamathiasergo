<script setup lang="ts">
import Layout from '@/layouts/DefaultLayout.vue'
import { RouterLink } from 'vue-router'
import NatiBg from '@/assets/img/nati-bg.png'
import VueEasyLightbox from 'vue-easy-lightbox'
import { ref } from 'vue'
import galeria1 from '@/assets/img/galeria1.jpeg'
import galeria2 from '@/assets/img/galeria2.jpeg'
import galeria3 from '@/assets/img/galeria3.jpeg'
import galeria4 from '@/assets/img/galeria4.jpeg'
import galeria5 from '@/assets/img/galeria5.jpeg'
import galeria6 from '@/assets/img/galeria6.jpeg'
import galeria7 from '@/assets/img/galeria7.jpeg'
import galeria8 from '@/assets/img/galeria8.jpeg'
import galeria9 from '@/assets/img/galeria9.jpeg'
import galeria10 from '@/assets/img/galeria10.jpeg'
import galeria11 from '@/assets/img/galeria11.jpeg'
import galeria12 from '@/assets/img/galeria12.jpeg'

const aboutContent = <any[]>[
  { id: 1, pretitle: 'ESPECIALIZAÇÃO', title: 'Pós em Ergonomia', content: 'com base na NR-17' },
  { id: 2, pretitle: 'SERVIÇOS OFERECIDOS', title: '6 Serviços', content: 'AEP | AET | ARP | Ginástica Laboral | Palestras | Treinamentos' },
  { id: 3, pretitle: 'ÁREA DE ATENDIMENTO', title: 'Bauru e Região', content: 'Atendo presencialmente, todas as cidades da região de Bauru' },
  { id: 4, pretitle: 'NORMA DE REFERÊNCIA', title: 'NR-17 Alinhada', content: 'todos os serviços seguem a Norma Regulamentadora de Ergonomia' }
];

const ergonomicList = <any[]>[
  { id: 1, icon: 'fa-solid fa-shield-heart', title: 'Prevenção de Lesões', content: 'Identificação e correção de riscos ergonômicos antes que se tornem afastamentos, LER/DORT e passivos trabalhistas.' },
  { id: 2, icon: 'fa-solid fa-gavel', title: 'Adequação à NR-17', content: 'Conformidade legal com a Norma Regulamentadora de Ergonomia, reduzindo riscos de autuações e processos jurídicos.' },
  { id: 3, icon: 'fa-solid fa-chart-line', title: 'Produtividade Real', content: 'Colaboradores com postos de trabalho adequados produzem mais, erram menos e se ausentam com muito menor frequência.' },
  { id: 4, icon: 'fa-solid fa-heart-pulse', title: 'Saúde Ocupacional', content: 'Promoção de bem-estar físico e mental no ambiente de trabalho, com práticas que realmente fazem diferença no cotidiano das equipes.' },
  { id: 5, icon: 'fa-solid fa-network-wired', title: 'Organização de Processos', content: 'Levantamentos ergonômicos estruturados que revelam oportunidades de melhoria nos fluxos, postos e ferramentas de trabalho.' },
  { id: 6, icon: 'fa-solid fa-handshake', title: 'Clima Organizacional', content: 'Investir nas condições de trabalho demonstra cuidado com as pessoas, fortalecendo engajamento, confiança e retenção de talentos.' }
];

const images = [
  galeria1,
  galeria2,
  galeria3,
  galeria4,
  galeria5,
  galeria6,
  galeria7,
  galeria8,
  galeria9,
  galeria10,
  galeria11,
  galeria12
];

const visibleRef = ref(false)
const indexRef = ref(0)
const showImg = (index: number) => {
  indexRef.value = index
  visibleRef.value = true
}
const onHide = () => visibleRef.value = false
</script>

<template>
  <Layout>
    <main>
      <!-- hero section -->
      <section class="d-flex justify-content-center hero">
        <div class="container-fluid" id="hero"></div>
        <div class="container-fluid" id="inner-hero"></div>

        <div class="container py-5 align-content-center">
          <div class="row">
            <div class="col-lg-6 z-0 align-self-center">
              <p class="text-start small">
                <span
                  class="py-2 px-4 rounded-pill bg-light text-principal border-principal border bg-opacity-25 fst-italic">
                  Especialista em Ergonomia e Ginástica Laboral
                </span>
              </p>

              <h1 class="text-light ff-bree display-4">
                Consultoria em <span class="text-principal">Ergonomia e Ginástica Laboral</span> - NR-17
              </h1>

              <p class="text-start text-light fs-5">
                Serviços de consultorias especializados em ergonomia ocupacional e ginástica laboral alinhados à NR-17,
                com foco na prevenção e saúde no trabalho.
              </p>

              <p class="text-center text-lg-start">
                <span class="py-1 px-3 rounded-pill bg-light text-light border-principal border bg-opacity-25 small">
                  <font-awesome-icon icon="fa-solid fa-location-dot" class="text-principal" />
                  Bauru e Região
                </span>
              </p>

              <p class="text-center text-lg-start pt-3">
                <a href="mailto:contato@nataliamathiasergo.com.br"
                  class="btn btn-default px-4 py-2 rounded-3 mb-3 mb-lg-0">
                  <font-awesome-icon icon="fa-solid fa-file-lines" />
                  Solicitar Orçamento
                </a>
                <a href="https://wa.me/5514996880711" class="btn btn-inverted px-4 py-2 rounded-3 ms-lg-3">
                  <font-awesome-icon icon="fa-brands fa-whatsapp" />
                  Falar no WhatsApp
                </a>
              </p>
            </div>
            <div class="col-lg-6 d-none d-lg-block align-self-center" v-reveal="'bottom'">
              <div class="d-flex flex-column gap-3">
                <div class="bg-light bg-opacity-10 text-light p-4 rounded-4 mb-3 hover-up">
                  <div class="mb-3">
                    <font-awesome-icon icon="fa-solid fa-clipboard-check"
                      class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                  </div>
                  <p class="fw-bold text-light">
                    Consultoria Completa
                  </p>
                  <p class="text-light">
                    AEP, AET e ARP com laudos técnicos precisos e alinhados às normas vigentes.
                  </p>
                </div>

                <div class="bg-light bg-opacity-10 text-light p-4 rounded-4 hover-up">
                  <div class="mb-3">
                    <font-awesome-icon icon="fa-solid fa-person-walking"
                      class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                  </div>
                  <p class="fw-bold text-light">
                    Ginástica Laboral
                  </p>
                  <p class="text-light">
                    Programas de bem-estar e prevenção no dia a dia.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- quem sou -->
      <section class="bg-light">
        <div class="container py-5">
          <div class="row">
            <div class="col-lg-6 align-self-center mb-3" v-reveal="'bottom'">
              <p class="text-principal fs-5">
                <font-awesome-icon icon="fa-solid fa-caret-right" />
                Quem Sou
              </p>

              <p class="display-5 text-green ff-bree">
                Experiência, Técnica e Acolhimento em Bauru e Região
              </p>

              <p class="fs-5 mb-4">
                Sou profissional de Educação Física e especialista em saúde corporativa com mais de 12 anos de
                trajetória. Minha missão é transformar ambientes de trabalho através da Consultoria em Ergonomia
                e Ginástica Laboral, unindo rigor técnico e um olhar humanizado para garantir que sua empresa seja
                um lugar de saúde e alta performance.
              </p>

              <RouterLink to="/sobre" class="btn btn-green px-4 py-2 rounded-4 fs-5">
                <font-awesome-icon icon="fa-solid fa-user" />
                Saiba mais
              </RouterLink>
            </div>

            <div class="col-lg-6">
              <div class="p-3 p-lg-5 bg-green rounded-4">

                <p class="text-light" v-for="value in aboutContent" :key="value.id" v-reveal="'bottom'">
                  {{ value.pretitle }}
                  <br>
                  <span class="text-principal fs-4 ff-bree fst-italic">{{ value.title }}</span>
                  <br>
                  {{ value.content }}
                  <hr class="thin-border-light" v-if="value.id < aboutContent.length">
                </p>

              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- sobre a ergonomia -->
      <section>
        <div class="container py-5">
          <div class="row mb-3">
            <p class="text-principal fs-5">
              <font-awesome-icon icon="fa-solid fa-caret-right" />
              Sobre a Ergonomia
            </p>
            <p class="text-center text-green ff-bree fs-1">
              Por que investir em Ergonomia?
            </p>
            <p class="text-center">
              A ergonomia vai muito além de um diferencial — ela é uma aliada essencial para o bem-estar e a segurança
              no ambiente de trabalho. Seguir as diretrizes da NR-17 é uma forma de cuidar das pessoas e também de
              manter a empresa protegida e organizada. Quando aplicada em empresas, clínicas e indústrias, a ergonomia
              contribui para prevenir dores, melhorar a qualidade de vida dos colaboradores e fortalecer a segurança
              jurídica do negócio, tudo de forma consciente e responsável.
            </p>
          </div>
          <div class="row d-flex justify-content-center">
            <div class="col-md-6 col-lg-4 mb-4" v-reveal="'bottom'" v-for="card in ergonomicList" :key="card.id">
              <div class="p-4 bg-light rounded-4 hover-up-wb">
                <font-awesome-icon :icon="card.icon"
                  class="text-principal bg-warning bg-opacity-10 p-3 rounded-4 fs-5" />
                <p class="ff-bree fs-5 mb-1">
                  {{ card.title }}
                </p>
                <p class="mb-1">
                  {{ card.content }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- ginástica laboral -->
      <section class="bg-light">
        <div class="container py-5">
          <div class="row mb-3">
            <div class="col-lg-6 align-self-center" v-reveal="'bottom'">
              <p class="text-principal fs-5 text-center">
                <font-awesome-icon icon="fa-solid fa-caret-right" />
                Ginástica Laboral: Movimento que transforma
              </p>
              <p class="text-center text-green ff-bree fs-1">
                O intervalo que gera produtividade
              </p>
              <p class="text-center">
                Minhas sessões de Ginástica Laboral são planejadas para quebrar a monotonia muscular e mental.
                Com foco em prevenção e integração, levo o movimento para dentro das empresas, reduzindo dores
                e fortalecendo o espírito de equipe
              </p>
            </div>
            <div class="col-lg-6 d-none d-lg-block" v-reveal="'bottom'">
              <img :src="NatiBg" alt="Profissional Natalia Mathias"
                class="img-fluid border-bottom border-5 border-success">
            </div>
          </div>
        </div>
      </section>

      <!-- galeria -->
      <section>
        <div class="container py-5">
          <div class="row" v-reveal="'bottom'">
            <p class="text-principal fs-5">
              <font-awesome-icon icon="fa-solid fa-caret-right" />
              Galeria de Fotos
            </p>
          </div>
          <div class="row g-3">
            <div v-for="(src, index) in images" :key="index" class="col-6 col-md-4 col-lg-3">
              <img :src="src" class="img-fluid rounded-3 cursor-pointer hover-up" @click="() => showImg(index)"
                style="object-fit: cover; height: 200px; width: 100%; cursor: pointer;" />
            </div>
          </div>

          <VueEasyLightbox :visible="visibleRef" :imgs="images" :index="indexRef" @hide="onHide" />
        </div>
      </section>

      <!-- call to action -->
      <section class="bg-warning-subtle">
        <div class="container py-5">
          <div class="row" v-reveal="'bottom'">
            <div class="col-lg-6 mx-auto">
              <p class="text-green fs-1 ff-bree text-center">
                Sua empresa com o melhor ambiente de trabalho possível
              </p>
              <p class="text-center fs-5">
                Entre em contato e descubra como podemos ajudar sua empresa a proteger seus funcionários, reduzir riscos
                e adequar à NR-17.
              </p>
              <p class="text-center">
                <a href="mailto:contato@nataliamathiasergo.com.br"
                  class="btn btn-default btn-lg px-4 py-2 rounded-3 mb-3 mb-lg-0">
                  <font-awesome-icon icon="fa-solid fa-file-lines" />
                  Solicitar Orçamento
                </a>
                <a href="https://wa.me/5514996880711" class="btn btn-default btn-lg px-4 py-2 rounded-3 ms-lg-3">
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
  min-height: 800px;
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

.cursor-pointer {
  cursor: pointer;
  transition: transform 0.3s ease;
}

.cursor-pointer:hover {
  transform: scale(1.03);
  filter: brightness(0.9);
}
</style>