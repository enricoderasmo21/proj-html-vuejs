<script>
import LinkItem from './LinkItem.vue';

export default{
    data() {
        return{

            navLinkLeft: [
                [
                    {
                        image: "",
                        title: "treatments",
                        subTitle: "Face & Body"
                    },
    
                    {
                        image: "",
                        title: "about",
                        subTitle: "Our Team"
                    },
                ],

                [
                    {
                        image: "",
                        title: "journal",
                        subTitle: "Tips & Tricks"
                    },
        
                    {
                        image: "",
                        title: "book now",
                        subTitle: "Special Offers"
                    },
                ]
            ],
        }
    },

    components:{
        LinkItem,
    }
}
</script>

<template>

    <nav>
        <div id="link-container">
            <i class="icon fa-solid fa-house"></i>

            <LinkItem v-for="link in this.navLinkLeft" :img="link[0].image" :title="link[0].title.toUpperCase()" :subTitle="link[0].subTitle"></LinkItem>

            <div id="logo-container">
                <img src="/img/avada-spa-logo-retina-new.png" alt="">
            </div>
        
            <LinkItem v-for="link in this.navLinkLeft" :img="link[1].image" :title="link[1].title.toUpperCase()" :subTitle="link[1].subTitle"></LinkItem>

            <i class="icon fa-solid fa-plus"></i>
        </div>
    </nav>


</template>

<style scoped lang="scss">

nav{
    display: flex;
    justify-content: center;

    width: 100%;
    height: 80px;

    #link-container{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 50px;

        width: 60%;
        height: 100%;
        
        #logo-container{
            width: 250px;
            
            img{
                width: 100%;
            }
        }

        .icon{
            font-size: 0.8em;
            color: #6f727b;
        }
        
    }
}
    

</style>