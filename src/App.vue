<template>
  <pageHeader></pageHeader>
  <main>
    <pageHero></pageHero>
  </main>
</template>

<script setup>
import pageHeader from "@/components/pageHeader.vue";
import pageHero from "./components/pageHero.vue";
</script>

<style>
/* colors */

:root {
  --Gray-gray-50: #fafafa;
  --Gray-gray-700: #4a5568;
  --Gray-gray-900: #1a202c;
  --base-white: #fff;
}

.transparent {
  color: transparent;
}

/* styles for all element */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* content wrapper styles  */

.wrapper {
  max-width: 90rem;
  margin: 0 auto;
}

/* anchor tag styles */

a {
  text-decoration: none;
}

/* font-family styles */

@font-face {
  font-family: inspiration-400;
  src: url("@/assets/fonts/inspiration/Inspiration-Regular.ttf");
}

@font-face {
  font-family: inter-300;
  src: url("@/assets/fonts/inter/Inter-300.ttf");
}

@font-face {
  font-family: inter-400;
  src: url("@/assets/fonts/inter/Inter-400.ttf");
}

@font-face {
  font-family: inter-500;
  src: url("@/assets/fonts/inter/Inter-500.ttf");
}

@font-face {
  font-family: inter-600;
  src: url("@/assets/fonts/inter/Inter-600.ttf");
}

@font-face {
  font-family: inter-700;
  src: url("@/assets/fonts/inter/Inter-700.ttf");
}

@font-face {
  font-family: inter-800;
  src: url("@/assets/fonts/inter/Inter-800.ttf");
}

.inspiration-400 {
  font-family: inspiration-400, cursive;
}

.inter-700 {
  font-family: inter-700, sans-serif;
}

.inter-800 {
  font-family: inter-800, sans-serif;
}

/* display styles */

a,
img {
  display: block;
}

.flex {
  display: flex;
}

.display-none {
  display: none;
}

.inline {
  display: inline;
}

/* align-items styles */

.align-center {
  align-items: center;
}

/* justify-content styles */

.space-between {
  justify-content: space-between;
}

.justify-end {
  justify-content: flex-end;
}

.justify-center {
  justify-content: center;
}

/* ul styles */

ul {
  list-style: none;
}

/* headings styles */

.headings-h6 {
  color: var(--Gray-gray-700);
  font-family: inter-500, sans-serif;
  font-size: 1rem;
  line-height: 1.5625rem;
}

.lite-h1 {
  color: var(--Gray-gray-900);
  font-family: inter-300, sans-serif;
  font-size: 2.8125rem;
  line-height: 4.4375rem;
}
/* cursor styles */

.pointer {
  cursor: pointer;
}

/* btn text styles */

.btn-lg {
  color: var(--Gray-gray-50);

  font-family: inter-600;
  font-size: 0.875rem;
  line-height: 0.875rem;
}

/* text-transform styles */

.capitalize {
  text-transform: capitalize;
}

/* position styles */

.fixed {
  position: fixed;
}

.absolute {
  position: absolute;
}

.relative {
  position: relative;
}

/* overflow styles */

.overflow-hidden {
  overflow: hidden;
}

/* border styles*/

.border-none {
  border: none;
}

/* text-align styles */

.text-align-center {
  text-align: center;
}

/* background styles */

.bg-base-white {
  background: var(--base-white);
}

/* background-clip styles */

.bg-clip-text {
  background-clip: text;
}

/* text styles */

.default-lg {
  color: var(--Gray-gray-700);

  font-family: Inter-400;
  font-size: 1.125rem;
  line-height: 2.25rem;
}

/* ellipse styles */

.big-ellipse {
  width: 4.5rem;
  height: 4.5rem;
}
</style>
