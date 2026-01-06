<script setup>
import Card from "./Card.vue";
import { ref } from "vue";
import axios from "axios";
const imagens = ref([]);
async function carregarImagens() {
    const res = await axios.get("https://picsum.photos/v2/list?page=2&limit=30");
    imagens.value = res.data;
    console.log(res);
}
carregarImagens();
</script>

<template>
    <section>
        <h2>Inspire-se</h2>
        <section class="cards">
            <Card v-for="img in imagens" :imagem="img.download_url" />
        </section>
    </section>
</template>

<style scoped lang="scss">
h2 {
    font-weight: 400;
    margin: 2rem;
}

.cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
</style>