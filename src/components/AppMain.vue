<script>
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
            <span>--Content goes here--</span>
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
            height: 300px;
            background-color: black;
            font-size: 30px;
            display: flex;
            align-items: center;
            padding-left: 15px;
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