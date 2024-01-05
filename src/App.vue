<template>
  <pageHeader></pageHeader>
  <main>
    <heroSection></heroSection>
    <servicesSection></servicesSection>
  </main>
</template>

<script setup>
import pageHeader from "./components/pageHeader.vue";
import heroSection from "./components/heroSection.vue";
import servicesSection from "./components/servicesSection.vue";
</script>

<style>
/* css variables */

:root {
  --base-white: #fff;
  --Gray-gray-700: #4a5568;
  --Gray-gray-50: #fafafa;
  --Gray-gray-900: #1a202c;
  --Gray-gray-800: #2d3748;
  --Shade-light-background: #f9f9ff;
  --Gray-gray-600: #718096;
  --Gradient-Primary-bg: linear-gradient(225deg, #f76680 0%, #57007b 100%);
  --Gray-gray-400: #cbd5e0;
}

/* all element styles */

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: inter-regular, sans-serif;
}

/* background colors */

.bg-white {
  background: var(--base-white);
}

.bg-shade-light {
  background: var(--Shade-light-background);
}

/* box shadows */

.nav-box-shadow {
  box-shadow: 0 0.25rem 2.5rem 0 rgba(0, 0, 0, 0.1);
}

.mobile-nav-box-shadow {
  box-shadow: 0 1.25rem 1.25rem 0px rgba(0, 0, 0, 0.1);
}

/* display props */

.flex {
  display: flex;
}

.block {
  display: block;
}

/* justify content */

.space-between {
  justify-content: space-between;
}

.justify-end {
  justify-content: flex-end;
}

.justify-center {
  justify-content: center;
}

/* align items */

.align-center {
  align-items: center;
}

.align-start {
  align-items: flex-start;
}

/* list */

ul {
  list-style: none;
}

/* anchor */

a {
  text-decoration: none;
}

/* position */

.fixed {
  position: fixed;
}

.absolute {
  position: absolute;
}

.relative {
  position: relative;
}

/* color */

.gray-50 {
  color: var(--Gray-gray-50);
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

.transparent {
  color: transparent;
}

/* fonts */

@font-face {
  font-family: inter-medium;
  src: url("@/assets/fonts/inter/Inter-Medium.ttf");
}

@font-face {
  font-family: inter-semibold;
  src: url("@/assets/fonts/inter/Inter-SemiBold.ttf");
}

@font-face {
  font-family: inter-light;
  src: url("@/assets/fonts/inter/Inter-Light.ttf");
}

@font-face {
  font-family: inter-bold;
  src: url("@/assets/fonts/inter/Inter-Bold.ttf");
}

@font-face {
  font-family: inter-extrabold;
  src: url("@/assets/fonts/inter/Inter-ExtraBold.ttf");
}

@font-face {
  font-family: inter-regular;
  src: url("@/assets/fonts/inter/Inter-Regular.ttf");
}

.font-medium {
  font-family: inter-medium, sans-serif;
}

.font-semibold {
  font-family: inter-semibold, sans-serif;
}

.font-light {
  font-family: inter-light, sans-serif;
}

.font-bold {
  font-family: inter-bold, sans-serif;
}

.font-extrabold {
  font-family: inter-extrabold, sans-serif;
}

/* button */

button {
  border: none;
}

button:focus {
  outline: none;
}

/* cursor */

.pointer {
  cursor: pointer;
}

/* flex shrink */

.shrink-0 {
  flex-shrink: 0;
}

/* text align */

.text-align-center {
  text-align: center;
}

/* background clip */

.background-clip-text {
  background-clip: text;
}

/* margin */

.center-margin {
  margin: 0 auto;
}

/* z-index */

.z-index--1 {
  z-index: -1;
}

/* border radius */

.border-circle {
  border-radius: 50%;
}

/* overflow-hidden */

.overflow-hidden {
  overflow: hidden;
}
</style>
