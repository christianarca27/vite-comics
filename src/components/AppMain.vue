<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <main>
        <div id="jumbo"></div>

        <div id="card-container"></div>

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
        height: 600px;
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