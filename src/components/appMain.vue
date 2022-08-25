<template>
    <main class="appMain">
        <div class="container-content">
            <div class="content">

                <div class="jumbo">
                    <!-- <img src="@/assets/img/jumbotron.jpg" alt="immagine jumbotron"> -->
                </div>



            </div>
        </div>
        <div class="container-comics">
            <ul>
                <li v-for="(link, index) in comicsLink" :key="index">
                    <img :src="link.imgName" :alt=" `Link ${link.name}`" />
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
            height: 350px;
            background-image: url('@/assets/img/jumbotron.jpg');
            background-position: top;
            background-size: cover;
            background-repeat: no-repeat;

            .content {
                color: $light_color;
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
                width: 15%;
                display: inline-block;
                vertical-align: middle;
                line-height: 100%;
            }
            h3 {
                color: $light_color;
                padding: 7px 0;
                display: inline-block;
            }
            img {
                padding: 4rem 0 ;
            }
        }
        .jumbo {
            height: 30vh;

            img {
                width: 100%;
                height: 100%;
            }
        }
    }

</style>
