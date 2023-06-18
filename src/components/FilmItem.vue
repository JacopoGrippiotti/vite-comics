<template>
    <div class="image-container">
        <img :src="filmElement.thumb" alt="">
        <h3>{{ filmElement.series }}</h3>
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
        width: calc((100% / 6) - 10px);
        height: 210px;
        margin-top: 20px;
        text-align: start;
        padding: 5px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        h3{
            color: white;
            font-size: 0.70rem;
            text-transform: uppercase;
        }
        img{
            height: calc(100% - 30px) ;
            width: 100%;
            object-fit: cover;

        }
    }
</style>