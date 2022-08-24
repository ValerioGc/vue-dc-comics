<template>
    <header class="appHeader">
        <img src="@/assets/img/dc-logo.png" alt="Logo DC Comics">
        <ul>
            <li v-for="(items, index) in navItems" :key="index">
                <a href="#" :class="{'active' : items.isActive}" class="nav">{{items.name}}</a>
            </li>
        </ul>
    </header>
</template>

<script>
    export default {
        name: 'appHeader',
        data() {
            return {
                navItems: [
                    {
                        name: 'Characters',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Comics',
                        path: '#',
                        isActive: true,
                    },
                    {
                        name: 'Movies',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'TV',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Games',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Collectables',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Videos',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Fans',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'News',
                        path: '#',
                        isActive: false,
                    },
                    {
                        name: 'Shop',
                        path: '#',
                        isActive: false,
                    }
                ]
            }
        }
    }
</script>


<style lang="scss">



@import '../styles/vars.scss';
@import '../styles/general.scss';

@import '../styles/mixins/flex-center.scss';
    
        header {
            @include flex-center('vertical');
            width: 80%;
            margin: auto;
            background-color: $light_color;
    
            a {
                color: $alt_dark_color;
            }
    
            ul {
                @include flex-center('vertical');
                @include justify('space_between');
                width: 80%;
            }
    
            .active {
                border-bottom: 2px solid $brand_color;
                color: $brand_color;
            }
            .logo {
                width: 50%;
            }
        }

</style>