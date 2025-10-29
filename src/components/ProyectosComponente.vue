<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Anime: Me encanta seguir diferentes series y explorar nuevos géneros.',
    'Videojuegos: Disfruto jugar todo tipo de videojuegos, desde aventuras hasta estrategia.',
    'Programación: Me apasiona aprender y crear proyectos de software, explorando nuevas tecnologías.',
    'Jugar con mi perra: Paso tiempo de calidad con mi mascota, divirtiéndonos y paseando juntos.'
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
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Anime: Me encanta seguir diferentes series y explorar nuevos géneros.
            </li>
            <li class="item">
                 Videojuegos: Disfruto jugar todo tipo de videojuegos, desde aventuras hasta estrategia.
            </li>
            <li class="item">
                Programación: Me apasiona aprender y crear proyectos de software, explorando nuevas tecnologías.
            </li>
            <li class="item">
                Jugar con mi perra: Paso tiempo de calidad con mi mascota, divirtiéndonos y paseando juntos.
            </li>
        </ul>
    </div> -->
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