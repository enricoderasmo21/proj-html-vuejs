<script>
import CardItem from './CardItem.vue';

export default{
    data() {
        return{

            treatments: [
                {
                    img: "img/Layer-1-new.jpg",
                    title: "Hydrotherapy",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-2-new.jpg",
                    title: "Massage",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-3-new.jpg",
                    title: "Aromatherapy",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-4-new.jpg",
                    title: "Heat Therapy",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-5-new.jpg",
                    title: "Skin Care",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-6-new.jpg",
                    title: "Spa Days",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/layer8-new.jpg",
                    title: "Beauty Treatments",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },

                {
                    img: "img/Layer-7-new.jpg",
                    title: "Residential",
                    info: "Vestibulum nec velit ante. Praesent dignissim interdum est, in lacinia elit pretium nec. Aliquam erat volutpat. Fusce laoreet mi leo.",
                },
            ]

        }
    },

    components: {
        CardItem,
    }
}
</script>

<template>
    <section>

        <div id="title-container">
            <div id="title">OUR TREATMENTS</div>
        </div>
        <div id="treatments-container">

            <CardItem v-for="card in treatments" :card="card"></CardItem>

        </div>



    </section>
</template>

<style scoped lang="scss">

#title-container{
    display: flex;
    justify-content: center;
    align-items: center;

    height: 180px;

    background-image: url(/img/ptb_cta-new.jpg);
    background-position: 0px -210px;
    background-size: cover;

    #title{
        font-size: 2.2em;
        color: white;
    }
}

#treatments-container{
    display: flex;
    flex-flow: row wrap;

    border: 1px solid white;
}
</style>