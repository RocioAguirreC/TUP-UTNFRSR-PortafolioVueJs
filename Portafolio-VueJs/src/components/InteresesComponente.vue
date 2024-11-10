<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Contributor to open-source data projects, focusing on cleaning datasets, visualizing data, and providing insights. Active participant on GitHub, especially with data science repositories.',
    'Enjoy analyzing public datasets to uncover trends in fields like healthcare, education, or climate. Recently explored a project on air quality impact on public health.',
    'Passionate about understanding how users interact with applications. Conduct informal UX testing in personal projects to optimize user satisfaction.',
    'Enthusiast about transforming raw data into compelling visual stories that aid decision-making.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>
