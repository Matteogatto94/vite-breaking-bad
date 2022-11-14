<script>
import { store } from '../store.js';
import SingleCharacter from './SingleCharacter.vue'
export default {
    name: 'CharactersList',
    components: {
        SingleCharacter
    },
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <section class="Characters">
        <div class="container">
            <div class="cards">
                <div class="characters_found">
                    <p>Found {{ store.charactersLength }} characters</p>
                </div>
                <div class="row row-cols-md-5 g-4">
                    <SingleCharacter :character="character" v-for="character in store.characters" />
                </div>
            </div>

        </div>
    </section>

</template>

<style lang="scss">
.characters_found {
    background-color: black;
    color: white;
    text-transform: uppercase;
    font-weight: bold;
    padding: 2rem;
    margin-bottom: 1rem;
}
</style>