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
                <div class="signup-button">
                    Sign-up Now!
                </div>

                <div class="contacts">
                    <h2>Follow Us</h2>
                    <img v-for="(icon,index) in iconList" :src="getIcon(index)" alt="">
                </div>
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

            ],
            iconList:[
                "../../src/assets/img/footer-facebook.png",
                "../../src/assets/img/footer-twitter.png",
                "../../src/assets/img/footer-youtube.png",
                "../../src/assets/img/footer-pinterest.png",
                "../../src/assets/img/footer-periscope.png"
            ]
        }

    },
                methods:{
                    getIcon(index){
                     return this.iconList[index]
                    }
                }
}
</script>
<style lang="scss">
   @use '../styles/partials/mixins' as*;
   @use '../styles/partials/variables' as*;


   footer{
    height: 100%;
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
        background-color: rgb(63, 61, 61);
        height: 100px;
        width: 100%;
        @include flex(row,space-between,center,nowrap);
           
        div.footer-jumbo-bottom{
            margin: 0 auto;
            @include flex(row,space-between,center,nowrap);
              
            div.signup-button{
                 border: 1px solid blue;
                 width: 13%;
                 color: white;
                 font-size: 1.2rem;
                 text-align: center;
                 padding: 8px;
                 font-weight: bold;
                }
 
              div.contacts{
                display: flex;
                width: 27%;
                margin: 10px 10px;

                h2{
                    margin-right: 20px;
                    color: rgb(56, 125, 246);
                    font-weight: 700;
                }
                img{
                    height: 30px;
                    margin: 0 5px;
                }
              }
            }     
        }
   }

</style>