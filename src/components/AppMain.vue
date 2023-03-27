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

        <div class="container">
            <h2 id="content-description">Current Series</h2>

            <div id="card-container">
                <AppCard v-for="comic in comics" :img="comic.thumb" :title="comic.series"></AppCard>
            </div>
        </div>

        <button>Load more</button>
    </main>
</template>

<style lang="scss" scoped>
@import "../style.scss";

main {
    text-align: center;

    #jumbo {
        width: 100%;
        height: 400px;
        background-image: url("/img/jumbotron.jpg");
        background-size: cover;
    }

    .container {
        position: relative;

        #content-description {
            background-color: $primary;
            padding: .5rem 1.5rem;

            position: absolute;
            top: 0;
            left: -1rem;
            transform: translateY(-50%);

            text-transform: uppercase;
            font-weight: bold;
            font-size: 1.8rem;
        }

        #card-container {
            padding-top: 50px;
            padding-bottom: 50px;

            display: flex;
            flex-flow: row wrap;
            gap: 30px;
        }
    }

    button {
        @include create-button($primary, white);

        margin-bottom: 1rem;
        padding: .5rem 3rem;

        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>