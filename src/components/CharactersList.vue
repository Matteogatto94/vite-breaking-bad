<script>
import { store } from '../store.js';
import CharactersLength from './CharactersLength.vue'
import SingleCharacter from './SingleCharacter.vue'
export default {
    name: 'CharactersList',
    components: {
        SingleCharacter,
        CharactersLength
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
                <CharactersLength />
                <div class="row row-cols-md-5 g-4">
                    <SingleCharacter :character="character" v-for="character in store.characters" />
                </div>
            </div>

        </div>
    </section>

</template>

<style lang="scss">

</style>