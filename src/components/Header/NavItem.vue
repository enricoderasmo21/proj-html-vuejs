<script>
import LinkItem from './LinkItem.vue';

export default{
    data() {
        return{

            navLink: [
                [
                    {
                        icon: "fa-solid fa-house",
                        title: "",
                        subTitle: "",
                        over: false, 
                    },

                    {
                        icon: "fa-brands fa-pagelines",
                        title: "treatments",
                        subTitle: "Face & Body",
                        over: false, 
                    },

                    {
                        icon: "fa-solid fa-person",
                        title: "about",
                        subTitle: "Our Team",
                        over: false, 
                    },
                ],

                [
                    {
                        icon: "fa-solid fa-heart",
                        title: "journal",
                        subTitle: "Tips & Tricks",
                        over: false,  
                    },
                    
        
                    {
                        icon: "fa-solid fa-bookmark",
                        title: "book now",
                        subTitle: "Special Offers",
                        over: false,   
                    },

                    {
                        icon: "fa-solid fa-plus",
                        title: "",
                        subTitle: "",
                        over: false,    
                    },
                ]
            ],
        }
    },

    components:{
        LinkItem,
    },
}
</script>

<template>

    <nav>
        <div id="link-container">

            <LinkItem v-for="link in this.navLink[0]" :icon="link.icon" :title="link.title.toUpperCase()" :subTitle="link.subTitle" :class="link.over ? 'over' : '', link.active ? 'active' : ''" class="link" @mouseover="link.over = true" @mouseleave="link.over = false"></LinkItem>

            <div id="logo-container">
                <img src="/img/avada-spa-logo-retina-new.png" alt="">
            </div>
        
            <LinkItem v-for="link in this.navLink[1]" :icon="link.icon" :title="link.title.toUpperCase()" :subTitle="link.subTitle" :class="link.over ? 'over' : '', link.active ? 'active' : ''" class="link" @mouseover="link.over = true" @mouseleave="link.over = false"></LinkItem>
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

        width: 80%;
        height: 100%;
        
        #logo-container{
            width: 250px;
            
            img{
                width: 100%;
            }
        }
        
        .link{
            cursor: pointer;
            &.over{
                color: #33a7b9;
            }

            &.active{
                color: #33a7b9;
            }
        }

    }
}
    

</style>