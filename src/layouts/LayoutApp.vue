<template>
  <div>
    <section class="navbar-slot">
      <slot name="navbar"></slot>
    </section>
    <section class="carousel-slot">
      <slot name="carousel-img"></slot>
    </section>
    <section class="form-random-movie-slot">
      <slot name="form-random-movie"></slot>
    </section>
    <section class="card-movie-selected-slot">
      <slot name="card-movie-selected"></slot>
    </section>
    <section class="footer-slot">
      <slot name="footer"></slot>
    </section>
  </div>
</template>
