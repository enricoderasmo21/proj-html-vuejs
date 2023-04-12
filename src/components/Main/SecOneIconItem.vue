<script>
export default{
    data() {
        return{

        }
    },

    props:{
        icon: String,
        title: String,
    }
}
</script>

<template>

    <div id="container">
        <i :class="icon" class="icon"></i>
        <div class="title" > {{ title }} </div>
    </div>
 
</template>

<style scoped lang="scss">
#container{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 10px;

    .icon{
        font-size: 3em;
        color: #b9afa1;

        transform: scale(-1, 1);
    }
    .title{
        color: #6f727b;
    }
}

</style>