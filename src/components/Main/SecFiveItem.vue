<script>
export default{
    data() {
        return{

        }
    }
}
</script>

<template>
    <section>
        <div id="container">
            <div id="inner-container">
                <div id="discount-container">
                    <div id="num">25%</div>
                    <div id="offer">SPECIAL OFFER</div>
                </div>
                <div id="text">
                    <div id="phrase"><em>Take some time. Treat yourself. You deserve it.</em></div>
                    <div id="discount-info">Book a treatment this month and receive a 25% on all further treatments.</div>
                </div>
                <button id="btn">BOOK NOW</button>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
#container{
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100%;
    min-height: 300px;

    background-image: url(/img/ptb_cta-new.jpg);
    background-size: cover;
    background-position: 0 -35px;

    #inner-container{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 30px;

        width: 60%;
        height: 100%;

        #discount-container{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 6px;

            padding: 20px;

            border: 1px solid #b9afa1;

            font-family: 'Lato', sans-serif;
            color: white;

            #num{
                font-size: 3.2em;
            }

            #offer{
                font-size: 0.7em;

            }
        }

        #text{
            color: white;
            line-height: 2.4em;

            #phrase{
                font-family: 'Libre Baskerville', serif;
                font-size: 1.5em;
            }

            #discount-info{
                font-family: 'Lato', sans-serif;
                font-size: 0.9em;

            }
        }

        #btn{
            padding: 10px 28px;
            margin-left: 60px;

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
}
</style>