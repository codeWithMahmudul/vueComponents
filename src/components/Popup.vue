<template>
    <div>
        <h2>This is a popup</h2>
        <input type="text" v-model="names.name">
        <button @click="$emit('close', names.name)">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        data() {
            return {
                names: {
                    name: "",
                    age: 23,
                }
            }
        },
        emits: {
            close: (name) => {
                if(!name){
                    return false;
                }else{
                    return true;
                }
            }
        },
    }
</script>

<style scoped>

</style>