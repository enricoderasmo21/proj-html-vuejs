<script>
export default{
    data() {
        return{

        }
    },

    props: {
        card: Object,
    }
}
</script>

<template>

    <div class="card">

        <div class="toggle-container">
            <div class="img-container">
                <img :src="card.img" alt="">
            </div>
    
            <div class="secondary">
                <em>{{ card.title }}</em>
            </div>
        </div>

        <div class="info-container">
            <div class="title">
                {{ card.title }}
            </div>
    
            <div class="row"></div>
    
            <div class="info">
                {{ card.info }}
            </div>

        </div>


    </div>
 
</template>

<style scoped lang="scss">

.card{
    display: flex;
    flex-direction: column;

    width: calc(100% / 4);

    .toggle-container{
        position: relative;

        width: 100%;
        height: 422px;


        .img-container{
            width: 100%;
            
            border-right: 1.5px solid white;
    
            img{
                width: 100%;
    
            }
        }
    
        .secondary{
            position: absolute;
            top: 0;
            left: 0;
    
            display: none;
            justify-content: center;
            align-items: center;
    
            width: 100%;
            height: 100%;
    
            border-right: 1.5px solid white;
    
            font-size: 1.4em;
            color: #b9afa1;
    
            background-color: white;

            transition: background-color 1s ease-in-out 100ms;

            &:hover{
                background-color: #b9afa1;
                color: white;  
            }

            
        }

        &:hover .secondary{
            display: flex;

            cursor: pointer;
        }
    }

    .info-container{
        display: flex;
        flex-direction: column;
        gap: 20px;


        padding: 20px;

        border-left: 1.5px solid #ebeaea;
        border-right: 1.5px solid #ebeaea;

        .title{
            font-size: 1.4em;
    
            color: #b9afa1;
        }
        .row{
            border-bottom: 2px dotted #b9afa1;
        }

        .info{
            padding-bottom: 10px;

            font-family: 'Lato', sans-serif;
            font-size: 0.9em;
            line-height: 1.5em;
            color: #747474;
        }   
    }
}

</style>