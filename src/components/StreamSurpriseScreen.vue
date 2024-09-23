<script setup></script>

<template>
  <div class="container-fluid">
    <figure>
      <img src="@/assets/img/kuromi.png" alt="Kuromi Logo" />
    </figure>
    <h1>Stream<span>Surprise</span></h1>
  </div>
</template>

<style scoped>
h1 {
  font-size: 2rem;
  font-weight: bold;
  color: var(--kuromi-white);
  text-transform: uppercase;
  letter-spacing: 1px;
  text-align: center;
  margin-top: 10px;
}

span {
  color: var(--kuromi-purple);
  font-weight: bold;
}

div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: var(--kuromi-dark-bg);
  padding: 10px;
}

img {
  width: 150px;
  animation: pulse 3s infinite ease-in-out;
}

figure {
  background-color: var(--kuromi-purple);
  border: 2px solid var(--kuromi-hover);
  border-radius: 50%;
  padding: 8px;
  box-shadow: 0 0 10px var(--kuromi-hover);
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
  100% {
    transform: scale(1);
  }
}

@media (min-width: 768px) {
  h1 {
    font-size: 3rem;
    letter-spacing: 2px;
  }

  img {
    width: 180px;
  }

  figure {
    border: 3px solid var(--kuromi-hover);
    padding: 10px;
    box-shadow: 0 0 15px var(--kuromi-hover);
  }
}

@media (min-width: 1200px) {
  h1 {
    font-size: 3.5rem;
  }

  img {
    width: 200px;
  }
}
</style>
