<script>
export default{
    data() {
        return{

            treatments: [
                {
                    name: "Oil Massage",
                    price: "$ 62 For 2 Hours",
                    description: "Lorem ipsum dolor sit amet",
                    active: false,
                },

                {
                    name: "Manicure",
                    price: "$ 14 For 1 Hour",
                    description: "Lorem ipsum dolor sit amet",
                    active: false,
                },

                {
                    name: "Aromatherapy",
                    price: "$ 40 For 2 Hours",
                    description: "Lorem ipsum dolor sit amet",
                    active: false,
                },
            ]
        }  
    },

    methods: {

        clicked(index){
            if(this.treatments[index].active == false){
                
                this.treatments[index].active = true;

            } else {

                this.treatments[index].active = false;
            }
        }

    }
}
</script>

<template>
    <section>
        <div id="container">
            <div id="inner-container">

                <div id="img-container">
                    <div id="img-inner-container">
                        <img src="/img/face_and_body_treatments-new.jpg" alt="">
                    </div>
                </div>

                <div id="info-container">

                    <div id="title">Face & Body Treatments</div>
                    <div id="paragraph">Pellentesque nec felis efficitur, sagittis eros et, pharetra risus. Sed at lacus a ex imperdiet dignissim vehicula quam. Vestibulum ante ipsum primis.</div>

                    <div id="treatments-container">
                        <div v-for="(treatment, index) in treatments" class="treatment">
                            <div class="treatments-title">
                                <div class="button plus" @click="clicked(index)" v-show="treatment.active == false">
                                    <i  class="fa-solid fa-plus"></i>
                                </div>
                                <div class="button minus" @click="clicked(index)" v-show="treatment.active == true">
                                    <i  class="fa-solid fa-minus minus"></i>
                                </div>
                                <div class="text"> <em>{{ treatment.name }}</em> </div>
                            </div>
                            <div class="treatment-description" v-show="treatment.active">
                                <div class="info"> <strong>{{ treatment.price }}</strong> - {{ treatment.description }} </div>
                            </div>
                        </div>
                    </div>
                    <button id="btn">BOOK AN APPOINTMENT</button>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
#container{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;

    min-height: 1000px;

    background-color: #f9f9f9;

    #inner-container{
        display: flex;
        flex-direction: row;
        gap: 80px;

        padding-top: 90px;
        
        #img-container{
            padding: 18px;
    
            width: 500px;
            height: 710px;
    
            background-color: white;

            box-shadow: 4px 4px 6px rgba(0,0,0, 0.2);

            #img-inner-container{
                overflow: hidden;

                img{
                    width: 100%;
    
                    transition: all .8s ease-in-out; 
    
                    &:hover{
                        transform: scale(1.6);
                    }
                }
            }
        }

        #info-container{
            display: flex;
            flex-direction: column;
            gap: 30px;

            padding-top: 40px;

            width: 340px;

            #title{
                font-size: 3.8em;
                color: #6f727b;
                line-height: .9em;
            }

            #paragraph{
                font-family: 'Montserrat', sans-serif;
                font-size: 0.8em;
                color: #6f727b;
                line-height: 1.7em;
            }

            #treatments-container{
                display: flex;
                flex-direction: column;
                gap: 10px;

                .treatment{
                    padding: 12px 20px;

                    background-color: white;
                    
                    border: 1px solid #b9afa1;

                    .treatments-title{
                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        gap: 20px;
                        .button{
                            display: flex;
                            justify-content: center;
                            align-items: center;
    
                            padding: 10px;
    
                            width: 16px;
                            height: 16px;
                            
                            font-size: 0.6em;
                            color: white;
    
                            cursor: pointer;

                            &.plus{
                                background-color: #6f727b;
                            }

                            &.minus{
                                background-color: #b9afa1;
                            }
                        }
                        .text{
                            font-size: 1.3em;
                            color: #b9afa1;
                        }
                    }

                    .treatment-description{
                        margin-top: 10px ;
                        padding: 20px 0px;

                        font-family: 'Montserrat', sans-serif;
                        font-size: 0.8em;

                        .info{
                            color: #747474;
                        }
                    }
                }
            }

            #btn{
                align-self: flex-start;

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
    }
}
</style>