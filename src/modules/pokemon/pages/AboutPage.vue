<template>
    <div>
        <h1>About page</h1>
        <hr>
        <h2>Emiliano {{ lastname }}</h2>
        <button @click="addLastName">Add lastname</button>
        <br>
        <br>
        <button @click="resetLastName">Clear</button>
    </div>
</template>

<script>

export default {
    data() {
        return {
            lastname: ''
        }
    },
    methods: {
        addLastName() {
            this.lastname = 'Diaz'
        },
        resetLastName() {
            this.lastname = ''
        }
    },
    beforeCreate() {
        console.log('beforeCreate');
    },
    created() {
        console.log('created');
    },
    beforeMount() {
        console.log('beforeMount');
    },
    mounted() {
        console.log('mounted');
    },
    beforeUpdate() {
        console.log('beforeUpdate');
    },
    updated() {
        console.log('updated');
    },
    activated() {
        console.log('activated');
    },
    deactivated() {
        console.log('deactivated');
    },
    beforeMount() {
        console.log('beforeMount');
    },
    unmounted() {
        console.log('unmounted');
    },
    errorCaptured: (err, vm, info) => {
        console.log('errorCaptured');
    },
    renderTracked() {
        console.log('renderTracked');
    },
    renderTriggered() {
        console.log('renderTriggered');
    }
}
</script>

<style scoped>
button {
    border:none;
    border-radius: 4px;
    background-color: rgb(65, 99, 100);
    padding: 12px;
    color: #ffffff;
    font-weight: bold;
    cursor: pointer;
}
button:hover {
    background-color: rgb(66, 127, 129);
}
</style>
