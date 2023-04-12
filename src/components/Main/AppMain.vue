<script>
import SecOneItem from './SecOneItem.vue';
import SecTwoItem from './SecTwoItem.vue';
import SecThreeItem from './SecThreeItem.vue';
import SecFourItem from './SecFourItem.vue';
import SecFiveItem from './SecFiveItem.vue';

export default{
    data() {
        return{

        }
    },

    components: {
        SecOneItem,
        SecTwoItem,
        SecThreeItem,
        SecFourItem,
        SecFiveItem
    }
}
</script>

<template>
    <SecOneItem></SecOneItem>

    <SecTwoItem></SecTwoItem>

    <SecThreeItem></SecThreeItem>

    <SecFourItem></SecFourItem>

    <SecFiveItem></SecFiveItem>
</template>

<style scoped lang="scss">

</style>