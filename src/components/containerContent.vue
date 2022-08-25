<template>
    <div class="comics-list-container">
        <!-- Titolo Sezione -->
        <h2 class="comics-section-title brand-style">Current Series</h2>
        <!-- Fumetti -->
        <ul class="comics-list">
            <singleComics v-for="(comics, index) in comicsList" :Series="comics.series" :Thumb="comics.thumb"
                :Price="comics.price" :key="index" />
        </ul>
        <!-- bottone carica altro -->
        <a class="button brand-style" href="#">Load More</a>
    </div>
</template>
.path
<script>
    import singleComics from './singleComics.vue';

    export default {
        name: 'containerContent',
        components: {
            singleComics,
        },
        data() {
            return {
                comicsList: [
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                        price: "$19.99",
                        series: "Action Comics",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                        price: "$3.99",
                        series: "American Vampire 1976",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                        price: "$16.99",
                        series: "Aquaman",
                        type: "graphic novel"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                        price: "$2.99",
                        series: "Batgirl",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        price: "$3.99",
                        series: "Batman",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        price: "$2.99",
                        series: "Batman Beyond",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                        price: "$3.99",
                        series: "Batman/Superman",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                        price: "$4.99",
                        series: "Batman/Superman Annual",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                        price: "$5.99",
                        series: "Batman: The Joker War Zone",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                        price: "$6.99",
                        series: "Batman: Three Jokers",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                        price: "$4.99",
                        series: "Batman: White Knight Presents: Harley Quinn",
                        type: "comic book"
                    },
                    {
                        thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                        price: "$16.99",
                        series: "Catwoman",
                        type: "graphic novel"
                    }
                ]
            }
        }
    }

</script>

<style lang="scss">

    @import '../styles/vars.scss';
    @import '../styles/general.scss';
    @import '../styles/mixins.scss';


        .comics-list-container {
            width: 80%;
            margin: auto;
            padding: 25px 0;
            text-align: center;

            .comics-section-title {
                padding: 15px 20px;
                position: relative;
                top: -55px;
                right: 42%;
            }

            .comics-list {
                @include flex-center('vertical', 'yes');
                @include justify('space_between');
            }

            .comics-card {
                width: calc(100% / 6 - 30px);
                height: calc(100vh / 4);
                margin: 40px 15px;

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
                                    filter: brightness(70%);
                                }
                                &:hover .comics-card a span {
                                    display: inline-block;
                                }
                            }

                            span {
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
            }

            .button {
                padding: 15px 50px;
                margin-top: 5rem;
                margin-bottom: 1rem;
                text-align: center;

                &:hover {
                    border-radius: 10px;
                    transition: all 0.2s linear 0.1s;
                    color: $brand_color;
                    background-color:$light_color ;
                }
            }
        }

</style>
