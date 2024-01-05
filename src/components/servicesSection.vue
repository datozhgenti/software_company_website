<template>
  <section class="services-section bg-shade-light">
    <h2 class="gray-900 font-bold text-align-center">Services we offer</h2>
    <div class="services-slider">
      <div
        class="slider-cards flex justify-center align-start overflow-hidden"
        @pointerdown="pointerStart"
        @pointerup="pointerEnd"
      >
        <div
          class="slider-card shrink-0"
          v-for="(card, index) in cards"
          :key="card"
          :class="{ 'active-card': index === activeIndex }"
          ref="sliderCards"
        >
          <div class="icon-wrapper">
            <img :src="card.imgUrl" alt="mobile icon" class="block" />
          </div>
          <h4 class="gray-800 font-semibold">
            {{ card.title }}
          </h4>
          <p class="gray-600">
            {{ card.paragraph }}
          </p>
        </div>
      </div>
      <div class="slider-nodes-wrapper flex justify-center align-center">
        <div class="slider-nodes flex align-center">
          <div
            class="slider-node border-circle pointer"
            v-for="(n, index) in cards.length"
            :class="{ active: index === activeIndex }"
            :key="n"
            @click="slide(index)"
          ></div>
        </div>
        <div class="slider-numb-wrapper"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { onMounted } from "vue";

const cards = ref([
  {
    imgUrl: require("@/assets/icons/mobile.svg"),
    title: "Mobile App Development",
    paragraph:
      "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },

  {
    imgUrl: require("@/assets/icons/mobile.svg"),
    title: "Mobile App Development",
    paragraph:
      "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    imgUrl: require("@/assets/icons/code.svg"),
    title: "Web Design & Development",
    paragraph:
      "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    imgUrl: require("@/assets/icons/dashboard.svg"),
    title: "Software Testing Service",
    paragraph:
      "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
  {
    imgUrl: require("@/assets/icons/dashboard.svg"),
    title: "Software Testing Service",
    paragraph:
      "A Website is an extension of yourself and we can help you to express it properly. Your website is your number one marketing asset because we live in a digital age.",
  },
]);

const activeIndex = ref(Math.floor(cards.value.length / 2));

const sliderCards = ref(null);

let left = 0;

function slide(index) {
  const oldActiveCard = sliderCards.value[activeIndex.value];

  const oldRect = oldActiveCard.getBoundingClientRect();

  activeIndex.value = index;

  const newActiveCard = sliderCards.value[activeIndex.value];

  const newRect = newActiveCard.getBoundingClientRect();

  left += oldRect.left - newRect.left;

  for (let card of sliderCards.value) {
    if (card === newActiveCard) {
      card.style.transform = `translate(${left / 16}rem,2.44rem)`;
    } else {
      card.style.transform = `translate(${left / 16}rem)`;
    }
  }
}

let pointerStartX = 0;

function pointerStart(e) {
  pointerStartX = e.clientX;
  console.log("start");
}

function pointerEnd(e) {
  const pointerEndX = e.clientX;

  console.log("end");
  let active = activeIndex.value;

  if (pointerStartX - pointerEndX > 0) {
    active++;
    if (active === cards.value.length) {
      active = cards.value.length - 1;
    }
    slide(active);
  } else if (pointerStartX - pointerEndX < 0) {
    active--;
    if (active < 0) {
      active = 0;
    }
    slide(active);
  }
}

onMounted(() => {
  slide(activeIndex.value);
});
</script>

<style scoped>
h2 {
  font-size: 2.1875rem;
  line-height: 3.4375rem;
}

img {
  width: 2.625rem;
  height: 2.625rem;
}

.services-section {
  padding: 2.88rem 0 3.56rem;
}

.services-slider {
  margin-top: 4.56rem;
}

.slider-cards {
  gap: 2.44rem;
  height: 20.375rem;
}

.slider-card.active-card {
  background: linear-gradient(white, white) padding-box,
    var(--Gradient-Primary-bg) border-box;
  border: 1px solid transparent;
}

.active-card h4 {
  background-clip: text;
  color: transparent;
  background-image: var(--Gradient-Primary-bg);
}

.slider-card {
  width: 20.8125rem;
  border-radius: 0.4375rem;
  background: #fafafa;

  box-shadow: 0px 4px 30px 0px rgba(0, 0, 0, 0.05);

  padding: 2.25rem 1rem;
  transition: transform 1s;
  touch-action: none;
}

h4 {
  padding-block: 1.25rem;
  font-size: 1.25rem;
  line-height: 136.523%;
}

p {
  font-size: 0.875rem;
  line-height: 162.023%;
}

.slider-nodes-wrapper {
  margin-top: 2.56rem;
}

.slider-node {
  width: 0.8125rem;
  height: 0.8125rem;
  border: 1px solid var(--Gray-gray-400);
}

.slider-nodes {
  gap: 0.5rem;
}

.slider-node.active {
  background: var(--Gradient-Primary-bg);
  border: none;
  width: 1.125rem;
  height: 1.125rem;
}
</style>
