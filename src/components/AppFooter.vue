<template>
    <footer>
        <div>
            <div class="container footer-jumbo-top" >

            </div>
        </div>
        
        <div>
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
    height: 900px;
    @include flex(column,center,center,nowrap);

       div.footer-jumbo-top{
        height: 70%;
       }
       div.footer-jumbo-bottom{
        height: 30%;
       }
   }

</style>