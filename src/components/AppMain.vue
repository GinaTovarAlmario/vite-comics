<script>
export default {
    data() {
        return {
        }
    }
}
</script>

<template>
    <main>
            <section class="jumbotron">
                <div class="top-jumbo">
                     --Content goes here--
                </div>
                 <div class="bottom-jumbo">
                    <ul>
                        <li>
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="comics">
                            <span> DIGITAL COMICS</span>
                        </li>
                        <li>
                            <img src="../assets/img/buy-comics-merchandise.png" alt="merch">
                            <span>DC MERCHANDISE</span>
                        </li>
                        <li>
                            <img src="../assets/img/buy-comics-subscriptions.png" alt="subscription">
                            <span>SUBSCRIPTION</span>
                        </li>
                        <li>
                            <img src="../assets/img/buy-comics-shop-locator.png" alt="locator">
                            <span>COMIC SHOP LOCATOR</span>
                        </li>
                        <li>
                            <img class="img-special" src="../assets/img/buy-dc-power-visa.svg" alt="visa">
                            <span>DC POWER VISA</span>
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
                    li{
                        display: flex;
                        align-items: center;
                        padding: 0 30px;
                        gap: 5px;

                        .img-special{
                           width:80px;
                           height: 90px;
                        }
                    }
                }
            }

        }
    }

</style>