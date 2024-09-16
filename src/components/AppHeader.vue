<script>
export default {
    data() {
        return {
            navLinks:['CHARACTERS','COMICS','MOVIES','TV','GAMES','COLLECTIBLES','VIDEO',
                'FANS','NEWS','SHOP'
            ],
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <section class="main-logo">
                <img src="../assets/img/dc-logo.png" alt="dc logo">
            </section>
            <section class="navbar">
                <nav>
                    <ul>
                        <li v-for="navItem in navLinks">
                            <a href="#">{{ navItem }}</a>
                        </li>

                    </ul>
                </nav>
            </section>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    header{
        background-color: white;
        margin: 30px auto;
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        a{
            color: black;
        }
        ul{
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: 700;

            li{
                padding: 20px 10px;

                &:hover,
                &.active{
                    border-bottom: 5px solid blue;
                }
            }
        }

    }
</style>