<template>
    <li>
        <img :src="linkThumb" :alt="`Link ${linkName}`" />
        <a href="#">
            <h3>{{linkName}}</h3>
        </a>
    </li>
</template>

<script>

    export default {
        name: 'buyComicsLink',
        props: {
            linkName: String,
            linkThumb: String,
            linkPath: String,
        }
    }

</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';
    @import '../styles/general.scss';
    @import '../styles/mixins.scss';

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

</style>
