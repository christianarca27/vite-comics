<script>
export default {
    data() {
        return {

        }
    },
    props: {
        img: String,
        title: String,
    }
}
</script>

<template>
    <div id="card">
        <img :src="img" alt="comic thumb">
        <p>{{ title }}</p>
    </div>
</template>

<style lang="scss">
#card {
    width: calc(100% / 6 - 30px * 5 / 6);

    &:hover {
        cursor: pointer;
    }

    img {
        width: 100%;
        aspect-ratio: 1;
        margin-bottom: 1rem;

        object-fit: cover;
        object-position: top;
    }

    p {
        text-transform: uppercase;
        text-align: start;
    }
}
</style>