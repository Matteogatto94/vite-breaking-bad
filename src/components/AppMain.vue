<script>
import CharactersList from './CharactersList.vue'
import SelectForm from './SelectForm.vue'
export default {
    name: 'AppMain',
    components: {
        SelectForm,
        CharactersList
    }

}
</script>

<template>

    <main>

        <SelectForm />
        <CharactersList />



    </main>

</template>

<style lang="scss">

</style>