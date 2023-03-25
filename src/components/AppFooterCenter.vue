<script>
export default {
    data() {
        return {
            lists: [
                {
                    title: "dc comics",
                    links: [
                        "Characters",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News"
                    ]
                },
                {
                    title: "shop",
                    links: [
                        "Shop DC",
                        "Shop DC Collectibles"
                    ]
                },
                {
                    title: "DC",
                    links: [
                        "Terms Of Use",
                        "Privacy policy (New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Certificates",
                        "Ratings",
                        "Shop Help",
                        "Contact Us"
                    ]
                },
                {
                    title: "sites",
                    links: [
                        "DC",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa"
                    ]
                },
            ]
        }
    },
}
</script>

<template>
    <div id="container-wrapper">

        <div class="container">
            <div id="lists-container">
                <div v-for="list in lists" class="list-container">
                    <h2>{{ list.title }}</h2>
                    <ul>
                        <li v-for="link in list.links">
                            <a href="">{{ link }}</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div id="footer-big-logo">
                <img src="/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#container-wrapper {
    background-image: url("/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;

    .container {
        height: 400px;

        display: flex;
        justify-content: space-between;

        #lists-container {
            width: 400px;
            height: 100%;
            padding: 50px 0;

            display: flex;
            flex-flow: column wrap;
            gap: 1rem;

            .list-container {
                h2 {
                    margin-bottom: .5rem;

                    font-size: 1.3rem;
                    text-transform: uppercase;
                }

                ul {
                    li {
                        a {
                            color: white;
                            font-size: .8rem;
                            opacity: .6;
                        }
                    }
                }
            }
        }

        #footer-big-logo {
            height: 100%;

            display: flex;
            align-items: center;

            overflow-y: hidden;
        }
    }
}
</style>