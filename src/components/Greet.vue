<template>
    <h2>Hello this message is from component. And the message is coming from {{ name }}</h2>
</template>

<script>
export default {
    name: 'Greet',
    props: ['name'],
}
</script>