<script>
export default {
    data() {
        return {
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
                        <li><a href="#">CHARACTERS</a></li>
                        <li class="active"><a href="#">COMICS</a></li>
                        <li><a href="#">MOVIES</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">GAMES</a></li>
                        <li><a href="#">COLLECTIBLES</a></li>
                        <li><a href="#">VIDEO</a></li>
                        <li><a href="#">FANS</a></li>
                        <li><a href="#">NEWS</a></li>
                        <li><a href="#">SHOP</a></li>
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