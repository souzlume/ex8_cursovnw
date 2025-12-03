<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <header>
    <img src="../assets/logo.png" alt="Logo" />

    <nav>
      <ul>
        <li>
          <a href="">
            <Icon icon="material-symbols:search" width="24" height="24" />
          </a>
        </li>
        <li><a href="">inicio</a></li>
        <li><a href="">Galeria</a></li>
        <li><a href="">Favoritos</a></li>
        <li>
          <a href="">
            <Icon icon="material-symbols:person-outline" width="24" height="24" />
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2rem;

  ul {
    display: flex;
    align-items: center;
    list-style: none;
    gap: 1rem;
  }

  a {
    text-decoration: none;
    color: black;
  }
}
</style>
