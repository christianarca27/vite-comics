<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <div id="container-wrapper">
        <div class="container">
            <div id="container-inner-left">
                <button>SIGN-UP NOW!</button>
            </div>

            <div id="container-inner-right">
                <strong>FOLLOW US</strong>

                <a href="">
                    <img src="/img/footer-facebook.png" alt="">
                </a>
                <a href="">
                    <img src="/img/footer-periscope.png" alt="">
                </a>
                <a href="">
                    <img src="/img/footer-pinterest.png" alt="">
                </a>
                <a href="">
                    <img src="/img/footer-twitter.png" alt="">
                </a>
                <a href="">
                    <img src="/img/footer-youtube.png" alt="">
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#container-wrapper {
    background-color: #303030;

    .container {
        height: 110px;

        display: flex;
        justify-content: space-between;
        align-items: center;

        #container-inner-left {
            button {
                background-color: #303030;
                padding: .7rem;
                border: #0282F9 solid 2px;

                color: white;
                cursor: pointer;
            }

            button:hover {
                background-color: #505050;
            }
        }

        #container-inner-right {
            display: flex;
            align-items: center;
            gap: 1rem;

            strong {
                color: #0282F9;
            }
        }
    }
}
</style>