<script>
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default{
  data(){
    return{

    }
  },

  components: {

    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
  <AppHeader></AppHeader>

  <AppMain></AppMain>

  <AppFooter></AppFooter>
</template>

<style scoped lang="scss">

</style>
