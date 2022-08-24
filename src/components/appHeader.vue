<template>
    <div class="appHeader">
        <img src="@/assets/img/dc-logo.png" alt="Logo DC Comics">
        <ul>
            <li v-for="(items, index) in navItems" :key="index">
                <a href="#" :class="{'active' : isActive}">{{items.name}}</a>
            </li>
        </ul>
    </div>
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


<style  lang="scss">

</style>