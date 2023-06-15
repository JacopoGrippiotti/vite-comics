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
    @include flex(row,space-between,none,nowrap);
    margin: 20px auto;
    ul{
        display: flex;
        font-size: 1.1rem;
        font-weight: bold;
        li{
            margin: 0 5px;
            height: 100%;
            align-items: center;
            display: flex;
            position: relative;
            &:hover a{
                color: blue;
            }

            a{
                color: black;
            }
            
            &::after{
                content: '';
                position: absolute;
                width: 100%;
                top: 100%;
            }
            
            &:hover::after{
                border-bottom: 3px solid blue;
            }
        }


    }
    img{
        height: 70px;
    }

  }
</style>