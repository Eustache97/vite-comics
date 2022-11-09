<script>
export default {
    name: "AppFooter",
    data() {
        return {
            links: [
                {
                    title: "dc comics",
                    contentLink: [
                        {
                            name: "Characters",
                            href: "/Characters"
                        },
                        {
                            name: "Comics",
                            href: "/Comics" 
                        },
                        {
                            name: "Movies",
                            href: "/Movies"
                        },
                        {
                            name: "Tv",
                            href: "/Tv"
                        },
                        {
                            name: "Games",
                            href:"/Games"
                        },
                        {
                            name: "Videos",
                            href: "/Videos"
                        },
                        {
                            name: "News",
                            href: "/News"
                        } 
                    ]
                },
                {
                    title: "dc",
                    contentLink: [
                        {
                            name: "Terms Of Use",
                            href: "/Terms-Of-Use"
                        },
                        {
                            name: "Privacy Policy (New)",
                            href: "/Privacy-Policy" 
                        },
                        {
                            name: "Ad Choices",
                            href: "/Ad-Choices"
                        },
                        {
                            name: "Advertising",
                            href: "/Advertising"
                        },
                        {
                            name: "Jobs",
                            href:"/Jobs"
                        },
                        {
                            name: "Subscriptions",
                            href: "/Subscriptions"
                        },
                        {
                            name: "Talent Workshops",
                            href: "/Talent-Workshops"
                        },
                        {
                            name: "CPSC Certificates",
                            href: "/CPSC-Certificates"
                        },
                        {
                            name: "Ratings",
                            href: "/Ratings"
                        },
                        {
                            name: "Shop Help",
                            href: "/Shop-Help"
                        },
                        {
                            name: "Contact Us",
                            href: "/Contact-Us"
                        }

                    ]
                },
                {
                    title: "sites",
                    contentLink: [
                        {
                            name: "DC",
                            href: "/DC"
                        },
                        {
                            name: "MAD Magazine",
                            href: "/MAD-Magazine" 
                        },
                        {
                            name: "DC Kids",
                            href: "/DC-Kids"
                        },
                        {
                            name: "DC Universe",
                            href: "/DC-Universe"
                        },
                        {
                            name: "DC Power Visa",
                            href:"/DC-Power-Visa"
                        }

                    ]
                },
                {
                    title: "shop",
                    contentLink: [
                        {
                            name: "Shop DC",
                            href: "/Shop-DC"
                        },
                        {
                            name: "Shop DC Collectibles",
                            href: "/Shop-DC-Collectibles" 
                        }
                        
                    ]
                }
            ]
        }
    }
}
</script>

<template>
 <footer>
    <div class="container">
        <div class="footer-top">
            <div class="footer-links row">
                <div class="links-list col-3"
                v-for="(link, index) in links" :key="index">
                    <h2> {{link.title}} </h2>
                    <ul>
                        <li
                        v-for="(content,position) in links[index].contentLink" :key="position">
                            <a :href="content.href"> {{content.name}} </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer-logo">
            </div>
        </div>
        <div class="footer-bottom"></div>
    </div> 
 </footer>   
</template>

<style lang="scss" scoped>
footer{
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-position: center;
    .footer-top{
        width: 100%;
        height: 300px;
        display: flex;
        justify-content: space-between;
        font-size: .7rem;
        .footer-links{
            width: 50%;
            padding: 1em 0;
            .links-list{
                &.col-3{
                    width: calc(100% / 3);
                }
                h2{
                    text-transform: uppercase;
                    color: white;
                    margin-bottom: .5em;
                }
                ul{
                    
                    li{
                        a{
                            color: grey;
                        }
                    }
                }
            }
            
        }
        .footer-logo{
            height: 100%;
            width: 50%;
            background-image: url("../assets/img/dc-logo-bg.png");
            background-size: cover;
            background-position: center;
        }
        
    }
}
</style>