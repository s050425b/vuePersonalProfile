<template>
    <div id="display">
        <div class="project" style="background-color: rgb(245, 165, 46);">
            <div class="image">
                <img id="project3-img" src="../assets/resource/photo/Screenshot 2020-09-10 at 12.20.55 AM.png" alt="">
            </div>
            <div class="description" style="color:white;">
                <span>In this website, there are...</span>
                <ul class="project1-ul">
                    <li><img v-bind:src="picture" />Yelp clone</li>
                    <li><img v-bind:src="picture" />Yelp API interaction</li>
                    <li><img v-bind:src="picture" />React framework</li>
                </ul>
                <a class="link" href="https://s050425b.github.io/s050425b5b.github.io/" v-on:mouseover="enterHandle" v-on:mouseout="outHandle" >Click here to access</a>
            </div>
        </div>
        <div class="project" style="background-color: rgb(2, 11, 94);">
            <div class='description' style="color:white;">
                <span>In this website, there are...</span>
                <ul id="secondProject-ul">
                    <li><img v-bind:src="picture"/>NASA API</li>
                    <li><img v-bind:src="picture" />Everyday updated mainpage</li>
                    <li><img v-bind:src="picture" />API search</li>
                </ul>
                <a class="link" v-on:mouseover="enterHandle" v-on:mouseout="outHandle" href="https://s050425b.github.io/s050425b2.github.io/">Click here to access</a>
            </div>
            <div class="image" id="project2-img">
                <img src="../assets/resource/photo/Screenshot 2020-09-08 at 7.23.06 PM.png" alt="">
            </div>
        </div>
        <div class="project" style="background-color: paleturquoise;">
            <div class="image">
                <img src="../assets/resource/photo/Screenshot 2020-09-08 at 6.35.45 PM.png" alt="">
            </div>
            <div class="description">
                <span>In this website, there are...</span>
                <ul class="project1-ul">
                    <li> <img v-bind:src="picture" /> Mouse Game  </li>
                    <li><img v-bind:src="picture" />Mini Keyboard Game</li>
                    <li><img v-bind:src="picture" />Otter photo</li>
                </ul>
                <a v-on:mouseover="enterHandle" v-on:mouseout="outHandle" class="link" href="https://s050425b.github.io">Click here to access</a>
            </div>
        </div>
    </div>
</template>

<script>
import $ from 'jquery';

export default {
    data(){
        return {
            picture: require("../assets/resource/photo/pngguru.com.png")
        }
    },
    methods:{
        enterHandle: function(event){
             $(event.currentTarget).addClass("red");
             $(event.currentTarget).hide();
             $(event.currentTarget).fadeIn();
        },
        outHandle: function(event){
             $(event.currentTarget).removeClass("red");
        }
    }
}
</script>

<style scoped>

    .project{
    display:flex;
    /*height:800px;*/
    padding: 10% 0;
    width:100%;
}

    .red{
        background-color: red;
    }

.image{
    display:flex;
    justify-content: center;
    align-items: center;
    width:50%;
    height:100%;
}

    .image img{
        width:50%;
        border: 1px solid white;
    }

#project3-img{
    width:80%;
}

.description{
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width:50%;
    height:100%;
}

    .description span{
        font-weight: bold;
        font-size:45px;
        margin-bottom:10%;
    }

    .description ul li{
        display:flex;
        align-items: center;
        width:70%;
        margin:0 auto;
        line-height: 60px;
        font-size:30px;
    }

    .description ul li img{
        width:10%;
        margin-right:10px;
    }

    .description ul li:hover{
        text-shadow: 1px 2px 4px #ffc400;
    }

    .project1-ul{
        width:500px;
        position: relative;
    }
    
    #project2-img{
        width:80%;
    }
    
    #secondProject-ul{
        width:100%;
    }

    .link{
        box-shadow: 0px 0px 10px 1px rgb(255, 255, 255);
        margin-top:70px;
        font-size:25px;
        background: white;
        border: 2px solid rgb(124, 124, 124);
        border-radius: 15px;
        padding:10px;
        font-weight: bold;
        box-sizing: border-box;
        color:black;
        text-decoration: unset;
    }
    .red{
        background:rgb(241, 180, 87);
    }

    @media only screen and (max-width: 870px){
        .info span{
            font-size:20px;
        }

        #topLeft{
            display:none;
        }

        #topRight{
            position: initial;
            width:100%;
        }

        .project{
            flex-direction: column;
        }

        .image{
            width:100%;
        }

        .description{
            width:100%;
            margin-top:8%;
        }

        .description span{
            text-align: center;
        }

        .description ul li{
            line-height: 30px;
            margin-top: 5%;
        }

        #project2-img{
            margin: 5% auto;
        }

        #project2-img img{
            width:100%;
        }
    }
</style>