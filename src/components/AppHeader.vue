<script>
export default {
    data() {
        return {
            navLinks:[
                {label:'CHARACTERS',url:'#',active:false},
                {label:'COMICS',url:'#',active:true},
                {label:'MOVIES',url:'#',active:false},
                {label:'TV',url:'#',active:false},
                {label:'GAMES',url:'#',active:false},
                {label:'COLLECTIBLES',url:'#',active:false},
                {label:'VIDEO',url:'#',active:false},
                {label:'FANS',url:'#',active:false},
                {label:'NEWS',url:'#',active:false},
                {label:'SHOP',url:'#',active:false}
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
                        <li v-for="(navItem,index) in navLinks" :key="index" :class="{active:navItem.active}">
                            <a :href="navItem.url">{{ navItem.label }}</a>
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
            flex-wrap: wrap;
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