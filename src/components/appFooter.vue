<template>
    <footer class="appFooter">
        <div>
            <ul>
                <li>
                    <h3>{{footLink.title}}</h3>
                </li>
                <li v-for="(links, index) in footLink" :key="index">
                    <a href="#">
                        {{links.name}}
                    </a>
                </li>
            </ul>
        </div>
        <div>
            <a href="#">SIGN-UP NOW!</a>
            <div>
                <h2>FOLLOW US</h2>
                <a href="#">
                    <i class="fa-brands fa-facebook-f"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-twitter"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-youtube"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-pinterest-p"></i>
                </a>
                <a href="#">
                    <i class="fa-solid fa-location-dot"></i>
                </a>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'appFooter',
}
</script>


<style  lang="scss">
</style>