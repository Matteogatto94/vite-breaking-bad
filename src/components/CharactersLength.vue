<script>
import { store } from '../store.js'
export default {
    name: 'CharactersLength',
    data() {
        return {
            store
        }
    },
    computed: {
        totalResults() {
            return this.store.characters.length
        }
    }
}
</script>

<template>
    <div class="characters_found">
        <p v-if="store.characters != null">Found {{ totalResults }} characters</p>
    </div>

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