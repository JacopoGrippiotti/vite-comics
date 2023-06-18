<template>
    <div class="image-container">
        <img :src="filmElement.thumb" alt="">
    </div>
</template>

<script>
export default {
    name:'FilmItem',
    props: {
        filmElement : Object
    },
    
}
</script>
<style lang="scss" scoped>
    div.image-container{
        width: calc((100% / 6) - 50px);
        height: 100px;
        img{
            height: 100%;
        }
    }
</style>