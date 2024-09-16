<script>
export default {
    data() {
        return {
            iconsElements: [
                {img:'../src/assets/img/buy-comics-digital-comics.png',text:'DIGITAL COMICS'},
                {img:'../src/assets/img/buy-comics-merchandise.png',text:'DC MERCHANDISE'},
                {img:'../src/assets/img/buy-comics-subscriptions.png',text:'SUBSCRIPTION'},
                {img:'../src/assets/img/buy-comics-shop-locator.png',text:'COMIC SHOP LOCATOR'},
                {img:'../src/assets/img/buy-dc-power-visa.svg',text:'DC POWER VISA'},
            ],

        }
    }
}
</script>

<template>
    <main>
        <section class="jumbotron">
            <div class="top-jumbo">
                <span>--Content goes here--</span>
            </div>
            <div class="bottom-jumbo">
                <ul>
                    <li v-for="iconItem in iconsElements">
                        <img :src="iconItem.img">
                        <span> {{iconItem.text}}</span>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    main{
        .jumbotron{
            color: white;
            .top-jumbo{
                height: 200px;
                background-color: black;
                font-size: 30px;
                display: flex;
                align-items: center;
                padding-left: 15px;
            }
            .bottom-jumbo{
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
    }

</style>