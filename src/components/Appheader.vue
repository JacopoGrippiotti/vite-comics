<template>
    <div class="container">
        <div class="logo-img" >
            <img :src='logoImage.src' alt="">
        </div>
        <ul class="nav-bar">
            <li v-for="item in navItems">
                <a href="#">
                    {{item}}
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            logoImage:{
                src:"../../src/assets/img/dc-logo.png"
            },
            navItems:[
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop'
        ]
        }
    },
}
</script>

<style lang="scss" scoped>
  @use '../styles/partials/mixins' as*;
  @use '../styles/partials/variables' as*;

  div.container{
    @include flex(row,space-between,center,nowrap);
    margin: 20px auto;
    ul{
        @include flex(row);
        font-size: 1.1rem;
        
        li{
            margin: 5px;
        }
    }
    img{
        height: 70px;
    }

  }
</style>