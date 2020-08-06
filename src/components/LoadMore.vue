<template>
    <button class="btn primary" v-on:click="loadMore">Cargar Más</button>

</template>

<script>
import Items from './Items';
export default {
    name: "LoadMore",
    components: Items,
    methods: {
        loadMore() {
            
        }
    }

}
</script>

<style scoped>

</style>