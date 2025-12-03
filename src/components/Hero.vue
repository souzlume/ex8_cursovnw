<script setup></script>

<template>
  <section class="hero">
    <div>
      <h2>Onde a paisagem vira <span>inspiração</span>.</h2>
      <p>
        Explore paisagens, cores e luzes que inspiram novas histórias através da
        fotografia.
      </p>
    </div>

    <img src="../assets/fotografo.png" alt="Imagem ilustrativa" />
  </section>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 2rem;

  h2 {
    font-size: 2rem;
  }

  span {
    font-size: 3rem;
    color: #e1306c;
  }

  img {
    width: 40vw;
  }
}
</style>
