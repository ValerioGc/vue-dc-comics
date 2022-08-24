<template>
    <main class="appMain">
        <div class="container-content">
            <div class="content">
                <h1>--> Content goes here &lt;--</h1>
            </div>
        </div>
        <div class="container-comics">
            <ul>
                <li v-for="(link, index) in comicsLink" :key="index">
                    <!-- <img :src="require('@/assets/img/' + link.imgName + '.png')" :alt=" `Link ${link.name}`"> -->
                    <img :src="'./assets/img/' + link.imgName + '.png'" :alt=" `Link ${link.name}`">
                    <h3>{{link.name}}</h3>
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
    @import '../styles/mixins.scss';

    main {
    
        .container-content {
            background-color: $dark_color;
            padding: 70px 0;
            
            .content {
                color: $light_color;
                width: 80%;
                margin: auto;
            }
        }
        .container-comics {
            @include flex-center('vertical');
            @include justify('space_between');
            
            background-color: $brand_color;
            
            ul {
                @include flex-center('space_between');
                @include justify('space_between');
                width: 80%;
                margin: auto;
            }
            img {
                width: 10%;
                display: inline-block;
                vertical-align: middle;
                line-height: 100%;
            }
            h3 {
                color: $light_color;
                padding: 7px 0;
                display: inline-block;
            }
        }
    }

</style>
