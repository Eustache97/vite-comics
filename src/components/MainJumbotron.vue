<script>
export default {
    name: "MainJumbotron"
}
</script>

<template>
<section>
    <div class="jumbotron">
        <div class="container">
            <div class="current-series">
                <h3>current series</h3>
            </div>
        </div>
        
    </div>
</section>   
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;
.jumbotron{
    width: 100%;
    height: 250px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-position: top;
    .container{
        height: 100%;
        position: relative;
        .current-series{
            text-transform: uppercase;
            position: absolute;
            bottom: -15px;
            left: 0;
            padding: .3em 2em;
            color: white;
            background-color: $primary-color;
        }
    } 
    
}
</style>