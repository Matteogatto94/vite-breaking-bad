<script>
import { store } from '../store.js'
export default {
    name: 'SelectForm',
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <div class="container">
        <select v-model="store.categorySelector" @change="$emit('findCategory')">
            <option selected>Select Category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Better Call Saul">Better Call Saul</option>
        </select>
    </div>

</template>

<style lang="scss">
select {
    padding: 0.5rem 0.5rem;
    border-radius: 10px;
}
</style>