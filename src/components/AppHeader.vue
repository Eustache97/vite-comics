<script>
export default {
    name: "AppHeader",
    data() {
        return {
            menu: [
                {
                    title: "Characters",
                    href: "/Characters",
                    active: false
                },
                {
                    title: "Comics",
                    href: "/Comics",
                    active: true
                },
                {
                    title: "Movies",
                    href: "/Movies",
                    active: false
                },
                {
                    title: "Tv",
                    href: "/Tv",
                    active: false
                },
                {
                    title: "Games",
                    href: "/Games",
                    active: false
                },
                {
                    title: "Collectibles",
                    href: "/Collectibles",
                    active: false
                },
                {
                    title: "Videos",
                    href: "/Videos",
                    active: false
                },
                {
                    title: "Fans",
                    href: "/Fans",
                    active: false
                },
                {
                    title: "News",
                    href: "/News",
                    active: false
                },
                {
                    title: "Shop",
                    href: "/Shop",
                    active: false
                }
            ]
        }
    }
}
</script>

<template>
 <header>
    <div class="container">
        <div class="header-div">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo-dc_comics">
            </div>
            <div class="nav">
                <ul>
                    <li
                    v-for="(link, index) in menu" :key="index">
                        <a :href="link.href"
                        :class="{'active' : link.active}"> {{link.title}} </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
 </header>  
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;
header{
    background-color: white;
    .container{
        .header-div{
            height: 100px;
            width: 100%;
            display:flex;
            justify-content: space-between;
            align-items: center;
            
            padding:  1em 0;
        }
        
    }
    
    .logo{
        height: 100%;
        img{
            max-height: 100%;
        }
    }
    .nav{
        ul{
            display: flex;
            gap: 1em; 
            text-transform: uppercase;
            font-size: .8rem;
            font-weight: 600;
            li{
                a{
                    display: inline-block;
                    line-height: 100px;
                    &:hover{
                        color: $primary-color;
                        
                    }
                    &.active{
                        color: $primary-color;
                        border-bottom: 3px solid $primary-color;
                        margin-bottom: .2rem;
                    }
                }
            }
        }
    }
}

</style>