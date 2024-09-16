<script>
export default {
    data() {
        return {
            socialsList:[
                {link:"../src/assets/img/footer-facebook.png",name:'facebook'},
                {link:"../src/assets/img/footer-twitter.png",name:'twitter'},
                {link:"../src/assets/img/footer-youtube.png",name:'youtube'},
                {link:"../src/assets/img/footer-pinterest.png",name:'pinterest'},
                {link:"../src/assets/img/footer-periscope.png",name:'periscope'},
            ],
            comicsLinksList:['CHARACTERS','COMICS','MOVIES','TV','GAMES','VIDEO','NEWS'],
            shopLinksList:['SHOP DC','SHOP DC COLLECTIBLES'],
            dcLinksList:['Terms of use','Privacy Policy(new)','Ad choices','Advertising','Jobs','Subscritions',
                'Talent Workshop','CSPC Certificates','Ratings','Shop Help','Contact Us'],
            sitesLinks:[ 'DC','MAD Magazine','DC Kids','DC Universe','DC Power visa'],
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="footer-links">
                <section id="comics">
                    <ul>
                        <li>
                            <h4>DC COMICS</h4>
                            <a href="#" v-for="comicLinkItem in comicsLinksList">{{comicLinkItem}}</a>
                        </li>
                        <li>
                            <h4>SHOP</h4>
                            <a href="#" v-for="shopLinkItem in shopLinksList">{{ shopLinkItem }}</a>
                        </li>
                    </ul>
                </section>
                <section id="dc">
                    <ul>
                        <li>
                            <h4>DC</h4>
                            <a href="#" v-for="dcItemList in dcLinksList">{{ dcItemList }}</a>
                        </li>
                    </ul>
                </section>
                <section id="sites">
                    <ul>
                        <li>
                            <h4>SITES</h4>
                            <a href="#" v-for="siteItem in sitesLinks">{{ siteItem }}</a>
                        </li>
                    </ul>
                </section>
            </div>
            <div class="logo-footer">
                <img src="../assets/img/dc-logo-bg.png" alt="logo">
            </div>
        </div>
        <div class="footer-bottom">
            <div class="sign-up">
                <button> SIGN-UP NOW!</button>
            </div>
            <div class="socials">
                <span class="follow">FOLLOW US</span>
                <img v-for="itemList in socialsList" :src=itemList.link :alt="itemList.name">
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer{
    color: grey;
    h4{
        color: white;
    }
    .footer-top{
        height: 350px;
        background-image: url(../assets/img/footer-bg.jpg);
        display: flex;
        align-items: center;
        .footer-links{
            display: flex;
            flex-basis: 60%;
            align-items: baseline;            
            ul{
                margin: 20px 0;
                
                li{
                    display: flex;
                    flex-direction: column;
                    align-items: baseline;
                    gap: 5px;
                    padding: 10px 20px;

                    a{
                        color: grey;
                    }
                }
            }
        }
        .logo-footer{
            display: flex;
            flex-basis: 40%;
            justify-content: center;
            img{
                height: 300px;
            }
        }
    }
    .footer-bottom{
        height: 100px;
        background-color: #303030;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding : 0 20px;

        .sign-up{
            button{
                color: white;
                padding: 10px 15px;
                border-color: blue;
                background-color: #303030;
                cursor: pointer;
            }
        }
        .socials{
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 15px;
            cursor: pointer;
            .follow{
                color: blue;
            }
        }
    }

}
</style>