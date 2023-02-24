<template>
    <div>
        <h1>Pokemon:<span>{{ id }}</span></h1>
    </div>
</template>

<script>
export default {
    props: {
        id: {
            type: Number,
            required: true
        }
    },
    data() {
        return {
            
        }
    },
    created() {
        
    },
}
</script>