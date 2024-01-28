<template>
  <header class="fixed bg-base-white" ref="header">
    <div class="wrapper">
      <div class="header-content flex space-between align-center">
        <div class="icon-wrapper">
          <a href="#" class="flex align-center">
            <img src="@/assets/icons/brand-icon.svg" alt="brand icon" />
            <span class="inspiration-400">Ik developers</span>
          </a>
        </div>
        <nav class="desktop-nav">
          <ul class="flex space-between">
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#"> About us</a>
            </li>
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#"> Services</a>
            </li>
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#">
                Case Studies</a
              >
            </li>
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#"> Blog</a>
            </li>
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#">
                How it Works</a
              >
            </li>
            <li>
              <a class="headings-h6 gray-700 capitalize" href="#"> Hire</a>
            </li>
          </ul>
        </nav>
        <div class="burger-icon-wrapper justify-end display-none">
          <img
            v-if="mobileNavOn"
            src="@/assets/icons/close.svg"
            alt="close burger menu button"
            class="close-icon"
            @click="closeMobileNav"
          />
          <img
            v-else
            src="@/assets/icons/burger.svg"
            alt="burger menu button"
            class="burger-icon"
            @click="openMobileNav"
          />
        </div>

        <div class="button-wrapper">
          <button class="btn-lg pointer border-none">Contact us</button>
        </div>
      </div>
    </div>
  </header>
  <nav
    class="mobile-nav fixed overflow-hidden text-align-center bg-base-white"
    ref="mobileNav"
  >
    <ul>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#"> About us</a>
      </li>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#"> Services</a>
      </li>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#">
          Case Studies</a
        >
      </li>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#"> Blog</a>
      </li>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#">
          How it Works</a
        >
      </li>
      <li>
        <a class="headings-h6 gray-700 capitalize inline" href="#"> Hire</a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { ref, onMounted } from "vue";

const mobileNav = ref(null);

const header = ref(null);

const mobileNavOn = ref(false);

function openMobileNav() {
  const mobileNavHeight = mobileNav.value.scrollHeight;

  mobileNav.value.style.height = `${mobileNavHeight}px`;

  mobileNav.value.style.boxShadow =
    "0px 0.25rem 2.5rem 0.8125rem rgba(0, 0, 0, 0.1)";

  mobileNavOn.value = true;
}

function closeMobileNav() {
  mobileNav.value.style.height = `0px`;
  mobileNavOn.value = false;

  setTimeout(() => {
    mobileNav.value.style.boxShadow = "none";
  }, 500);
}

onMounted(() => {
  mobileNav.value.style.top = `${getComputedStyle(header.value).height}`;
});
</script>

<style scoped>
/* header styles */

header {
  padding: 0.625rem 1.5625rem;
  top: 0;
  left: 0;
  right: 0;
  box-shadow: 0px 0.25rem 2.5rem 0.8125rem rgba(0, 0, 0, 0.1);
}

header,
.mobile-nav {
  z-index: 100;
}

/* brand image styles */
.icon-wrapper img {
  width: 1.83719rem;
  height: 1.37781rem;
}

.icon-wrapper span {
  font-size: 1.5rem;
  color: #000;
}

.icon-wrapper {
  padding: 1.08813rem 2.07881rem 1.06794rem 0.89675rem;
}

/* nav styles */

.desktop-nav {
  flex-basis: 40.3125rem;
}

nav ul {
  padding: 0.625rem 0rem;
}

.mobile-nav {
  height: 0;
  left: 0;
  right: 0;
  transition: height 1s;
}

.mobile-nav li + li {
  margin-top: 0.5rem;
}

/* button styles */

.button-wrapper button {
  padding: 0.875rem 1.5625rem;
  border-radius: 0.3125rem;
  background: linear-gradient(225deg, #6675f7 0%, #57007b 100%);
}

/* burger icon styles */
.burger-icon-wrapper img {
  width: 2.625em;
  height: 2.625em;
}

/* responsive designs */

@media (max-width: 64rem) {
  .desktop-nav {
    display: none;
  }

  .burger-icon-wrapper {
    display: flex;
    order: 3;
  }

  .button-wrapper {
    flex-grow: 1;
    display: flex;
    justify-content: flex-end;
    padding-right: 0.5rem;
  }
}

@media (max-width: 24.0625rem) {
  .icon-wrapper span {
    display: none;
  }

  .icon-wrapper {
    padding-left: 0;
  }
}
</style>
