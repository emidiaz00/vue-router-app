<template>
    <div>
        <router-link to="/">Pokemon List</router-link>
        <router-link to="/id">PokemonId</router-link>
        <router-link to="/about">About</router-link>
    </div>
</template>

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