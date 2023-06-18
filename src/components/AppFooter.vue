<template>
    <footer>
        <div class="footer-top">
            <div class="container footer-jumbo-top" >
                    <div class="list-container" v-for="(item,index) in listItems">
                        <h1>{{ item.title }}</h1>
                        <ul>
                            <li v-for="item in listItems[index].items" >{{ item }}</li>
                        </ul>
                    </div>

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
            listItems:[
                {
                    title:"Dc comics",
                    items:["Characters",
                           "Comics",   
                           "Movies",
                           "TV",
                           "Games",
                           "Videos",
                           "News"]
                },
                {
                    title:"Shop",
                    items:["Shop DC",
                           "Shop DC Collectibles"]
                },
                {
                    title:"DC",
                    items:["Terms Of Use",
                           "Privacy policy (New)" ,  
                           "Ad Choices" ,  
                           "Advertising" ,  
                           "Jobs" ,  
                           "Subscriptions" ,  
                           "Talent Workshops" ,  
                           "CPSC Certificates" ,  
                           "Ratings" ,  
                           "Shop Help" ,  
                           "Contact Us" ]
                },
                {
                    title:"Sites",
                    items:["DC",
                           "Mad Magazine",
                           "DC Kids",
                           "DC Universe",
                           "DC Power Visa"]
                }

            ]
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
                height: 100%;
                display: flex;
                flex-direction: column;
                flex-wrap: wrap;
                margin: 0 auto;
                align-content: flex-start;

                div.list-container{
                    width: 15%;
                    margin-top: 30px;
                    color: white;

                    h1{
                        font-size: 1.3rem;
                        font-weight: 700;
                    }

                    li{
                        margin-top: 4px;
                        font-size: 0.85rem;
                    }
                }
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