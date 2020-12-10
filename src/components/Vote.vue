<template>
    <div  >
    <div class="sun-body">
            <div class="vote__list">
                <h2 class="title-2">Vote</h2>
                <div class="vote__list-header">
                    <div class="text">
                    <div class="vote__list-header-1">
                        <a @click.prevent="isEnded = !isEnded" :class="{lol: isEnded }" href="" >Active</a>
                    </div>
                    <div class="vote__list-header-2">
                        <a @click.prevent="isEnded = !isEnded" :class="{lol: !isEnded }" href="">Closed</a>
                    </div>
                    </div>
                </div>
                <div v-if="isEnded">
                <div class="vote__list-body" style="padding-top:10%; padding-bottom:10%;">
                    <div class="vote__list-body-1"> 
                        <img src="src/assets/vote-logo.png" alt style="width:18%; max-width:200px; min-width:100px;">
                    </div>
                    <div class="vote__list-body-2">
                        <p>No proposal up for vote. Please check other voting instead.</p>
                    </div>
                </div>
                </div>
                <div v-else>
                    <div class="vote_list-body-close" style="padding-top:5%; padding-bottom:5%;">
                        <a href="#" @click="changeCompNow(1)">
                        <div class="vote_list-body-close-1">
                            <div class="l1-close">
                                <span class="l1-close-1">Vote for Your Favorite Pool</span> 
                                <span class="l1-close-2-1">Ends at:Oct 18 2020 03:00:00 </span>
                            </div>
                            <div class="l2-close">
                                <div class="l2-close-1">Closed</div>
                                <div class="l2-close-2">
                                    <span >Author:  
                                        <span class="c3">SUN Team</span>
                                    </span>
                                    <span  >Total pool supply:  
                                        <span class="c3"> 1,200 SUN</span>
                                    </span>
                                </div>
                            </div>
                        </div>
                        </a>
                        <a href="#"  @click="changeCompNow(2)">
                            <div class="vote_list-body-close-1">
                                <div class="l1-close">
                                    <span class="l1-close-1">Vote the featured token onto JustSwap’s token list</span> 
                                    <span class="l1-close-2-1">Nov 07 2020 20:00:00 </span>
                                </div>
                                <div class="l2-close">
                                    <div class="l2-close-1">Closed</div>
                                    <div class="l2-close-2">
                                        <span >Author:  
                                            <span class="c3">SUN Team</span>
                                        </span>
                                         
                                    </div>
                                </div>
                            </div>
                            </a>
                    </div>       
                </div>     
            </div>
        </div>
    </div>    
</template>

<script>

export default {
    data: function() {
        return {
            isEnded: true,
        }
    },
    methods: {
        changeCompNow(value) {
            this.$emit('selectClose', value);
        }
    }
}
</script>

<style>
    .title-2{
                margin-left: -55%;
                color:#ffffff;
                font-size:19.2px;
                font-family: PingFangSC-Medium;
                margin-top:50px;
            }
    .vote__list-header{
                width: 1189px;
                height: 639px;
                border: 1px solid #ccc;
                border-radius: 10px;
                padding: 20px;
                background:#ffffff;
                margin:10px 0px 0px;
                padding:20px;
                margin-left: 400px;
                align-items: center;
                justify-content: center;
            }
            .text{
                 display: flex;
                 border-bottom-style: solid;
                 border-bottom-width: thin;
                 border-bottom-color:#ccc;
                 margin:20px 20px;
            }
            .vote__list-header-1{
                 margin-right: 5%;
                 
            }
            .vote__list-body-1 img{
                 margin-left:490px;
            }
            .vote__list-body, .vote_list-body-close{
                margin-top:-650px;
                margin-left: 25%;
            }
            .vote__list-body,.vote_list-body-close{
                 display:center;
                 width:1149px;
                 height: 225px;
            }
            .vote__list-body-2{
                margin-left:390px;
            }
            .sun-footer{
                width:1422px;
                height: 52;
                width:100%;
                margin:0px 0px 80px;
                padding-bottom: 30px;
                text-align: center;
                margin-top:20%;
                }
                a:link, a:visited{ 
                    color:#999;
                    text-decoration:none;
                }  
                .sun-footer a{
                    margin:0 40px;
                    font-size:12px;
                    font-family:AvenirNext-Medium;
                } 
            .vote_list-body-close-1{
                padding:30px 20px;
                width: 1149px;
                height: 139px;
                background: #ffffff;
                box-shadow: 0 20px 40px 0 hsla(0,0%,58%,.06);
                border-radius: 10px;
                margin-left:-3%;
                margin-top:1%;
                
            }  
            .l1-close{
                color:#333333;
                font-size:19.2px;
                font-family: PingFangSC-Medium;

            } 
            .l2-close-2{
                font-size: 11.15px;
                font-family: PingFangSC-Regular;
                padding: 5px 19px;

            }      
            .vote_list-body-close{
                color:rgba(0,0,0,.65);
                font-size:14px;
                font-variant:tabular-nums;
                line-height:1.5715;
                list-style:none;
                font-feature-settings:"num","num";
                width:1149px;
                height:139px;
                margin-left:23%;
                padding:30px 20px;

            }
            .l1-close-2-1{
                width:20%;
                color:#999999;
                font-size:10px;
                
            }
            .l1-close{
                display: flex;
                align-items: center;
                justify-content: space-between;

            }
            .l1-close-1{
                color:#333333;
                font-size:19.2px;
                font-family:PingFangSC-Medium;
            }
            .l1-close-2-2{
                font-size: 10px;
            }
            .l2-close-1{
                color:#999999;
                font-size:16px;
                font-family: PingFangSC-Regular;
                border-radius: 7.5px;
                padding: 5px 19px;
                background-color:#99999933;
                margin:20px 20px
            }  
            .l2-close{
                display: flex;
                align-items: center;
                justify-content: space-between;
            }
            .c3{
                color:#333333;
            } 
            .text-success{
                color:rgb(42, 42, 192);
            }
            .lol{
                color:#5915e1!important;
                border-bottom:1px solid blue;
            }
</style>
