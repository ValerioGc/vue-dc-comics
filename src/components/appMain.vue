<template>
    <main class="appMain">
        <div class="container-content">
            <div class="content">
                <appJumbo />
                <containerContent />
                <buyComics />
            </div>
        </div>
    </main>
</template>

<script>

    import appJumbo from '@/components/appJumbo.vue';
    import containerContent from '@/components/containerContent.vue';
    import buyComics from '@/components/buyComics.vue';

    export default {
        name: 'appMain',
        components: {
            appJumbo,
            buyComics,
            containerContent,
        }
    }
    
</script>

<style lang="scss">

    @import '../styles/vars.scss';
    @import '../styles/general.scss';
    @import '../styles/mixins.scss';

        .container-content {
            background-color: $dark_color;

            .content {
                color: $light_color;
            }
        }
</style>
