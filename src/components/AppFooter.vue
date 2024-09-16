<script>
export default {
    data() {
        return {
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
                            <a href="#">CHARACTERS</a>
                            <a href="#">COMICS</a>
                            <a href="#">MOVIES</a>
                            <a href="#">TV</a>
                            <a href="#">GAMES</a>
                            <a href="#">VIDEO</a>
                            <a href="#">NEWS</a>
                        </li>
                        <li>
                            <h4>SHOP</h4>
                            <a href="#">SHOP DC</a>
                            <a href="#">SHOP DC COLLECTIBLES</a>
                        </li>
                    </ul>
                </section>
                <section id="dc">
                    <ul>
                        <li>
                            <h4>DC</h4>
                            <a href="#">Terms of use</a>
                            <a href="#">Privacy Policy(new)</a>
                            <a href="#">Ad choices</a>
                            <a href="#">Advertising</a>
                            <a href="#">Jobs</a>
                            <a href="#">Subscritions</a>
                            <a href="#">Talent Workshop</a>
                            <a href="#">CSPC Certificates</a>
                            <a href="#">Ratings</a>
                            <a href="#">Shop Help</a>
                            <a href="#">Contact Us</a>
                        </li>
                    </ul>
                </section>
                <section id="sites">
                    <ul>
                        <li>
                            <h4>SITES</h4>
                            <a href="#"> DC</a>
                            <a href="#">MAD Magazine</a>
                            <a href="#">DC Kids</a>
                            <a href="#">DC Universe</a>
                            <a href="#">DC Power visa</a>
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
                <img src="../assets/img/footer-facebook.png" alt="facebook">
                <img src="../assets/img/footer-twitter.png" alt="twitter">
                <img src="../assets/img/footer-youtube.png" alt="youtube">
                <img src="../assets/img/footer-pinterest.png" alt="pinterest">
                <img src="../assets/img/footer-periscope.png" alt="periscope">
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
                    padding: 0 20px;

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