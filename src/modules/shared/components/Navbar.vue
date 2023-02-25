<template>
    <div>
        <!--<router-link :to="{ name: 'home'}">Pokemon List</router-link>
        <router-link :to="{ name: 'pokemon-id', params: { id:  85}}">PokemonId</router-link>
        <router-link :to="{ name: 'about'}">About</router-link> -->
        <CustomLink
            v-for="link in links" 
            :key="link.to"
            :link="link"
        />
        
    </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {
    data() {
        return {
            links: [
                { to: '/', name: 'Pokemons'},
                { to: '/pokemon-id/50', name: 'Por id'},
                { to: '/about', name: 'About'},
                { to: 'https://google.com', name: 'Pokemons'}
            ]
        }
    },

    components: {
        CustomLink: defineAsyncComponent(() => import('./CustomLink.vue'))
    }

}

</script>

<style scoped>

div a {
    padding: 20px;
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;
}

.router-link-exact-active {
  color: #42b983;
}

    
</style>