<template>
  <pageHeader></pageHeader>
  <main>
    <pageHero></pageHero>
    <servicesSection></servicesSection>
  </main>
</template>

<script setup>
import pageHeader from "@/components/pageHeader.vue";
import pageHero from "./components/pageHero.vue";
import servicesSection from "./components/servicesSection.vue";
</script>

<style>
/* colors */

:root {
  --Gray-gray-50: #fafafa;
  --Gray-gray-300: #e2e8f0;
  --Gray-gray-400: #cbd5e0;
  --Gray-gray-500: #a0aec0;
  --Gray-gray-600: #718096;
  --Gray-gray-700: #4a5568;
  --Gray-gray-800: #2d3748;
  --Gray-gray-900: #1a202c;
  --base-white: #fff;
  --Shade-light-background: #f9f9ff;
  --Gradient-Primary-bg: linear-gradient(225deg, #f76680 0%, #57007b 100%);
  --Brand-Primary-bg: #57007b;
}

.transparent {
  color: transparent;
}

.gray-500 {
  color: var(--Gray-gray-500);
}

.gray-600 {
  color: var(--Gray-gray-600);
}

.gray-700 {
  color: var(--Gray-gray-700);
}

.gray-800 {
  color: var(--Gray-gray-800);
}

.gray-900 {
  color: var(--Gray-gray-900);
}

.brand-primary {
  color: var(--Brand-Primary-bg);
}

/* styles for all element */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: inter-400, sans-serif;
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

.lite-h1 {
  font-family: inter-300, sans-serif;
  font-size: 2.8125rem;
  line-height: 4.4375rem;
}

.headings-h2 {
  font-size: 2.1875rem;
  font-family: inter-700, sans-serif;
  line-height: 3.4375rem;
}

.headings-h4 {
  font-size: 1.25rem;
  font-family: inter-600, sans-serif;
  line-height: 136.523%;
}

.headings-h6 {
  font-family: inter-500, sans-serif;
  font-size: 1rem;
  line-height: 1.5625rem;
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

.bg-gray-300 {
  background: var(--Gray-gray-300);
}

.bg-brand-primary {
  background: var(--Brand-Primary-bg);
}

/* background-clip styles */

.bg-clip-text {
  background-clip: text;
}

/* text styles */

.default {
  font-size: 0.875rem;
  line-height: 162.023%;
}

.default-lg {
  font-family: Inter-400;
  font-size: 1.125rem;
  line-height: 2.25rem;
}

/* ellipse styles */

.big-ellipse {
  width: 4.5rem;
  height: 4.5rem;
  z-index: -1;
}

/* border-radius styles */

.border-cirle {
  border-radius: 50%;
}

/* height styles */

.h100 {
  height: 100%;
}

/* flex-shrink */

.flex-shrink-0 {
  flex-shrink: 0;
}
</style>
