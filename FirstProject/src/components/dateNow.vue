<template>
    <div>
        <p>{{date}}</p>
        <button @click="newDate()">New Date</button>
        <p>my age is: {{age}} => this age make with props</p>
        <input type="checkbox" id="checkbox" v-model="checked">
        <label for="checkbox">{{ checked }}</label><br>
        <div class="check-names">
            <input type="checkbox" id="ahmed" value="Ahmed" v-model="checkedNames">
            <label for="ahmed">Ahmed</label>
            <input type="checkbox" id="nserallah" value="Nserallah" v-model="checkedNames">
            <label for="nserallah">Nserallah</label>
            <input type="checkbox" id="shadi" value="Shadi" v-model="checkedNames">
            <label for="shadi">Shadi</label>
            <p>names: {{checkedNames}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "dateNow",
    props:['age'],
    data: function () {
        return {
            date: new Date(),
            checked: true,
            checkedNames: [],
        }
    },
    methods: {
        newDate: function () {
            return this.date = Date();
        }
    }
}
</script>

<style scoped>

</style>

