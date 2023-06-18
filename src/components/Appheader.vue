<template>

    <header>
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
    </header>
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

  header{
    height: $sectionsHeight;
    @include flex(row, center,center,nowrap);
  }
  div.container{
    @include flex(row,space-between,none,nowrap);
    
    ul{
        display: flex;
        font-size: 1.1rem;
        font-weight: bold;
        li{
            margin: 0 5px;
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
                top: 115%;
                right: 0;
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