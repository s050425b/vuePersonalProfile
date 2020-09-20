
<template>
    <div id="heading">
        <div id="top">
            <div id="topRight">
                <div id="top-title">
                    <h2>Welcome to my skill demonstration!</h2>
                    <h2>Hope you have fun here</h2>
                </div>
                <div id="top-self">
                    <span>{{fullName}}</span><br>
                    <span>{{nickName}}</span>
                </div>
                <div id="top-info">
                    <h2>You can view my information here below!</h2>
                    <div id="top-info-link">
                        <a href="../assets/resource/doc/CV_LauChungYuen.docx" download="">CV</a>
                        <a href="../assets/resource/doc/CoverLetter_LauChungYuen.docx" download="">Cover Letter</a>
                    </div>
                </div>
                <div id="top-know" v-on:click="clickHandle" >
                    <img src="" alt="">
                    <span>Click to know more about me</span>
                </div>
            </div>
            <div id="topLeft"><img src="../assets/resource/photo/2015m.jpg" alt=""></div>
        </div>
        <div id="more-info">
            <div id="flex">
                <div class="info-container">
                    <div class="info">
                        <span>Phone: {{phoneNum}}</span>
                        <span>Education: BBA (Information System)</span>
                        <span>Email: {{email}}</span>
                    </div>
                </div>
                <div class="info-container">
                    <div class="info">
                        <span>Age: {{age}}</span>
                        <span>Hobby: Football, badminton, dance</span>
                        <span>Favourte food: Sushi</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
import $ from 'jquery';

export default { 
    name: "First",
    data () {
        return{
            fullName: "Lau Chung Yuen",
            nickName: "Jason",
            age: 21,
            phoneNum: "+852 6181 7555",
            email: "jasonlauxd@gmail.com"
        }
    },
    methods: {
        clickHandle: function(){
            
            console.log(document.getElementById("more-info").style.display);
            if (document.getElementById("more-info").style.display==="none" || document.getElementById("more-info").style.display==="" ){
                $("#more-info").slideDown();
            } else {
                $("#more-info").slideUp();
            }
        }
    }
}
</script>

<style scoped>
    #top{
    display:flex;
    background-image: url("../assets/resource/photo/Colorful-Powerpoint-Background.jpg");
    background-position: center;
    background-size: cover;
}

#topRight{
    position: relative;
    left:3%;
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width:50%;
    height: 800px;
}
    #topRight #top-title{

        text-align:center;
        font-size: 50px;
        font-weight: bold;
        line-height: 80px;
    }

    #topRight #top-self{
        margin-top: 40px;
        font-size: 30px;
        text-align: center;
    }

    #topRight #top-info{
        margin-top:50px;
        line-height: 70px;
        
    }

        #topRight #top-info h2{
            text-align:center;
            font-weight: bold;
            font-size:30px;
        }
        #topRight #top-info #top-info-link{
            display: flex;
            justify-content: space-between;
            width: 350px;
            margin: 10px auto;
        }

            #topRight #top-info #top-info-link a{
                display:flex;
                justify-content: center;
                align-items: center;
                width:150px;
                height:50px;
                color:black;
                text-decoration: unset;
                border:1px solid black;
            }

            #topRight #top-info #top-info-link a:hover{
                cursor: pointer;
                background-color: rgb(233, 198, 3);
            }


            #top #topRight #top-know{
                position: absolute;
                top: 90%;
                bottom: 0px;
                display:flex;
                align-items: center;
                cursor: pointer;
            }

            #top #topRight  #top-know img{
                width:30px;
                margin-right:10px;
                transform: rotate(90deg);
            }
            
            #top #topRight #top-know .rotate{
                transition: 0.1s;
                 transform: rotate(180deg);
            }



     #topLeft{
         display:flex;
         align-items: center;
         width: 15%;
         margin:0 auto;
        
     }
            
    #topLeft img{
        width:100%;
        border: 2px solid grey;
    }
            
            
    #more-info{
        display:none;
        width:100%;
        padding:50px;
        background-color: rgb(241, 241, 241);
    }
            
    #flex{
        display:flex;
        height:100%;
    }

    #more-info .info{
        height:200px;
        font-size: 25px;
        display:flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: flex-start;
        text-align: center;
    }

    #more-info .info-container{
        display:flex;
        height:100%;
        justify-content: center;
        align-items: center;
        width:50%;
    }

      @media only screen and (max-width: 870px){
        #top-title h2{
            font-size:40px;
        }

        #flex{
            flex-direction: column;
        }

        #top #topRight #top-know{
            position: initial;
        }

        #topRight #top-info h2{
            font-size: 20px;
        }



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
      }
</style>

