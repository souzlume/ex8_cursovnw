<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";
const menuAberto = ref(false);
const toggleMenu = () => { menuAberto.value = !menuAberto.value; };
</script>

<template>
  <header>
    <img src="../assets/logo.svg" alt="Logo" />

    <section class="navegation">
      <div class="busca">
        <a href="">
          <Icon icon="basil:search-outline" width="33" height="33" />
        </a>
      </div>

      <nav :class="['menu', { mostrar: menuAberto }]">
        <ul>
          <li><a href="">Início</a></li>
          <li><a href="">Galeria</a></li>
          <li><a href="">Favoritos</a></li>
          <li>
            <a href="">
              <Icon icon="bi:person-fill" width="30" height="30" />
            </a>
          </li>
        </ul>
      </nav>
    </section>

    <button class="btn_menu" @click="toggleMenu">
      <Icon icon="jam:menu" width="33" height="33" />
    </button>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  padding: 2rem;
  box-shadow: 1px 1px 5px #262626;

  ul {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
    list-style: none;
  }

  a {
    text-decoration: none;
    color: #262626;

    &:hover {
      color: #e1306c;
      transition: 0.3s;
    }
  }
}

.navegation {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: end;
  margin: 0 2rem;
}

.btn_menu {
  background-color: transparent;
  border: none;
  cursor: pointer;
  display: block;

  &:hover {
    color: #e1306c;
    transition: 0.3s;
  }
}

.menu {
  display: none;
}

.mostrar {
  display: flex;
  width: 50%;
  height: auto;
  position: absolute;
  top: 100px;
  right: 0;
  background-color: #f1f1f1;
  box-shadow: 1px 1px 10px #a7a7a7;
  border-bottom-left-radius: 10px;
  border-top-left-radius: 10px;
}

@media (min-width: 769px) {
  header {
    ul {
      display: flex;
      flex-direction: row;
      gap: 3rem;
      align-items: center;
    }
  }

  .menu {
    display: flex;
  }

  .btn_menu {
    display: none;
  }

  .navegation {
    gap: 2rem;
  }
}
</style>
