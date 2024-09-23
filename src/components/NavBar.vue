<template>
  <nav class="navbar bg-body-tertiary" data-bs-theme="dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img
          src="@/assets/img/kuromi-icon.png"
          alt="Logo"
          width="40"
          height="34"
          class="d-inline-block align-text-top"
        />
        <h1>Stream<span>Surprise</span></h1>
      </a>
      <a class="get-movie btn btn-outline-primary" href="#">Get a Movie</a>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background-color: var(--kuromi-dark-bg);
  padding: 15px 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
}

h1,
span {
  display: inline;
}

h1 {
  margin: 0;
  font-size: 1rem;
  font-weight: bold;
  color: var(--kuromi-white);
  text-transform: uppercase;
  letter-spacing: 1px;
  text-align: center;
  transition: color 0.3s;
}

span {
  color: var(--kuromi-purple);
  font-weight: bold;
}

a {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: color 0.3s;
}

a:hover h1 {
  color: var(--kuromi-purple);
}

img {
  margin-right: 10px;
}

.btn-outline-primary {
  --bs-btn-font-weight: 600;
  --bs-btn-color: var(--kuromi-purple);
  --bs-btn-bg: transparent;
  --bs-btn-border-color: var(--kuromi-purple);
  --bs-btn-hover-color: var(--kuromi-white);
  --bs-btn-hover-bg: var(--kuromi-purple); /* Morado más claro para hover */
  --bs-btn-hover-border-color: var(--kuromi-purple); /* Morado más claro para hover */
  --bs-btn-focus-shadow-rgb: var(--kuromi-purple); /* Sombra de enfoque con morado */
  --bs-btn-active-color: var(--bs-btn-hover-color);
  --bs-btn-active-bg: var(--kuromi-purple); /* Mantiene el morado brillante al presionar */
  --bs-btn-active-border-color: var(--kuromi-hover); /* Morado más claro para borde activo */
}

.get-movie:hover {
  transform: scale(1.05);
}

.get-movie:active {
  transform: scale(0.95);
}

@media (min-width: 576px) {
  .navbar {
    padding: 15px 20px;
  }

  h1 {
    font-size: 1.2rem;
  }

  img {
    width: 50px;
    height: auto;
  }
}

@media (min-width: 768px) {
  h1 {
    font-size: 1.5rem;
  }

  .navbar {
    padding: 15px 30px;
  }
}

@media (min-width: 992px) {
  h1 {
    font-size: 1.8rem;
  }
}
</style>
