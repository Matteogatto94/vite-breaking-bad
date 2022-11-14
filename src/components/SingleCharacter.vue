<script>
import { store } from '../store.js';
export default {
    name: 'SingleCharacter',
    props: {
        character: Object
    },

    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <div class="col">
        <div class="card">
            <img :src="character.img" :alt="character.name">
            <h2>{{ character.name }}</h2>
            <p class="category">{{ character.category }}</p>
            <p class="status">{{ character.status }}</p>
        </div>

    </div>
</template>

<style lang="scss">
.Characters {
    padding: 1rem;

    .cards {
        margin-top: 1rem;
        background-color: white;
        padding: 1.5rem;
    }

    .card {
        align-items: center;
        padding: 1rem;
        height: 450px;
        width: 250px;
        background-color: #2E3A46;

        h2 {
            color: white;
            font-size: 1rem;
            padding: 1rem;
        }

        p {
            color: darkgrey;
        }
    }

    img {
        width: 200px;
        height: 250px;
    }
}
</style>