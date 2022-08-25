<template>
    <li class="comics-card">
        <a href="#">
            <img :src="Thumb" :alt="`Copertina ${Series}`" />
            <span class="price">{{Price}}</span>
        </a>
        <h3>{{Series}}</h3>
    </li>
</template>

<script>

    export default {
        name: 'singleComics',
        props: {
            Series: String,
            Thumb: String,
            Price: String,
        }
    }

</script>

<style lang="scss" scoped>
    
    @import '../styles/vars.scss';
    @import '../styles/general.scss';

    .comics-card {
        width: calc(100% / 6 - 20px);
        height: calc(100vh / 4);
        margin: 40px 0px;

        a {
            position: relative;
            display: inline-block;
            height: 100%;
            width: 100%;

            img {
                object-fit: cover;
                object-position: top;
                width: 100%;
                height: 100%;

                &:hover {
                    filter: brightness(50%);
                    transition: all 0.2s linear 0.1s;
                    border-radius: 10px;
                }

                &:hover .price {
                    display: inline-block;
                }
            }

            .price {
                display: none;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translateX(-50%);
                font-weight: bold;
                font-size: 20px;
                color: $light_color;
                text-shadow: 2px 2px 3px $dark_color;
            }
        }

        h3 {
            font-size: 1.1rem;
            padding: 10px 0;
        }
    }

</style>
