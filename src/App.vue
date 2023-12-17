<template>
  <pageHeader></pageHeader>
</template>

<script setup>
import pageHeader from "./components/pageHeader.vue";
</script>

<style>
/* css variables */

:root {
  --base-white: #fff;
  --Gray-gray-700: #4a5568;
  --Gray-gray-50: #fafafa;
}

/* all element styles */

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* background colors */

.bg-white {
  background: var(--base-White);
}

/* box shadows */

.nav-box-shadow {
  box-shadow: 0px 4px 40px 0px rgba(0, 0, 0, 0.1);
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

/* align items */

.align-center {
  align-items: center;
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

/* color */

.gray-700 {
  color: var(--Gray-gray-700);
}

.gray-50 {
  color: var(--Gray-gray-50);
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

.font-medium {
  font-family: inter-medium, sans-serif;
}

.font-semibold {
  font-family: inter-semibold, sans-serif;
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
</style>
