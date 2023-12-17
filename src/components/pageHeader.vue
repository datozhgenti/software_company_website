<template>
  <header class="bg-white nav-box-shadow flex space-between align-center fixed">
    <div class="icon-wrapper">
      <a href="#" class="block">
        <img
          src="@/assets/icons/brand.svg"
          alt="brand icon"
          class="brand-icon block"
        />
      </a>
    </div>
    <nav class="desktop-nav">
      <ul class="flex space-between">
        <li v-for="link of links" :key="link">
          <a :href="link.href" class="gray-700 font-medium block">{{
            link.name
          }}</a>
        </li>
      </ul>
    </nav>
    <div class="burger-image-wrapper justify-end">
      <img
        src="@/assets/icons/burger.svg"
        alt="burder icon"
        class="burger-icon block"
      />
    </div>

    <div class="btn-wrapper shrink-0">
      <button class="block pointer gray-50 font-semibold">Contact us</button>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { name: "About us", href: "#" },
        { name: "Services", href: "#" },
        { name: "Case Studies", href: "#" },
        { name: "Blog", href: "#" },
        { name: "How it Works", href: "#" },
        { name: "Hire", href: "#" },
      ],
    };
  },
};
</script>

<style scoped>
header {
  padding: 0.625rem 1.5625rem;
  top: 0;
  left: 0;
  right: 0;
}

.brand-icon {
  width: 1.875rem;
  height: 1.4375rem;
}

nav {
  flex-basis: 40.3125rem;
}

ul {
  padding: 0.625rem 0rem;
}

a {
  line-height: 1.5625rem;
}

button {
  border-radius: 0.3125rem;
  background: linear-gradient(225deg, #6675f7 0%, #57007b 100%);
  padding: 0.875rem 1.5625rem;
  font-size: 0.875rem;
  line-height: 0.875rem;
  margin-left: 1.25rem;
}

.icon-wrapper {
  padding: 1.08813rem 2.07881rem 1.06794rem 0.89675rem;
}

.burger-icon {
  width: 2.625rem;
  height: 2.625rem;
}

.burger-image-wrapper {
  display: none;
  order: 1;
}

@media (max-width: 45.9375rem) {
  .desktop-nav {
    display: none;
  }

  .burger-image-wrapper {
    display: flex;
  }

  .btn-wrapper {
    flex-grow: 1;
    display: flex;
    justify-content: flex-end;
  }

  button {
    margin: 0 0.3125rem 0 0;
  }
}
</style>
