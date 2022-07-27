<template>
  <nav class="nav" ref="nav">
    <a class="nav__link">Filter 1</a>
    <a class="nav__link">Filter 2</a>
    <a class="nav__link">Filter 3</a>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const nav = ref();

let lastScrollY = window.scrollY;

window.addEventListener("scroll", () => {
  if (lastScrollY < window.scrollY) {
    nav.value.classList.add("nav__hidden");
  } else {
    nav.value.classList.remove("nav__hidden");
  }

  lastScrollY = window.scrollY;
});
</script>

<style lang="scss" scoped>
$nav-height: 50px;

.div {
  top: 100px;
}

.nav {
  z-index: 2;
  width: 100%;
  height: $nav-height;
  position: fixed;
  top: 50px;
  left: 0;
  background: #a8abbb;
  display: flex;
  align-items: center;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.2s;

  &__hidden {
    transform: translateY(calc(-2 * $nav-height));
    box-shadow: none;
  }

  &__link {
    color: #ffffff;
    text-decoration: none;
    margin: 0 1em;
    font-weight: bold;
  }
}
</style>
