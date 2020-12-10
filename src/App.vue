<template>
  <div id="app">
    <app-header @selectChoice="updateParent"></app-header>
    <app-content v-if="isChoice === 'SUN'"  ></app-content>
    <app-vote v-else-if="isChoice === 'Vote' && currentCompA === 0" v-on:selectClose="getComp "></app-vote>
    <sun-team v-else-if="isChoice === 'Vote' && currentCompA === 1"></sun-team>
    <app-FAQs v-else-if="isChoice === 'FAQs'"></app-FAQs>
     
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Content from "./components/Content.vue";
import Vote from "./components/Vote.vue";
import FAQs from "./components/FAQs.vue";
import SunTeam from "./components/SunTeam.vue";
/*import Stake from './components/Stake.vue';*/
 
export default {
  data: function () {
    return {
      isChoice: 'SUN',
      currentCompA: 0,  
    }
  },
    components: {
        appHeader: Header,
        appFooter: Footer,
        appContent: Content,
        appVote: Vote,
        appFAQs: FAQs,
        SunTeam,
        /*Stake*/
    },
    methods: {
      updateParent(value) {
        this.isChoice = value;
      },
      getComp(data) {
        this.currentCompA = data;   
      },
         
    }
}
</script>

<style>
    *{
            margin: 0;
            padding: 0;
        }
        body{
            background-color: rgb(221, 221, 221);
        }
        .sun-header-background-img{
            width: 100%;
            z-index: -1;
            position:absolute;
            height: 400px;
            background-size: cover;
            background-image: url('../src/assets/nen-sun.png');
        }
        .sun-header-content{
            display: flex;
        }
        .sun-header-img{
            width: 42.5%;
        }
        .sun-header-img img{
            width: 20%;
            margin:30px 0px 0px 50px;
        }
        .sun-header-menu{
            width: 40.5%;
        }
        .sun-header-MENU{
            list-style: none;
            display: flex;
        }
        .sun-header-MENU li{
            display: inline-block;
            margin-top: 45px;
            color: white;
            margin-right: 25px;
            padding: 5px 15px;
            cursor: pointer;
        }
        .sun-header-connect-wallet{
            border: 0px solid blueviolet;
            border-radius: 7.5px;
            padding: 5px 15px;
            margin-right: 50px;
            background-color: blueviolet;
            display: inline-flex;
        }
        .sun-header-connect-wallet a{
            text-decoration: none;
            color: white;
        }
        .sun-header-connect-translate{
            display: inline-flex;
            display: inline-block;
        }
        .sun-header-connect-translate-select{
            border: 0px solid blueviolet;
            border-radius: 7.5px;
            padding: 5px 15px;
        }
        .chinh{
            border: 0px solid blueviolet;
            border-radius: 7.5px;
            padding: 5px 15px;
            background-color: blueviolet;
        }
        .sun-header-MENU-hover:hover{
            border: 0px solid blueviolet;
            border-radius: 7.5px;
             
            background-color: blueviolet;
        }
        .sun-header-connect{
            width: 17%;
            color: white;
            display:flex;
            margin-left:2%;
        }
        .sun-header-connect div{
            margin-top: 0px;
        }
        .sun-header-connect{
            margin-top:2%;
        }
        .sun-body-content h1, h2, h3, h3 a{
            text-align: center;
            color: white;
        }
        .sun-body-content h1{
            font-size: 50px;
            margin-top: 45px;
        }
        .sun-body-content h2{
            font-size: 18px;
            margin-top: 20px;
        }
        .sun-body-content h3{
            font-size: 12px;
            margin-top: 10px;
            margin-bottom: 10px;
        }
        .sun-body-content-warning{
            color: tomato;
            margin: auto;
            text-align: center;
            border:1px solid rgb(240, 135, 117);
            padding: 10px;
            background-color: rgb(235, 223, 196);
            max-width: 900px;
        }
        .sun-body-content-box{
            border: white solid 1px;
            background-color: white;
            border-radius: 10px;
            padding: 26px 30px 16px;
            width: 50%;
            margin: auto;
            display: flex;
            margin-top: 10px;
            margin-bottom: 70px;
        }
        .sun-body-content-box1{
            width: 80%;
        }
        .sun-body-content-box1-1{
            width: 40%;
            display: flex;
        }
        .sun-body-content-box1-2{
            width: 60%;
            margin-top: 15px;
            letter-spacing: 0;
        }
        .sun-body-content-box1-2-p1{
            font-size: 20px;
        }
        .sun-body-content-box1-2-p2{
            font-family:pingFangSC-Regular;
            font-size: 12px;
            color:#999;letter-spacing: 0;
        }
        .sun-body-content-box1-1{
            opacity: 0.8;
            font-family:  PingFangSC-Regular;
            font-size: 14px;
            color:#666;
            letter-spacing: 0;
            padding-left: 3px;
            background-size: 20px 20px;
        }
        .title{
            font-family: PingFangSC-Regular;
            font-size: 14px;
            padding-left:10px;
        }
        .MR{
            font-size:12px;
            margin-left: 8px;
            transform-origin: left;
            
        }
        .sun-body-content-box2{
            position: relative;
            width:50%;

        }
        .sun-body-content-box2 a{
            text-decoration: none;
            color: white;
            font-size: 12px;
            display: block;
            
        }
        .sun-body-BODY-head{
            text-align: center;
            font-size: 20px;
        }
        .sun-body-BODY-head span a{
            text-decoration: none;
            color: gray;

        }
        
        .center__item-body-amount-TRX{
            margin-top:15px;
            font-family: PingFangSC-Regular;
            font-size: 20px;
        }
        .i {
            color:#999;
        }
        .trx{
            font-size:12px;
        }
        .getLP{
                font-family:pingFangSC-Regular;
                font-size: 12px;
                color:#fff;letter-spacing: 0;
                text-align:center;
                padding:10px 14px;
                background:#5915e1;
                border-radius:5px;
                display: inline-table;
                text-decoration: none;
                margin:40px 10px;
        }
        .pool-container{
            width:100%;
            margin:60px 0px 0px;
            width:1189px; 
            height: 1350px;
            margin-left:310px;
        }
        
        .sun-body-content h1{
                color:#fff;
                font-weight: 400;

            }
        .sun-body-content h2{
                font-family: HelveticaNeue-Bold;
                font-size:18px;
                letter-spacing: 0;
                margin-bottom:10px;
            }
            .sun-body-content h3{
                color:#fff;
                font-size:12px;
            }
            .sun__item{
                position: relative;
                width: 330px;
                height: 360px;
                border: 1px solid #ccc;
                border-radius: 10px;
                padding: 20px;
                background-color: white;
                margin-left:30px;
                overflow:hidden;
            }
            .sun__item-header{
                display: flex;
                align-items: center;
                justify-content: center;
            }
            .sun__item-header-img{
                position: relative;
                width: 30%;
            }
            .sun, .toke{
                width: 50px;
                height: 50px;
            }
            .toke{
                position: absolute;
                top: 0px;
                right: 0;
                left: 40px;
            }
            .sun__item-header-text{
                width: 70%;
            }
            .sun__item-header-text-1{
                font-size: 25px;
            }
            .sun__item-header-text-2{
                font-size: 12px;
                color:#666;
            }
            .sun__item-body{
                margin: 30px 0px;
            }
            .sun__item-body-conten-left{
                font-size: 12px;
                color:#666;
            }
            .sun__item-body-conten-right{
                font-size: 13px;
                color: #1ba27a;
            }
            .sun__item-body-conten,.sun__item-body-table-test{
                display: flex;
                align-items: center;
                justify-content: space-between;
            }
            .sun__item-body-table{
                margin-top: 20px;
                border-radius: 10px;
                padding: 20px;
                box-shadow: inset 0 -2px 8px 0 rgba(51,1,138,.08);
                background-color: #fff;
            }
            .hihi{
                font-size: 10px;
                color:#666;
            }
            .sun__item-footer{
                margin-top: 50px;
            }
            .sun__item-footer-link, .sun__item-footer-button{
                text-align: center;
                display: block;
            }
            .type-link{
                color: #6726eb;
                font-size: 12px;
                line-height: 20px;
                margin-top: 25px;
                text-decoration: none;
                
            }
            .buton-click{
                width: 100%;
                padding: 10px;
                border: none;
                outline: none;
                border-radius: 10px;
                margin-top: 13px;
                background: #b79cef;
                color: white;
            }
            .buton-click{
            
                transform:translateY(4px);
            }
            .x{
                color:#5915e1;

            }
            .body-1{
                display:flex;
                margin: 30px 20px;
            
            }
            .body-2{
                display:flex;
                margin: 30px 20px;
            }
            .body-3{
                display:flex;
                margin: 30px 20px;
            }
            .sun-footer{
            width:1422px;
            height: 52;
            width:100%;
            margin:0px 0px 80px;
            padding-bottom: 30px;
            text-align: center;
             
            }
            a:link, a:visited{ 
                color:#999;
                text-decoration:none;
            }
            .sun-footer a{
                margin:0 30px;
                font-size:12px;
                font-family:AvenirNext-Medium;
            }
            .over{
                transform: rotate(-315deg);
                transform-origin: right top;
                font-family: AvenirNext-Bold;
                font-size: 14px;
                color: #fff;
                background: #999;
                position: absolute;
                right: -25px;
                top: 80px;
                height: 33px;
                line-height: 33px;
                width: 150px;
                text-align: center;
            }
            .pass-2{
                margin-left: 315px;
            }
            .sun__item-body-time{
                margin-left:100px;
                color:red;
            }
            .sun__item-footer-link{
                font-variant:tabular-nums;
                list-style:none;
                font-feature-settings: "tnum","tnum";
            }
            .data-show{
                background:#fffbe6;
                margin: 20px 499px 0px 499px;
                padding: 8px 30px 8px 15px;
                transition: width 2s;
                display:block;
            }
            .sun-body-messger{
                color:rgb(236, 91, 91);
                text-align: center;
                font-size:14px;
                font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji"
            }     
            .remove{
                appearance: button;
                -webkit-writing-mode: horizontal-tb !important;
                text-rendering: auto;
                color: -internal-light-dark(black, white);
                letter-spacing: normal;
                word-spacing: normal;
                text-transform: none;
                text-indent: 0px;
                text-shadow: none;
                display: inline-block;
                text-align: center;
                align-items: flex-start;
                cursor: default;
                background-color: -internal-light-dark(rgb(239, 239, 239), rgb(59, 59, 59));
                box-sizing: border-box;
                margin: 0em;
                font: 400 13.3333px Arial;
                padding: 1px 6px;
                border-width: 2px;
                border-style: outset;
                border-color: -internal-light-dark(rgb(118, 118, 118), rgb(133, 133, 133));
                border-image: initial;
                 

            }
            .dropbtn {
            background-color: #4CAF50;
            color: white;
            padding: 16px;
            font-size: 16px;
            border: none;
            cursor: pointer;
            }

            /* The container <div> - needed to position the dropdown content */
            .dropdown {
            position: relative;
            display: inline-block;
            }

            /* Dropdown Content (Hidden by Default) */
            .dropdown-content {
            display: none;
            position: absolute;
            background-color: #f9f9f9;
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            }

            /* Links inside the dropdown */
            .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            }

            /* Change color of dropdown links on hover */
            .dropdown-content a:hover {background-color: #f1f1f1}

            /* Show the dropdown menu on hover */
            .dropdown:hover .dropdown-content {
            display: block;
            }

            /* Change the background color of the dropdown button when the dropdown content is shown */
            .dropdown:hover .dropbtn {
            background-color: #3e8e41;
            }
             
</style>
