 <template>
      <div v-if="check">
        <div class="mask">
        <div class="modal">
        <div class="connect__to-wallet">
            <div class="connect__to-wallet-title">
                <span @click.prevent="isEnded = !isEnded" :class="{lol: isEnded }" class="connect__to-wallet-title-1">Stake</span>
                <span @click.prevent="isEnded = !isEnded" :class="{lol: !isEnded }" class="connect__to-wallet-title-1">Claim</span>
                <span @click.prevent="check=!check" class="connect__to-wallet-title-2">
                    <button class="remove">x</button>
                </span>
            </div>
             
            <div class="connect__to-wallet-body">
                <p>Enter the amount of TRX you want to stake</p>
                <div class="connect__to-wallet-body-item-1">
                    <div class="item">
                        <input type="text" id="amountStake">
             
                    </div>
                    <div class="item-text-1">
                        <span>SUN</span>
                    </div>
                </div>
                <div class="connect__to-wallet-body-link">
                    <p>TRX Blance:</p>
                    <button class="buton-click" @click="triggerSmartContract1">stake</button>
                </div>
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
            isEnded:true,
            check:true,
        }
    },
    methods: {
            async triggerSmartContract1(){
                    const trc20ContractAddress = "TEfPRoBKPj6zUXNKofQ9asrJoNk8gP9Rd3";//contract address
                    var address = "TWQ1xAk6EQh2hV1dDZV6e6S31yBfeMiP1A";//msg
                    var amountStake = parseInt(document.getElementById('amountStake').value);
                    try {
                        let contract = await tronWeb.contract().at(trc20ContractAddress);
                        //Use call to execute a pure or view smart contract method.
                        // These methods do not modify the blockchain, do not cost anything to execute and are also not broadcasted to the network.
                        let result = await contract.stake(
                            amountStake
                        ).send({
                            feeLimit: 5000000
                        }).then(output => {console.log('- Output:', output, '\n');});
                    } catch(error) {
                        console.error("trigger smart contract error",error)
                    }
                    
                }
            
            }
    
     }
</script>

<style>
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
        .connect__to-wallet{
            pointer-events: auto;
            width: 372px;
            height: 349px;
            border: 1px solid #ccc;
            border-radius: 48px;
            padding: 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background:#fff;
        }
        .connect__to-wallet-title{
            width:338px;
            height:16px;
            display:flex;
            font-family:PingFangSC-semibold;
            font-size:20px;
            color:#333;
            line-height:28px;
            text-align:left;
            margin-top:-88%;
            border-bottom: 1px solid #f0f0f0;
            padding:20px
        }
         
        .connect__to-wallet-title-1{
            width:492px;
            height:28px;
        }
        .connect__to-wallet-title-2 img{
            width:46px;
            height:46px;
            margin-left:-15%;
            margin-top:-15%;
        }
        .connect__to-wallet-body{
            padding:24px;
            width:300px;
            height:300px;
            margin-left:-105%;
            margin-top:55%;
        }
        .item{
            width:492px;
            height:90px;
            margin-top:23%
        }
        .connect__to-wallet-body-item-1{
            display:flex;
            width: 285px;
            height: 44px;
            box-shadow: 0 10px 40px 0 rgba(21,55,156,.06);
            border-radius: 10px;
            padding: 20px;
            align-items: center;
            justify-content: space-between;
            margin-left:-4%;
        }
        .item-text-1{
            width:132px;
            height:31px;
            color:#333333;
            font-size:20px;
            font-family: AvenirNext-Medium;
        }
        
        
        .connect__to-wallet-body-link{
            margin-top:-1%;
            margin-left:-10%;
        }
        .connect__to-wallet-body-link span{
            width:180px;
            height:15px;
            color:#999999;
            font-size:14px;
            font-family: AvenirNext-Medium;
        }
         
        .mystake{
            display:flex;
        }
        .buton-click {
            width: 100%;
            padding: 10px;
            border: none;
            outline: none;
            border-radius: 10px;
            margin-top: 13px;
            background: #b79cef;
            color: white;
        }
        .connect__to-waller-footer{
            text-align: center;
            display: block;
        }
        .lol{
                color:#5915e1!important;
                border-bottom:3px solid blue;
            }
</style>
