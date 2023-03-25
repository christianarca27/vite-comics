<script>
export default {
    data() {
        return {
            links: [
                "characters",
                "comics",
                "movies",
                "tv",
                "games",
                "collectibles",
                "videos",
                "fans",
                "news",
                "shop"
            ],
            activeIndex: 0,
        }
    },
    methods: {
        changeActiveLink(linkIndex) {
            this.activeIndex = linkIndex;
        }
    },
}
</script>

<template>
    <header>
        <div class="container">
            <div id="logo">
                <img src="/img/dc-logo.png" alt="Logo DC Comics">
            </div>

            <div id="links">
                <ul>
                    <li v-for="(link, index) in links" @click="changeActiveLink(index)"
                        :class="activeIndex == index ? 'active' : ''">{{ link }}</li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    background-color: #fff;
    color: black;

    .container {
        height: 100px;

        display: flex;
        flex-flow: row nowrap;
        justify-content: space-between;
        align-items: center;

        #logo {
            img {
                height: 80px;
            }
        }

        #links {
            height: 100%;

            ul {
                height: 100%;

                display: flex;
                gap: 1em;

                text-transform: uppercase;
                font-weight: 500;

                li {
                    height: 100%;

                    display: flex;
                    align-items: center;

                    cursor: pointer;
                }

                li.active {
                    border-top: transparent solid 5px;
                    border-bottom: #0282F9 solid 5px;
                    color: #0282F9;
                }
            }
        }
    }
}
</style>