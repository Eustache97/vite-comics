<script>
export default {
    name: "MainThumb",
    props: {
        title: String,
        imgSrc: String
    }
}
</script>

<template>
<div class="thumb">
    <div class="image">
        <img :src="imgSrc" alt="title">
    </div>
    
    <h4> {{title}} </h4>
</div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;
.thumb{
    width: calc(100% / 6 - 2rem);
    margin: 1rem;
    .image{
        width: 100%;
        height: 120px;
        overflow: hidden;
    }
    
    
    h4{
        color: white;
        font-size: .6rem;
        margin-top: .3rem;
        text-transform: uppercase;
    }
}
</style>