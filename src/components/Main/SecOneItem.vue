<script>
import SecOneIconItem from './SecOneIconItem.vue';

export default{
    data() {
        return{

            icons: [
                {
                    icon: "fa-solid fa-hands",
                    text: "Messages"
                },
                {
                    icon: "fa-regular fa-face-smile",
                    text: "Therapy"
                },
                {
                    icon: "fa-solid fa-heart",
                    text: "Relaxing"
                },
                {
                    icon: "fa-regular fa-moon",
                    text: "Meditation"
                },
                {
                    icon: "fa-solid fa-snowflake",
                    text: "Natural Beauty"
                },
            ]

        }
    },

    components: {
        SecOneIconItem,
    }
}
</script>

<template>
    <section>
        <div id="container-centered">

            <div id="inner-top">
                <div id="title">Luxury Spa Experiences</div>
                <i class="fa-solid fa-leaf icon"></i>
                <div id="subtitle"><em>Morbi pharetra, quam id consequat imperdiet, lectus est tincidunt massa, eu posuere leo nibh non fermentum</em></div>
                <div id="row"></div>
                <div id="paragraph">Vestibulum nec velit ante. Prasent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo. Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.</div>
                <button id="btn">OUR APPROACH</button>
            </div>

            <div id="inner-bottom">

                <SecOneIconItem v-for="icon in icons" :icon="icon.icon" :title="icon.text" class="flex"></SecOneIconItem>

            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">

#container-centered{
    margin: 80px auto;

    width: 60%;

    #inner-top{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 24px;

        padding: 0 60px;
        margin: 0 auto;

        width: 80%;

        text-align: center;

        #title{
            font-size: 3.6em;
            color: #6f727b;
        }

        .icon{
            font-size: 1.8em;
            color: #b9afa1;
        }

        #subtitle{
            font-size: 1.6em;
            color: #b9afa1;
        }

        #row{
            width: 10%;

            border-bottom: 2px solid #b9afa1;
        }

        #paragraph{
            font-family: 'Montserrat', sans-serif;
            font-size: 0.9em;
            line-height: 1.6em;
            color: #6f727b;
        }

        #btn{
            margin-top: 20px;
            padding: 10px 28px;

            background-color: white;

            border-style: none;
            border: 3px solid #b9afa1;
            border-radius: 50px;

            font-family: 'Montserrat', sans-serif ;
            font-weight: bold;
            font-size: 0.7em;
            color: #b9afa1;
            letter-spacing: 1px;

            cursor: pointer;

            &:hover{
                color: #33a7b9;
                border-color: #33a7b9;
            }
        }

    }

    #inner-bottom{
        display: flex;
        flex-direction: row;
        justify-content: space-between;

        margin-top: 80px;

        width: 100%;

        translate: 28px 0;

        .flex{
            &:nth-child(2) {
                translate: 0 50px;
            }

            &:nth-child(4) {
                translate: 0 50px;
            }
        }

    }
}
</style>