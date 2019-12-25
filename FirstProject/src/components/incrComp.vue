<template>
    <div>
        <h2>number {{count}}</h2>
        <button @click="count++">Increment</button>
        <button @click="count--">Decrement</button>
    </div>
</template>

<script>
export default {
    name: "incrComp",
    data: function() {
        return {
            count: 0,
            age: 26,
        }
    }
}
</script>

<style scoped>

</style>