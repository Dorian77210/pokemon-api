<template>
    <div class="header text-warning bg-dark d-flex">
        <b-dropdown id="dropdown-left" text="Navigation" variant="primary" class="m-2">
            <b-dropdown-item> 
                <router-link to="/">API Pokemon</router-link>
            </b-dropdown-item>
            <b-dropdown-item> 
                <router-link :to="{name: 'pokemon-compare' }">Compare Pokemons</router-link>
            </b-dropdown-item>
            <b-dropdown-item>
                <router-link :to="{name: 'berries-view' }">Berries</router-link>
            </b-dropdown-item>
            <b-dropdown-item>
                <router-link :to="{name: 'objects-view'}">Objects List</router-link>
            </b-dropdown-item>
        </b-dropdown>
        <div class="text-center title align-self-center">
            <h6>{{ $props.title }}</h6>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'AppHeader',
        props: {
            title: String
        }
    }

</script>

<style>

    .header {
        padding: 1% 0%;
    }

    .title {
        margin-right: auto;
        margin-left: auto;
    }

</style>