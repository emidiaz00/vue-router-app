<template>
    <div>
        <div v-if="pokemon">
            <img :src="pokemon.sprites.front_default" :alt="pokemon.name" srcset="">
        </div>
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
            pokemon: null 
        }
    },
    created() {
        this.getPokemon()
    },
    methods: {
        async getPokemon() {
            try {
                const baseUrl = 'https://pokeapi.co/api/v2/pokemon/'
                const pokemon = await fetch(`${baseUrl}${this.id}`).then(r => r.json());
                this.pokemon = pokemon
            } catch (error) {
                this.$router.push('/')
                console.log('No hay ningún pokemon con este id');
            }
        }
    },
    watch: {
        id() {
            this.getPokemon()
        }
    },
}
</script>
<style scoped>

</style>