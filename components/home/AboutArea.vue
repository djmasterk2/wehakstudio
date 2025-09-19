<script setup>
import CountUp from "vue-countup-v3";

const counter_data = [
  {
    id: 1,
    title: "Years Of Experience",
    count: 8,
    cls: "plus",
  },
  {
    id: 2,
    title: "Completed Projects",
    count: 1,
    cls: "k-plus",
  },
  {
    id: 3,
    title: "Client Satisfactions",
    count: 90,
    cls: "percent",
  },
];
</script>

<template>
  <ClientOnly>
    <section id="about" class="about-area">
      <div class="container">
        <div class="row">
          <!-- START ABOUT TEXT DESIGN AREA -->
          <div class="col-lg-3 col-sm-3">
            <h2 class="about-pre-title">Acerca de nosotros</h2>
          </div>
          <div class="col-lg-9 col-sm-9">
            <div class="about-content-part wow fadeInUp delay-0-2s">
              <p>
                En We HAK creamos soluciones visuales estratégicas que conectan marcas con su audiencia.
                Somos una agencia creativa especializada en branding profesional,
                diseño web y gestión de redes sociales.
                Transformamos tus ideas en marcas con intención.
              </p>
            </div>
            <!-- START COUNTER DESIGN AREA -->
            <div
              class="hero-counter-area d-flex justify-content-between wow fadeInUp delay-0-4s"
            >
              <div
                v-for="(counter, i) in counter_data"
                :key="i"
                class="counter-item counter-text-wrap"
              >
                <span :class="`count-text d-flex justify-content-center ${counter.cls}`">
                  <count-up
                  :end-val="counter.count" 
                ></count-up>
                </span>
                <span class="counter-title">{{ counter.title }}</span>
              </div>
            </div>
            <!-- / END COUNTER DESIGN AREA -->
          </div>
          <!-- / END ABOUT TEXT DESIGN AREA -->
        </div>
      </div>
    </section>
  </ClientOnly>
</template>