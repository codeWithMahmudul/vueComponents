<template>
    <div>
        <button @click="incrementCount">Clicked {{ counter }} times</button>
    </div>
</template>

<script>
    export default {
        name: 'ClickCounter',
        data() {
            return {
                counter: 0
            }
        },
        methods: {
            incrementCount() {
                this.count += 1
            }
        }
    }
</script>

<style scoped>

</style>