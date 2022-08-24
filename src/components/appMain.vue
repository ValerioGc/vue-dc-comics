<template>
    <main class="appMain">
        <div class="container-content">
            <h1>--> Content goes here &lt;--</h1>
        </div>
        <div class="container-comics">
            <ul>
                <li v-for="(link, index) in comicsLink" :key="index">
                    <!-- <img :src="require('@/assets/img/' + link.imgName + '.png')" :alt=" `Link ${link.name}`"> -->
                    <img :src="'./assets/img/' + link.imgName + '.png'" :alt=" `Link ${link.name}`">
                    <h2>{{link.name}}</h2>
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'appMain',
        data() {
            return {
                comicsLink: [
                    {
                        name: 'Digital Comics',
                        path: '#',
                        imgName: 'buy-comics-digital-comics',
                    },
                    {
                        name: 'DC Merchandise',
                        path: '#',
                        imgName: 'buy-comics-merchandise'
                    },
                    {
                        name: 'Subscription',
                        path: '#',
                        imgName: 'buy-comics-subscription'
                    },
                    {
                        name: 'Comic shop locator',
                        path: '#',
                        imgName: 'buy-comics-shop-locator'
                    },
                    {
                        name: 'DC Power visa',
                        path: '#',
                        imgName: 'buy-dc-power-visa'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">



    @import '../styles/vars.scss';
    @import '../styles/general.scss';

    @import '../styles/mixins/flex-center.scss';

    main {
        background-color:  $brand_color;
    
        .container-content {
            background-color: $dark_color;
        }
        .container-comics {
            @include flex-center('vertical');
            width: 80%;
        }
    }

</style>
