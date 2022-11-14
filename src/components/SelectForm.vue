<script>
export default {
    name: 'SelectForm'
}
</script>

<template>

    <div class="container">
        <select>
            <option selected>Select Category</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>

</template>

<style lang="scss">
select {
    padding: 0.5rem 0.5rem;
    border-radius: 10px;
}
</style>