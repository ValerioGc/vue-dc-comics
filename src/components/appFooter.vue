<template>
    <footer class="appFooter">
        <div class="footer-top">
            <div v-for="(titles, index) in footLink" :key="index">
                <h3>
                    {{titles.title}}
                </h3>
                <a href="#" v-for="(titles, index) in titles.linkName" :key="index">
                    {{titles.nameL}}
                </a>
            </div>
            <img src="@/assets/img/dc-logo-bg.png" alt="Logo DC Comics">
        </div>
        <div class="footer-low">
            <a href="#" class="button">SIGN-UP NOW!</a>
            <div>
                <h2>FOLLOW US</h2>
                <a href="#">
                    <!-- <font-awesome-icon icon="fa-brands fa-facebook-f" /> -->
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
    data() {
        return {
            footLink: [
                {   
                title:'DC Comics',
                linkName: 
                    [
                        {
                            nameL:'Characters',
                            path:'#',
                        },
                        {
                            nameL:'Comics',
                            path:'#',
                        },
                        {
                            nameL:'Movies',
                            path:'#',
                        },
                        {
                            nameL:'TV',
                            path:'#',
                        },
                        {
                            nameL:'Games',
                            path:'#',
                        },
                        {
                            nameL:'Videos',
                            path:'#',
                        },
                        {
                            nameL:'News',
                            path:'#',
                        }
                    ]
                },
                {
                    title: 'SHOP',
                    linkName:
                        [
                            {
                                nameL: 'Characters',
                                path: '#',
                            },
                            {
                                nameL: 'Comics',
                                path: '#',
                            }
                        ]
                },
                {
                    title: 'DC',
                    linkName:
                        [
                            {
                                nameL: 'Terms Of Use',
                                path: '#',
                            },
                            {
                                nameL: 'Privacy policy (New)',
                                path: '#',
                            },
                            {
                                nameL: 'Ad Choices',
                                path: '#',
                            },
                            {
                                nameL: 'Advertising',
                                path: '#',
                            },
                            {
                                nameL: 'Jobs',
                                path: '#',
                            },
                            {
                                nameL: 'Subscritions',
                                path: '#',
                            },
                            {
                                nameL: 'Talent Workshops',
                                path: '#',
                            },
                            {
                                nameL: 'CPSC Certificates',
                                path: '#',
                            },
                            {
                                nameL: 'Ratings',
                                path: '#',
                            },
                            {
                                nameL: 'Show Help',
                                path: '#',
                            },
                            {
                                nameL: 'Contact Us',
                                path: '#',
                            }
                        ]
                },
                {
                    title: 'SITES',
                    linkName:
                        [
                            {
                                nameL: 'DC',
                                path: '#',
                            },
                            {
                                nameL: 'MAD Magazine',
                                path: '#',
                            },
                            {
                                nameL: 'DC Kids',
                                path: '#',
                            },
                            {
                                nameL: 'DC Universe',
                                path: '#',
                            },
                            {
                                nameL: 'DC Power Visa',
                                path: '#',
                            }
                        ]
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

    footer {
        background-color: $alt_dark_color;

        .footer-top {
            @include flex-center('vertical');
            @include justify('space_around');
            background-image: url('@/assets/img/footer-bg.jpg');
            background-repeat: no-repeat;
            background-size: cover;

            .sec-title {
                color: $light_color;
                text-transform: uppercase;
            }

            a {
                color: $alt_light_color;
                display: block;
                padding: 2px 0;
            }

            h3 {
                color: $light_color;
                padding: 10px 0;
            }

            img {
                width: 15%
            }
        }

        .footer-low {
            @include flex-center('vertical');
            @include justify('space_between');
            padding: 30px 0;
            margin:auto;
            width: 80%;

            a.button {
                padding: 10px 15px;
                border: 3px solid $brand_color;
                color: $light_color;
                text-transform: uppercase;

                &:hover {
                    color: $brand_color;
                    border-color: $light_color;
                    transition: all 0.5s linear 0.1s;
                }
            }

            h2 {
                text-transform: uppercase;
                color: $brand_color;
            }

            i {
                border-radius: 50%;
                background-color: $alt_light_color;
            }
        }
    }
    
</style>