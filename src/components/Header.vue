<template>
    <div>
        <div class="sun-header-background-img"></div>
        <div class="sun-header">
                <div class="sun-header-content">
                    <div class="sun-header-img">
                        <img src="src/assets/Sun-logo.png">
                    </div>
                    <div class="sun-header-menu">
                        <ul class="sun-header-MENU">
                            <li class="sun-header-MENU-hover" @click="changeSelect('SUN')" :class="{chinh:changeSelect1}">SUN</li>
                            <li class="sun-header-MENU-hover" @click="changeSelect('Vote')" :class="{chinh:changeSelect2}">Vote</li>
                            <li class="sun-header-MENU-hover" @click="changeSelect('FAQs')" :class="{chinh:changeSelect3}">FAQs</li>
                            <div class="dropdown">
                                <li><a href="#" class="sun-header-MENU-dropdown">Learn</a></li>
                                <div class="dropdown-content">
                                    <a href="#">WhitePaper</a>
                                    <a href="#">Audit</a>
                                </div> 
                            </div>  
                        </ul>
                    </div>
                    <div class="sun-header-connect">
                        <div @click="openWallet">
                        <div v-if="adress">
                        <div class="sun-header-unconnect-wallet">
                            <div class="address-text">
                            <img src="src/assets/tronlink.svg" alt="">
                            <span>{{adress}}</span>
                            </div>
                        </div>
                        </div>
                        <div v-else>
                        <div class="sun-header-connect-wallet">
                            <a href="#">Connect to Wallet</a>
                        </div>
                        </div>
                        </div>
                        <div class="sun-header-connect-translate">
                            <select class="sun-header-connect-translate-select">
                                <option>English</option>
                                <option>简体中文</option>
                            </select>
                        </div>
                    </div>
                </div>
        </div>
        <div class="close">
        <div v-if="check">
        <div class="mask">
            <div class="modal">
            <div v-if="adress" class="connect__to-wallet-to">
                <div class="connect__to-wallet-to-title">
                    <span class="connect__to-wallet-to-title-1">Connect to Wallet</span>
                    <span @click.prevent="check=!check" class="connect__to-wallet-t-title-2">
                        <button class="remove">x</button>
                    </span>
                </div>
                 
                <div class="connect__to-wallet-to-body">
                    <div class="connect__to-wallet-to-body-item-1">
                        <div class="item-text">Connected with Tronlink</div>
                        <div class="adress-text">
                            <span>{{adress}}</span>
                            <span>Copy</span>
                        </div>
                    </div>
                    <div class="connect__to-wallet-to-body-img">
                        <img src="src/assets/lol.png" alt="">
                        <div class="balance">0</div>
                        <p style="margin-left: 4%;">SUN Balance</p>
                    </div>
                </div>
            </div >
            <div v-else class="connect__to-wallet-to">
                <div class="connect__to-wallet-to-title">
                    <span class="connect__to-wallet-to-title-1">Connect to Wallet</span>
                    <span @click.prevent="check=!check" class="connect__to-wallet-t-title-2">
                        <button class="remove">x</button>
                    </span>
                </div>
                 
                <div class="connect__to-wallet-to-body">
                    <div class="connect__to-wallet-to-body-img">
                        <img src="src/assets/lol.png" alt="">
                    </div>
                    <div class="connect__to-wallet-to-body-item-2">
                        <span>
                            <img src="src/assets/tronlink.svg" alt="">
                        </span>
                        <span class="text-tronlink">
                            <span>TronLink Wallet</span>
                        </span>
                    </div>
                    <div class="connect__to-wallet-to-body-link">
                        <span>Haven't installed TronLink yet?</span>
                        <a href="">click here>></a>
                    </div>
                </div>
            </div>
            </div>
        </div>
    </div>
    </div>
    </div>
</template>

<script>

export default {
      data: function(){
          return{
              changeSelect1:true ,
                changeSelect2:false ,
                changeSelect3:false,
                adress:'',
                isEnded:true,
                check:true,
                
          }
      },
 
    methods: {
        changeSelect(item) {
            this.$emit('selectChoice', item);
            if(item == 'SUN') {
                this.changeSelect1=true 
                this.changeSelect2=false 
                this.changeSelect3=false
            } 
            else if(item == 'Vote') {
                this.changeSelect1=false 
                this.changeSelect2=true 
                this.changeSelect3=false
            } 
            else {
                this.changeSelect1=false 
                this.changeSelect2=false 
                this.changeSelect3=true
            } 
        },
       gettronweb: function(){
            if(window.tronWeb && window.tronWeb.defaultAddress.base58){
             this.adress=window.tronWeb.defaultAddress.base58
             
            }
        },
        openWallet: function(){
            var close = document.querySelector('.close')
            close.classList.add('open')
            this.check = true
        }
    },
    created() {
        this.interval = setInterval(() => this.gettronweb(), 1000);
    }
}
</script>

<style>
    .sun-header-unconnect-wallet{
        font-size:14px;
        display:flex;
        align-items:center;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
        max-width: 133px;
        margin-left:-6%;
    }
    .address-text{
        display:flex;
        margin-right: 20px;
        background:#fff;
        border-radius: 5px;
        padding: 0 7px;
        font-family: HelveticaNeue;
        font-size:14px;
        color:#333;
        height: 30px;
        line-height: 30px;
    }

    .mask{
            position: fixed;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            z-index: 1000;
            height: 100%;
            background-color: rgba(0,0,0,.45);
            
        }
        .modal{
            box-sizing: border-box;
            color: rgba(0,0,0,.65);
            font-size: 14px;
            font-variant: tabular-nums;
            line-height: 1.5715;
            list-style: none;
            font-feature-settings: "tnum","tnum";
            position: relative;
            margin: 150px auto;
            padding: 0 0 24px;
            pointer-events: none;
            margin-left:35%;
        }
        .connect__to-wallet-to{
            width: 530px;
            height: 425px;
            border: 1px solid #ccc;
            border-radius: 48px;
            padding: 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background:#ffff;
            pointer-events: auto;
        }
        .connect__to-wallet-to-title{
            width:507px;
            height:35px;
            display:flex;
            font-family:PingFangSC-semibold;
            font-size:20px;
            color:#333;
            line-height:28px;
            text-align:left;
            margin-top:-72%;
            border-bottom: 1px solid #f0f0f0;
            padding:20px
        }
         
        .connect__to-wallet-to-title-1{
            width:492px;
            height:28px;
        }
        .connect__to-wallet-t-title-2 img{
            width:46px;
            height:46px;
            margin-left:-15%;
            margin-top:-15%;
        }
        .connect__to-wallet-to-body{
            padding:24px;
            width:467px;
            height:300px;
            margin-left:-109%;
            margin-top:20%;
        }
        .item-img{
            width:290px;
            height:82px;
        }
        .item-img{
            margin-top:10%
        }
        .connect__to-wallet-to-body-img{
             margin-left:37%;
            margin-top:3%; 
        }
        .connect__to-wallet-to-body-item-1{
            width: 450px;
            height: 44px;
            box-shadow: 0 10px 40px 0 rgba(21,55,156,.06);
            border-radius: 10px;
            padding: 20px;
            align-items: center;
            justify-content: space-between;
            margin-left:-2%;
            background:hsla(0,0%,66.7%,.2);
        }
        .connect__to-wallet-to-body-item-2{
            width: 450px;
            height: 44px;
            box-shadow: 0 10px 40px 0 rgba(21,55,156,.06);
            border-radius: 10px;
            padding: 20px;
            align-items: center;
            justify-content: space-between;
            margin-left:-2%;
            display:flex;
        }
        .item-text-1{
            width:132px;
            height:31px;
            color:#333333;
            font-size:20px;
            font-family: AvenirNext-Medium;
        }
        .connect__to-wallet-to-body-link{
            margin-top:21%;
            margin-left:-10%;
        }
        .connect__to-wallet-to-body-link span{
            width:180px;
            height:15px;
            color:#999999;
            font-size:14px;
            font-family: AvenirNext-Medium;
        }
        .adress-text{
            display:flex;
            justify-content: space-between;
            align-items: center;
        }
        .balance{
            margin-top:3%;
            margin-left:15%;
        }
        .text-tronlink{
            margin-left:50%;
             font-size:20px;
             font-family:AvenirNext-medium;
        } 
        .close{
            display:none;
        }
        .close.open{
            display: block;
        }
</style>
