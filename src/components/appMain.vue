<template>
    <div class="appMain">
        <div>
            <h1>--> Content goes here &lt;--</h1>
        </div>
        <div>
            <ul>
                <li v-for="(link, index) in comicsLink" :key="index">
                    <img :src="`../assets/img/${link.imgPath}`" :alt="`Link ${link.name}`">
                    <h2>{{link.name}}</h2>
                </li>
            </ul>
        </div>
    </div>
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
                        imgPath: 'buy-comics-digital-comics.png'
                    },
                    {
                        name: 'DC Merchandise',
                        path: '#',
                        imgPath: '@/assets/img/buy-comics-merchandise.png'
                    },
                    {
                        name: 'Subscription',
                        path: '#',
                        imgPath: '@/assets/img/buy-comics-subscription.png'
                    },
                    {
                        name: 'Comic shop locator',
                        path: '#',
                        imgPath: '@/assets/img/buy-comics-shop-locator.png'
                    },
                    {
                        name: 'DC Power visa',
                        path: '#',
                        imgPath: '@/assets/img/buy-dc-power-visa.png'
                    }
                ]
            }
        }
    }
</script>


<style  lang="scss">
</style>