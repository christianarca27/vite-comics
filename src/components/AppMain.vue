<script>
import AppCard from './AppCard.vue';
import json from '../json/dc-comics.json'

export default {
    data() {
        return {
            comics: json,
        };
    },
    components: { AppCard },
}
</script>

<template>
    <main>
        <div id="jumbo"></div>

        <div id="card-container">
            <AppCard v-for="comic in comics" :img="comic.thumb" :title="comic.series"></AppCard>
        </div>

        <button>Load more</button>
    </main>
</template>

<style lang="scss" scoped>
main {
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    gap: 3rem;

    #jumbo {
        width: 100%;
        height: 400px;
        background-image: url("/img/jumbotron.jpg");
        background-size: cover;
    }

    #card-container {
        max-width: 1200px;
        width: 100%;

        display: flex;
        flex-flow: row wrap;
        gap: 30px;
    }

    button {
        background-color: #0282F9;
        margin-bottom: 1rem;
        padding: .5rem 3rem;

        color: white;
        // font-size: 1.2rem;
        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>