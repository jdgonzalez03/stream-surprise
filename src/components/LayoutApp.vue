<template>
  <div>
    <div class="navbar-slot">
      <slot name="navbar"></slot>
    </div>
    <div class="carousel-slot">
      <slot name="carousel-img"></slot>
    </div>
    <div class="form-random-movie-slot">
      <slot name="form-random-movie"></slot>
    </div>
    <div class="card-movie-selected-slot">
      <slot name="card-movie-selected"></slot>
    </div>
    <div class="footer-slot">
      <slot name="footer"></slot>
    </div>
  </div>
</template>
