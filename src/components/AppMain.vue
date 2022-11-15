<script>
import axios from 'axios'
import { store } from '../store.js'
import CharactersList from './CharactersList.vue'
import SelectForm from './SelectForm.vue'
export default {
    name: 'AppMain',
    components: {
        SelectForm,
        CharactersList
    },
    data() {
        return {
            store
        }
    },
    methods: {
        selectCategory() {
            const categorySelector = this.store.categorySelector
            const url = `${this.store.API_URL}?category=${categorySelector}`
            console.log(url);

            axios.get(url)
                .then(response => {
                    console.log(response);
                    store.characters = response.data
                    store.charactersLength = response.data.length
                })
                .catch(err => {
                    console.error(err.message);
                    store.error = err.message
                })
        }
    }

}
</script>

<template>

    <main>

        <SelectForm @findCategory="selectCategory" />
        <CharactersList />



    </main>

</template>

<style lang="scss">

</style>