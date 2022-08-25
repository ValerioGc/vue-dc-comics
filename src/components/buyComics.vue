<template>
    <div class="container-comics brand-style">
        <ul>
            <buyComicsLink v-for="(link, index) in comicsLink" 
            :linkName="link.name" 
            :linkThumb="link.imgName"
            :linkPath="link.link" :key="index" />
        </ul>
    </div>
</template>

<script>

import buyComicsLink from './buyComicsLink.vue';

    export default {
    name: "buyComics",
    components : {
        buyComicsLink,
    },
    data() {
        return {
            comicsLink: [
                {
                    name: "Digital Comics",
                    link: "#",
                    imgName: require("../assets/img/buy-comics-digital-comics.png"),
                },
                {
                    name: "DC Merchandise",
                    link: "#",
                    imgName: require("../assets/img/buy-comics-merchandise.png"),
                },
                {
                    name: "Subscription",
                    link: "#",
                    imgName: require("../assets/img/buy-comics-subscriptions.png"),
                },
                {
                    name: "Comic shop locator",
                    link: "#",
                    imgName: require("../assets/img/buy-comics-shop-locator.png"),
                },
                {
                    name: "DC Power visa",
                    link: "#",
                    imgName: require("../assets/img/buy-dc-power-visa.svg"),
                },
            ],
        };
    }
}

</script>

<style lang="scss">

    @import '../styles/vars.scss';
    @import '../styles/general.scss';
    @import '../styles/mixins.scss';

        .container-comics {
            width: 100%;
            padding: 70px 0;
            @include flex-center('vertical', 'no');
            @include justify('space_between');

            ul {
                @include flex-center('vertical', 'no');
                @include justify();
                width: 80%;
                margin: auto;

                li {
                    @include flex-center('center', 'no');

                    img {
                        width: 40px;
                        height: 40px;
                        margin-right: 10px;
                    }

                    h3 {
                        color: $light_color;
                        line-height: 40px;

                        &:hover {
                            transition: all 0.3s linear 0.1s;
                            color: $alt_light_color;
                            text-decoration: underline;
                        }
                    }
                }
            }
        }

</style>
