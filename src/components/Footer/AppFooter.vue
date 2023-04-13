<script>
export default{
    data() {
        return{

        }
    },

    methods:{
        scrollBack(){
            document.documentElement.scrollTop = 0;
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

        <div id="scroll-back-btn" @click="scrollBack()">
            <i class="fa-solid fa-chevron-up"></i>
        </div>
    </footer>
</template>

<style scoped lang="scss">
footer{
    position: relative;

    #container{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    
        padding: 12px 50px 0 50px;
    
        height: 120px;
    
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

    #scroll-back-btn{
        position: fixed;
        right: 60px;
        bottom: 0;

        z-index: 2;

        display: flex;
        align-items: center;
        justify-content: center;

        padding: 8px 14px 3px 14px;

        font-size: 0.8em;
        color: white;

        background-color: #474747;

        border-radius: 4px 4px 0 0;

        cursor: pointer;
    }
}

</style>