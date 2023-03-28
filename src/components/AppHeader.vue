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
            activeIndex: 1,
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
                    <li v-for="(link, index) in links" :class="activeIndex == index ? 'active' : ''">
                        <a href="#" @click="changeActiveLink(index)">{{ link }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../style.scss" as *;

header {
    background-color: white;
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

                    a {
                        color: black;
                    }

                    &.active {
                        border-top: transparent solid 5px;
                        border-bottom: $primary solid 5px;
                        color: $primary;
                    }
                }
            }
        }
    }
}
</style>