<script>
export default{
    data() {
        return{

        }
    }
}

</script>

<template>

    <div id="jumbo-container">
        <img src="/img/avada-spa-slider-image-1-new.jpg" alt="">

        <div class="jumbo-text">
            <div class="text"> <em>Give yourself permission</em></div>
            <div class="title">Relax, Revive & Rejuvenate</div>

            <button id="btn">EXPLORE TREATMENTS</button>
        </div>

        <div id="labels-container">
            <div class="label">
                <i class="fa-solid fa-laptop icon"></i>
                <div class="text">Demos</div>
            </div>
            <div class="label">
                <div id="price">
                    <span id="dollar">$</span>
                    <span id="num">39</span>
                </div>
                <div class="text">On Sale</div>
                
            </div>
        </div>
    </div>

</template>

<style scoped lang="scss">
#jumbo-container{
    position: relative;

    width: 100%;
    height: 650px;

    overflow: hidden;

    img{
        width: 100%;

        object-fit: contain;
        object-position: 0 -150px;
    }

    .jumbo-text{
        position: absolute;
        top: 43%;
        left: 50%;
        transform: translate(-50%, -50%);

        text-align: center;
        color: white;

        .text{
            font-size: 2em;
        }

        .title{
            font-size: 4.6em;
            white-space: nowrap;
        }

        #btn{
            padding: 10px 28px;
            margin-top: 24px;

            font-family: 'Montserrat', sans-serif ;
            font-weight: bold;
            font-size: 0.7em;
            color: white;
            letter-spacing: 1px;

            background-color: #b9afa1;

            border-style: none;
            border-radius: 50px;

            cursor: pointer;

            &:hover{
                background-color: #33a7b9;
            }
        }   
    }

    #labels-container{
        position: absolute;
        top: 40px;
        right: 12px;

        display: flex;
        flex-direction: column;
        gap: 8px;

        .label{
            position: relative;

            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 4px;

            width: 54px;
            height: 54px;

            background-color: white;

            border-radius: 6px;

            font-family: 'Montserrat', sans-serif;

            cursor: pointer;

            .icon{
                font-size: 1.4em;
            }

            .text{
                font-size: 0.6em;
                font-weight: bold;
            }

            #price{
                font-weight: bold;

                color: #63bb7a; 
                
                #dollar{
                    position: relative;
                    bottom: 6px;

                    font-size: 0.8em;
                }

                #num{
                    font-size: 1.2em;
                }
            }

           
        }
    }
}

</style>