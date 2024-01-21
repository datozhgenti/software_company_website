<template>
  <section class="hero-section">
    <div class="wrapper">
      <div
        class="hero-section-content flex justify-center align-center relative"
      >
        <div class="left">
          <h1 class="lite-h1">
            Great
            <span class="product bg-clip-text transparent inter-700"
              >Product</span
            >
            <span class="build inter-800"> is built by great</span>
            <span class="teams inter-800 bg-clip-text transparent"> teams</span>
          </h1>
          <p class="default-lg">
            We help build and manage a team of world-class developers to bring
            your vision to life
          </p>
          <div class="btn-wrapper">
            <button class="btn-lg border-none">Let’s get started!</button>
          </div>
        </div>
        <div class="right">
          <img
            src="@/assets/images/hero-image.svg"
            alt="hero image"
            class="hero-image"
          />
        </div>
        <img
          src="@/assets/icons/ellipse.svg"
          alt="ellipse"
          class="big-ellipse absolute"
        />
      </div>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style scoped>
/* content styles */

.hero-section-content {
  padding: 9.25rem 6.5rem 6.69rem 11.94rem;
}

/* text styles */
h1 .product {
  background-image: linear-gradient(
    180deg,
    #de4396 0%,
    rgba(13, 28, 159, 0) 100%
  );
}

h1 .build,
h1 .teams {
  font-size: 3.3125rem;
}

h1 .teams {
  background-image: linear-gradient(225deg, #f7666f 0%, #406aff 100%);
}

p {
  margin: 1.75rem 0 4.69rem;
}

/* button styles */

.btn-wrapper button {
  border-radius: 0.3125rem;
  background: #3d63ea;
  box-shadow: 0px 4px 49px 0px rgba(0, 0, 0, 0.15);
  padding: 1.1875rem 1.875rem;
}

/* hero image styles */

.hero-image {
  width: 38.375rem;
  height: 34.125rem;
}

/* big ellipse styles */

.big-ellipse {
  bottom: -2.25rem;
  left: 33.3%;
}

/* responsive styles */

@media (max-width: 76.4375rem) {
  .hero-section-content {
    flex-wrap: wrap;
    row-gap: 1.5rem;
  }
}

@media (max-width: 58.125rem) {
  .hero-image,
  .right {
    width: 100%;
  }

  .hero-section-content {
    padding: 9.25rem 0.5rem 6.69rem 0.5rem;
  }
}
</style>
