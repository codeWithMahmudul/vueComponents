<template>
    <div>
        <h2 v-bind="$attrs">{{ title }}</h2>
        <h2>Likes - {{ likes }}</h2>
    </div>
    <div>
        <h2>This is a test</h2>
    </div>
</template>

<script>
    export default {
        name: 'Article',
        props: {
            title: {
                type: String,
                required: true,
                default: "Default title of the blog",
            },
            likes: Number,
        },
        inheritAttrs: false,
    }
</script>

<style lang="scss" scoped>

</style>