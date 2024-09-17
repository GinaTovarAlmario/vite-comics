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
            comicsLinksList:[
                {label:'CHARACTERS', url:'#'},
                {label:'COMICS', url:'#'},
                {label:'MOVIES',ulr:'#'},
                {label:'TV',ulr:'#'},
                {label:'GAMES',ulr:'#'},
                {label:'VIDEO',ulr:'#'},
                {label:'NEWS',ulr:'#'}
            ],
            shopLinksList:[
                {label:'SHOP DC',ulr:'#'},
                {label:'SHOP DC COLLECTIBLES',ulr:'#'}
            ],
            dcLinksList:[
                {label:'Terms of use',ulr:'#'},
                {label:'Privacy Policy(new)',ulr:'#'},
                {label:'Ad choices',ulr:'#'},
                {label:'Advertising',ulr:'#'},
                {label:'Jobs',ulr:'#'},
                {label:'Subscritions',ulr:'#'},
                {label:'Talent Workshop',ulr:'#'},
                {label:'CSPC Certificates',ulr:'#'},
                {label:'Ratings',ulr:'#'},
                {label:'Shop Help',ulr:'#'},
                {label:'Contact Us',ulr:'#'}
            ],
            sitesLinks:[ 
                {label:'DC',ulr:'#'},
                {label:'MAD Magazine',ulr:'#'},
                {label:'DC Kids',ulr:'#'},
                {label:'DC Universe',ulr:'#'},
                {label:'DC Power visa',ulr:'#'}
            ],
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="footer-links">
                <section id="comics">
                    <div class="title">
                        <h4>DC COMICS</h4>
                    </div>
                    <div class="list">
                        <ul>
                            <li v-for="(comicLinkItem,index) in comicsLinksList" :key="index">
                                <a :href="comicLinkItem.url">{{comicLinkItem.label}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="title">
                        <h4>SHOP</h4>
                    </div>
                    <div class="list">
                        <ul>
                            <li v-for="(shopLinkItem,index) in shopLinksList" :key="index">
                                <a :href="shopLinkItem.url">{{ shopLinkItem.label }}</a>
                            </li>
                        </ul>
                    </div>                   
                </section>
                <section id="dc">
                    <div class="title">
                        <h4>DC</h4>
                    </div>
                    <div class="list">
                        <ul>
                            <li  v-for="(dcItemList,index) in dcLinksList" :key="index">
                                <a :href="dcItemList.url">{{ dcItemList.label}}</a>
                            </li>
                        </ul>
                    </div>
                </section>
                <section id="sites">
                    <div class="title">
                        <h4>SITES</h4>
                    </div>
                    <div class="list">
                        <ul>
                            <li v-for="(siteItem,index) in sitesLinks" :key="index">
                                <a :href="siteItem.url">{{ siteItem.label}}</a>
                            </li>
                        </ul>
                    </div>
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
                <img v-for="(itemList,index) in socialsList" :key="index" :src=itemList.link :alt="itemList.name">
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
        section{
            height: 350px;
            font-size: 16px;
            padding-top: 20px;
        }
        .footer-links{
            flex-basis: 60%;
            display: flex;
            align-items: center;
            justify-content: space-around;
            .list{

                ul{
                margin: 20px 0;
                
                    li{
                        display: flex;
                        flex-direction: column;
                        align-items: baseline;
                        padding: 3px 0;
                        a{
                            color: grey;
                            cursor: pointer;
                        }
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