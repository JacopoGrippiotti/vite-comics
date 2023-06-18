<template>
    <footer>
        <div class="footer-top">
            <div class="container footer-jumbo-top" >

                <div class="background-container"></div>

            </div>
        </div>
        
        <div class="footer-bottom">
            <div class="container footer-jumbo-bottom">

            </div>
        </div>
        
    </footer>
    
</template>
<script>
export default {
    name: 'AppFooter',
    data() {
        return {

        }
    },
}
</script>
<style lang="scss">
   @use '../styles/partials/mixins' as*;
   @use '../styles/partials/variables' as*;


   footer{
    height: 780px;
    @include flex(column,none,center,nowrap);
       
       div.footer-top{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        width: 100%;
        height: 350px;

            div.footer-jumbo-top{
                position: relative;
                width: 100%;
                height: 100%;

                div.background-container{
                    position: absolute;
                    background-image: url(../assets/img/dc-logo-bg.png);
                    background-size: cover;
                    width: 500px;
                    height: 100%;
                    background-repeat: no-repeat;
                    left: 54%;
                    background-position: 50%;
                    
                }

            }
       }
       div.footer-bottom{
        background-color: rgb(74, 73, 73);
        height: 100px;
        width: 100%;
       }
       
      
   }

</style>