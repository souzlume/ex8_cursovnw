<script setup></script>

<template>
  <section class="hero">
    <img src="../assets/fotografo.png" alt="Foto de alguém tirando foto" />
    <div class="texto">
      <h1>Onde a paisagem vira <span class="destaque">inspiração</span>.</h1>
      <p class="desc">
        Explore paisagens, cores e luzes que inspiram novas histórias através da
        fotografia.
      </p>
    </div>
  </section>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  padding: 2rem;
  align-items: center;
}

img {
  width: 70vw;
}

h1 {
  color: #262626;
  font-size: 3.4rem;
  text-align: center;
  margin: 1rem;

  .destaque {
    color: #e1306c;
    font-size: 4.5rem;
  }
}

.desc {
  color: #262626;
  text-align: center;
  font-size: 1.2rem;
  margin: 1rem;
}

.texto {
  margin: 1rem;
}

@media (min-width: 769px) {
  .hero {
    flex-direction: row-reverse;
    align-items: center;
    justify-content: space-between;
  }

  img {
    width: 35vw;
  }

  .texto {
    width: 50%;
  }

  h1,
  .desc {
    text-align: start;
  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 2.8rem;

    .destaque {
      font-size: 3.5rem;
    }
  }
}
</style>
