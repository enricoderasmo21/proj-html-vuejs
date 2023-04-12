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
                <div id="text">
                    <p>"If you want to relax, watch the clouds pass by if you're laying on the grass, or sit in front of the creek; just doing nothing and having those still moments is what really rejuvenates the body..."</p>
                    <div id="author"> FRIEDA FRIEDSON, <span id="job">MASSEUSE</span></div>
                </div>
            </div>
        </div>

    </section>
</template>

<style scoped lang="scss">
#container{
    display: flex;
    justify-content: center;
    align-items: center;

    min-height: 600px;
    width: 100%;

    background-image: url(/img/Home-quota-new.jpg);

    #inner-container{
        width: 35%;

        #text{
            display: flex;
            flex-direction: column;
            gap: 20px;

            font-family: 'Roboto', sans-serif;
            color: rgba(255, 255, 255, 0.75);

            text-align: center;

            p{
                line-height: 1.6em;
                color: white;
            }

            #author{
                font-weight: bold;
                color: white;

                #job{
                    color: rgba(255, 255, 255, 0.75);
                }
            }
        }

    }
}

</style>