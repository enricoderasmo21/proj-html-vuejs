<script>
import { objectToString } from '@vue/shared';

export default{
    data() {
        return{

        }
    },

    props: {
        img: String,
        title: String,
        subTitle: String,
    }
}
</script>

<template>

    <div class="link-container">

        <div class="img-container">
            <img :src="img" alt="">
        </div>

        <div class="title"> {{ title }} </div>

        <div class="subtitle"> {{ subTitle }} </div>

    </div>


    
</template>

<style scoped lang="scss">

.link-container{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;

    .title{
        font-size: 0.8em;
        color: #6f727b;
    }

    .subtitle{
        font-size: 0.6em;
        color: #6f727b;
    }
}


</style>