<script>
import { objectToString } from '@vue/shared';

export default{
    data() {
        return{

        }
    },

    props: {
        icon: String,
        title: String,
        subTitle: String,
    }
}
</script>

<template>

    <div class="link-container">

        <i :class="icon" class="icon"></i>

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

    color: #6f727b;

    font-family: 'Montserrat', sans-serif;

    .icon{
        font-size: 0.8em;
    }

    .title{
        font-size: 0.7em;
        font-weight: bold;
        letter-spacing: 1px;
    }

    .subtitle{
        font-size: 0.5em;
    }   
}


</style>