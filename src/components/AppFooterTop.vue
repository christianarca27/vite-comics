<script>
export default {
    data() {
        return {
            links: [
                {
                    image: "/img/buy-comics-digital-comics.png",
                    text: "digital comics"
                },
                {
                    image: "/img/buy-comics-merchandise.png",
                    text: "dc merchandise"
                },
                {
                    image: "/img/buy-comics-shop-locator.png",
                    text: "subscription"
                },
                {
                    image: "/img/buy-comics-subscriptions.png",
                    text: "comic shop locator"
                },
                {
                    image: "/img/buy-dc-power-visa.svg",
                    text: "dc power visa"
                },
            ],
        }
    },
}
</script>

<template>
    <div id="container-wrapper">
        <div class="container">
            <ul>
                <li v-for="link in links">
                    <img :src="link.image" alt="">
                    <a href="">{{ link.text }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style.scss" as *;

#container-wrapper {
    background-color: #0282F9;
    height: 150px;

    .container {
        height: 100%;

        ul {
            height: 100%;

            display: flex;
            justify-content: space-around;
            align-items: center;

            li {
                display: flex;
                align-items: center;
                gap: 1rem;
                text-transform: uppercase;

                img {
                    height: 60px;
                }

                a {
                    color: white;
                }
            }
        }
    }
}
</style>