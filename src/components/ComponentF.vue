<template>
    <div>
        <h2>{{ name }}'s username is:{{ username }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ComponentF',
        inject: ['username', 'name']
    }
</script>

<style lang="scss" scoped>

</style>