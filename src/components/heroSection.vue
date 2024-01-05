<template>
  <section class="hero-section relative">
    <div class="hero-content flex center-margin align-center">
      <div class="left">
        <h1 class="gray-900 font-light">
          Great
          <span class="product background-clip-text transparent font-bold"
            >Product</span
          >
          is
          <span class="built font-extrabold">built by great</span>
          <span class="teams background-clip-text transparent font-extrabold">
            teams</span
          >
        </h1>
        <p class="gray-700">
          We help build and manage a team of world-class developers to bring
          your vision to life
        </p>
        <div>
          <button class="font-semibold gray-50">Let’s get started!</button>
        </div>
      </div>
      <div class="right">
        <img
          src="@/assets/images/hero.svg"
          alt="hero image"
          class="hero-img block"
        />
      </div>
    </div>
    <img
      src="@/assets/images/ellipse-180.svg"
      alt="ellipse"
      class="ellipse absolute z-index--1"
    />
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.hero-section {
  padding-top: 9.25rem;
  padding-bottom: 6.69rem;
}

h1 {
  font-size: 2.8125rem;
  line-height: 4.4375rem;
}

p {
  margin: 1.75rem 0 4.69rem;
  font-size: 1.125rem;
  line-height: 2.25rem;
}

button {
  padding: 1.1875rem 1.875rem;
  border-radius: 0.3125rem;
  background: #3d63ea;
  box-shadow: 0px 4px 49px 0px rgba(0, 0, 0, 0.15);
  font-size: 0.875rem;
  line-height: 0.875rem;
}

.product {
  background-image: linear-gradient(
    180deg,
    #de4396 0%,
    rgba(13, 28, 159, 0) 100%
  );
}

.built,
.teams {
  font-size: 3.3125rem;
}

.teams {
  background-image: linear-gradient(225deg, #f7666f 0%, #406aff 100%);
}

img.hero-img {
  width: 38.375rem;
  height: 34.125rem;
}

.hero-content {
  max-width: 71.6rem;
}

.ellipse {
  bottom: -2.25rem;
  left: 33.5%;
  width: 4.5rem;
  height: 4.5rem;
}

@media (max-width: 74.375rem) {
  .hero-content {
    flex-wrap: wrap;
    justify-content: center;
  }

  .hero-content .right {
    order: -1;
  }

  .hero-content .left {
    text-align: center;
  }
}

@media (max-width: 41.875rem) {
  img.hero-img {
    width: 100%;
    height: 50vh;
  }
}
</style>
