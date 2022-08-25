<template>
    <div class="container-comics brand-style">
        <ul>
            <li v-for="(link, index) in comicsLink" :key="index">
                <img :src="link.imgName" :alt="`Link ${link.name}`" />
                <a href="#">
                    <h3>{{ link.name }}</h3>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>

    export default {
        name: 'buyComics',
        data() {
            return {
                comicsLink: [
                    {
                        name: 'Digital Comics',
                        path: '#',
                        imgName: require('../assets/img/buy-comics-digital-comics.png'),
                    },
                    {
                        name: 'DC Merchandise',
                        path: '#',
                        imgName: require('../assets/img/buy-comics-merchandise.png'),
                    },
                    {
                        name: 'Subscription',
                        path: '#',
                        imgName: require('../assets/img/buy-comics-subscriptions.png'),
                    },
                    {
                        name: 'Comic shop locator',
                        path: '#',
                        imgName: require('../assets/img/buy-comics-shop-locator.png'),
                    },
                    {
                        name: 'DC Power visa',
                        path: '#',
                        imgName: require('../assets/img/buy-dc-power-visa.svg'),
                    },
                ],
            }
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
