<script>
export default{
    data() {
        return{

        }
    }
}
</script>

<template>
    <footer>
        <div id="container">
            
            <div id="logo-container">
                <img src="/img/avada-spa-logo-retina-new.png" alt="">
            </div>

            <div id="copyright">&copy;COPIRIGHT 2012-2020 | AVADA THEME BY THEMEFUSION | ALL RIGHTS RESERVED | POWERED BY <br> WORDPRESS</div>

            <div id="social-container">
                <div class="social">
                    <i class="fa-brands fa-facebook-f"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-twitter"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <div class="social">
                    <i class="fa-brands fa-youtube"></i>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
#container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    padding: 20px 50px 0 50px;

    height: 95px;

    border-top: 8px solid #e9eaee;

    #logo-container{
        width: 200px;

        img{
            width: 100%
        }
    }

    #copyright{
        font-family: 'Lato', sans-serif;
        font-size: 0.6em;
        color: #aeb2bd;

        text-align: center;
        line-height: 1.3em;
    }

    #social-container{
        display: flex;
        flex-direction: row;
        gap: 10px;

        .social{
            padding: 8px 10px;

            color: #bdbcbc;

            border-radius: 4px;

            background-color: #e8e8e8;

            cursor: pointer;
        }
    }
}

</style>