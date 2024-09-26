<template>
  <div>
    <section class="navbar-slot">
      <slot name="navbar"></slot>
    </section>
    <section class="carousel-slot">
      <slot name="carousel-img"></slot>
    </section>
    <section id="select-movie" class="select-movie-slot">
      <slot name="select-movie"></slot>
    </section>
    <section class="card-movie-selected-slot">
      <slot name="card-movie-selected"></slot>
    </section>
    <section class="footer-slot">
      <slot name="footer"></slot>
    </section>
  </div>
</template>

<style scoped>
.carousel-slot {
  padding-top: 40px;
  margin: 16px;
}

@media (min-width: 1200px) {
  .carousel-slot {
    margin: 0 auto;
    max-width: 1200px;
  }
}

.select-movie-slot {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
