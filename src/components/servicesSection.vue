<template>
  <section class="services-section">
    <div class="wrapper">
      <div class="services-section-content relative">
        <h2 class="headings-h2 gray-900 text-align-center">
          Services we offer
        </h2>
        <div class="services-slider-wrapper flex justify-center">
          <div
            class="services-card flex-shrink-0"
            v-for="(servicesCard, index) of servicesCards"
            :key="servicesCard"
            :class="{ active: index === defaultActiveCard }"
          >
            <div
              class="image-wrapper border-cirle flex justify-center align-center"
            >
              <img :src="servicesCard.img" alt="code icon" />
            </div>
            <h4 class="headings-h4 gray-800">{{ servicesCard.title }}</h4>
            <p class="default gray-600">
              {{ servicesCard.desc }}
            </p>
          </div>
        </div>
        <div class="slider-nodes-wrapper flex justify-center align-center">
          <div
            class="slider-node border-cirle pointer"
            v-for="(n, index) in servicesCards.length"
            :key="n"
            :class="{ active: index === defaultActiveCard }"
          ></div>
        </div>
        <div class="slider-numb-wrapper flex align-center absolute">
          <h6 class="active-card-numb headings-h6 gray-500">01</h6>
          <div class="progress-bar bg-gray-300">
            <div class="progress bg-brand-primary h100"></div>
          </div>
          <h6 class="total-cards headings-h6 brand-primary">05</h6>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const servicesCards = ref([
  {
    img: require("@/assets/icons/mobile.svg"),
    title: "Mobile App Development",
    desc: "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    img: require("@/assets/icons/mobile.svg"),
    title: "Mobile App Development",
    desc: "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    img: require("@/assets/icons/code.svg"),
    title: "Web Design & Development",
    desc: "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    img: require("@/assets/icons/dashboard.svg"),
    title: "Software Testing Service",
    desc: "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    img: require("@/assets/icons/dashboard.svg"),
    title: "Software Testing Service",
    desc: "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
]);

const defaultActiveCard = ref(Math.floor(servicesCards.value.length / 2));
</script>

<style scoped>
/* section content styles */

.services-section {
  background: var(--Shade-light-background);
}

.services-section-content {
  padding: 2.88rem 0 3.56rem;
}

/* slider wrapper styles */

.services-slider-wrapper {
  margin-top: 4.56rem;
  gap: 2.44rem;
}

/* services card styles */

.services-card {
  flex-basis: 20.8125rem;
  padding: 2.55rem 1rem;
  border-radius: 0.4375rem;
  background: #fafafa;
  box-shadow: 0rem 0.25rem 1.875rem 0rem rgba(0, 0, 0, 0.05);
}

.image-wrapper,
.services-card.active {
  background: linear-gradient(#fafafa, #fafafa) padding-box,
    var(--Gradient-Primary-bg);
}

.services-card.active {
  border: 1px solid transparent;
  transform: translateY(2.44rem);
}

.services-card.active h4 {
  background-clip: text;
  color: transparent;
  background-image: var(--Gradient-Primary-bg);
}

.services-card .image-wrapper {
  width: 3.625rem;
  height: 3.625rem;
  border: 1px solid transparent;
}

.services-card .image-wrapper img {
  width: 2.625rem;
  height: 2.625rem;
}

.services-card h4 {
  margin: 1.25rem 0;
}

/* slider nodes styles */

.slider-nodes-wrapper {
  margin-top: 5rem;
  gap: 0.5rem;
}

.slider-node {
  width: 0.8125rem;
  height: 0.8125rem;
  border: 1px solid var(--Gray-gray-400);
}

.slider-node.active {
  width: 1.125rem;
  height: 1.125rem;
  background: var(--Gradient-Primary-bg);
}

/* slider-numb styles */

.slider-numb-wrapper {
  width: 10.25rem;
  gap: 0.5rem;
  bottom: 3.67rem;
  right: 12.6%;
}

.progress-bar {
  width: 6.9375rem;
  height: 0.1875rem;
}

.progress {
  width: 20%;
}
</style>
