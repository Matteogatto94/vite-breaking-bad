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
            let categorySelector = this.store.categorySelector
            let url = store.API_URL
            console.log(url);

            if (this.store.categorySelector !== 'Tutte Le Categorie') {
                url = `${this.store.API_URL}?category=${categorySelector}`
            }

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