<script>
import SeriesList from './SeriesList.vue';
export default {
    data() {
        return {
            iconsElements: [
                {imgUrl:'buy-comics-digital-comics.png',text:'DIGITAL COMICS'},
                {imgUrl:'buy-comics-merchandise.png',text:'DC MERCHANDISE'},
                {imgUrl:'buy-comics-subscriptions.png',text:'SUBSCRIPTION'},
                {imgUrl:'buy-comics-shop-locator.png',text:'COMIC SHOP LOCATOR'},
                {imgUrl:'buy-dc-power-visa.svg',text:'DC POWER VISA'},
            ],
            
        }
    },
    components:{
        SeriesList,

    },
    methods:{
        getImageUrl(imagePath){
            return new URL(`../assets/img/${imagePath}`, import.meta.url).href;
        },
    },
}
</script>

<template>
    <main>
        <section class="jumbotron">
            <img id="jumbo-img" src="../assets/img/jumbotron.jpg" alt="jumbotronDc">
        </section>
        <section id="current-series">
            <h2 class="box title-section">Current Series</h2>
            <div class="content-series">
                <SeriesList />
            </div>
            <div id="more-info">
                <a class="box" href="#">Load More</a>
            </div>
        </section>
        <section id="options">
            <ul>
                <li v-for="(iconItem, index) in iconsElements" :key="index">
                    <img :src="getImageUrl(iconItem.imgUrl)">
                    <span> {{iconItem.text}}</span>
                </li>
            </ul>
        </section>
        
    </main>
</template>

<style lang="scss" scoped>
    main{
        .jumbotron{
            color: white;
            height: 350px;
            overflow: hidden;
            #jumbo-img{
                width: 100%;
                height: auto;
            }
        }
        #current-series{
            color: white;
            height: 800px;
            background-color: black;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            padding-left: 20px;

            .content-series{
            display: flex;
            align-items: center;
            }
            .box{
                background-color: blue;
                color: white;
                width: 200px;
                padding: 10px 15px;
            }
            .title-section{
                position: absolute;
                top: -25px;
                left: 15px;
                right: 0;

            }
            #more-info{
                margin: 30px 0;
            }
            
        }
        #options{
            height: 300px;
            background-color: blue;
            display: flex;
            align-items: center;
            justify-content: center;
            ul{
                display: flex;
                align-items: center;
                justify-content: space-around;
                flex-wrap: wrap;
                li{
                    display: flex;
                    flex-wrap: wrap;
                    align-items: center;
                    gap: 5px;
                    font-size: 14px;
                    margin-right: 15px;
                    img{
                        width:100px;
                        height: 100px;
                    }
                        
                }
            }
        }

        
    }

</style>