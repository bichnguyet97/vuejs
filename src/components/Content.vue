<template>
    <div class="sun-body">
            <div class="sun-body-content">
                <h1>Today's a good day to sow SUN</h1>
                <h2>Stake to mine and earn SUN</h2>
                <h3>SUN smart contract has been verified by SlowMist. Check out the audit report <a href="https://sun.io/docs/audit-report-sun_en.pdf">here</a>.</h3>
                <!-- <div class="sun-body-content-warning">Currently we only support staking through this page. Assets that are staked via other means will not be included in Official mining and cannot be returned.</div> -->
                <div v-if="check" class="data-show">
                    <span  class="sun-body-messger">
                        Currently we only support staking through this page. Assets that are staked via other means will not be included in Official mining and cannot be returned.
                    </span>
                    <button @click.prevent="check=!check" class="remove">x</button>
                </div>
                <div class="sun-body-content-box">
                    <div class="sun-body-content-box1">
                        <div class="sun-body-content-box1-1">
                            <img src="src/assets/1.svg">
                            <span class="title">Total Staked Value</span>
                            <span><a href="https://sun.io/#/rules" class="MR">Mining rules</a></span>
                        </div>
                        <div class="sun-body-content-box1-2">
                            <div class="center__item-body-amount-TRX">
                                <span class="i">≈</span>
                                <span class="demo" > 8,075,763,817</span>
                                <span class="trx">TRX</span>
                            </div><br>
                            <p class="sun-body-content-box1-2-p2">≈ 199,013,590 USD</p>
                               
                        </div>
                    </div>
                    <div class="sun-body-content-box2">
                        <a style="color: #fff" class="getLP" href="https://justswap.io/?lang=en-US#/home?tokenAddress&type=add" target="_bank">Get LP Token on JustSway</a>
                    </div>
                </div>
            </div>
            <div class="sun-body-BODY">
                <div class="sun-body-BODY-head">
                    <span>
                        <a @click.prevent="isEnded = !isEnded" :class="{color: isEnded}" href="">Active</a>
                    </span>
                    <span>|</span>
                    <span>
                        <a @click.prevent="isEnded = !isEnded" :class="{color: !isEnded}" href="">Ended</a>
                    </span>
                </div>
            </div>
            <div>
                <a href="test.html"></a>
            </div>
            <div v-if="isEnded">
                <div class="pool-container">
                    <div class="body-1">
                    <section>
                    <div class="sun__item">
                        <div class="sun__item-header">
                            <div class="sun__item-header-img">
                                <img src="src/assets/lol.png" alt="" class="sun">
                                <img src="src/assets/token-logo.png " alt="" class="toke"> 
                            </div>
                            <div class="sun__item-header-text">
                                <span class="sun__item-header-text-1"> SUN/TRX LP Pool </span><br>
                                <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                    <span class="x">9x</span>
                                    <span>SUN</span>
                                </span>
                            </div>
                        </div>
                        <div class="sun__item-body">
                            <div class="sun__item-body-conten">
                                <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                <span class="sun__item-body-conten-right">APY: 37.74%</span>
                            </div>
                            <div class="sun__item-body-table">
                                <p class="hihi">Total Staked</p>
                                <div class="sun__item-body-table-test">
                                    <div class=""> 
                                        1,740,200
                                    </div>
                                    <div class="">
                                        SUN
                                    </div>
                                </div>
                                <div class="sun__item-body-table-test">
                                    <div class=""> 
                                        562,315,719
                                    </div>
                                    <div class="">
                                        TRX
                                    </div>
                                </div>
                                <p class="hihi">Pool Supply</p>
                                <div class="sun__item-body-table-test">
                                    <div class=""> 
                                        23,672
                                    </div>
                                    <div class="">
                                        SUN
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="sun__item-footer">
                            <div class="sun__item-footer-link">
                                <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                            </div>
                            <div @click="openStake">
                            <div class="sun__item-footer-button">
                                <button @click="getbalanceTRX(), getBalanceOfToken(),getBalanceOfStake() " class="buton-click">Select</button>
                            </div>
                            </div>
                        </div>
                    </div>
                    </section>
                    <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/t-logo.png" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> USDT/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                        </div>
                                        <div class="">
                                            TRX
                                        </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div @click="openStake">
                                <div class="sun__item-footer-button">
                                    <button @click="getbalanceTRX(), getBalanceOfToken(),getBalanceOfStake() " class="buton-click">Select</button>
                                </div>
                                </div>
                            </div>
                        </div>
                    </section>
                    <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/cc-logo.png" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> JST/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                        </div>
                                        <div class="">
                                            TRX
                                        </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                        </div>
                    </section>
                    </div>
                    <div class="body-2">
                    <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/j-logo.png" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> USDJ/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                        </div>
                                        <div class="">
                                            TRX
                                        </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                        </div>
                    </section>
                    <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/g-logo.png" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> WBTT/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                        </div>
                                        <div class="">
                                            TRX
                                        </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                        </div>
                    </section>
                    <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/smile-logo.png" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> WIN/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                        </div>
                                        <div class="">
                                            TRX
                                        </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                        </div>
                    </section>
                    </div>
                    <div class="body-3">
                        <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/lol.png" alt="" class="sun">
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> TRX Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                            </div>
                                            <div class="">
                                            SUN
                                            </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                            </div>
                                            <div class="">
                                            TRX
                                            </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                            </div>
                                            <div class="">
                                            SUN
                                            </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                            </div>
                        </section>
                        <section>
                        <div class="sun__item">
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/token-logo.png " alt="" class="sun"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> SUN Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">9x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-conten">
                                    <span class="sun__item-body-conten-left">Total:54,463,422,056</span>
                                    <span class="sun__item-body-conten-right">APY: 37.74%</span>
                                </div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            1,740,200
                                            </div>
                                            <div class="">
                                            SUN
                                            </div>
                                    </div>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            562,315,719
                                            </div>
                                            <div class="">
                                            TRX
                                            </div>
                                    </div>
                                    <p class="hihi">Pool Supply</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            23,672
                                            </div>
                                            <div class="">
                                            SUN
                                            </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link" href="https://justswap.io/?lang=en-US?tokenAddress=TKkeiboTkxXKJpbmVFbv4a8ov5rAfRDMf9&type=add#/home" target="liquidity">Get LP Token</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Select</button>
                                </div>
                            </div>
                            </div>
                        </section>
                        </div> 
                </div>
            </div>
            <div v-else>
                <div class="ended">
                    <div class="pass-2"> 
                    <div class="body-1">
                        <section>
                        <div class="sun__item">
                            <div class="over">Ended</div>
                            <div class="sun__item-header">
                                <div class="sun__item-header-img">
                                    <img src="src/assets/L-logo.svg" alt="" class="sun">
                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                </div>
                                <div class="sun__item-header-text">
                                    <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                        <span class="x">4x</span>
                                        <span>SUN</span>
                                    </span>
                                </div>
                            </div>
                            <div class="sun__item-body">
                                <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                <div class="sun__item-body-table">
                                    <p class="hihi">Total Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            22,400
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                    <p class="hihi">My Staked</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            --
                                        </div>
                                        <div class="">
                                            HT/TRX LP
                                        </div>
                                    </div>
                                    <p class="hihi">Pending Claim</p>
                                    <div class="sun__item-body-table-test">
                                        <div class=""> 
                                            --
                                        </div>
                                        <div class="">
                                            SUN
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="sun__item-footer">
                                <div class="sun__item-footer-link">
                                    <a class="type-link gray">Claim & Unstake</a>
                                </div>
                                <div class="sun__item-footer-button">
                                    <button class="buton-click">Continue mining for more profits</button>
                                </div>
                            </div>
                        </div>
                        </section>
                        <section>
                            <div class="sun__item">
                                <div class="over">Ended</div>
                                <div class="sun__item-header">
                                    <div class="sun__item-header-img">
                                        <img src="src/assets/lol.png" alt="" class="sun">
                                        <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                    </div>
                                    <div class="sun__item-header-text">
                                        <span class="sun__item-header-text-1"> SUN/TRX LP Pool </span><br>
                                        <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                            <span class="x">15x</span>
                                            <span>SUN</span>
                                        </span>
                                    </div>
                                </div>
                                <div class="sun__item-body">
                                    <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                    <div class="sun__item-body-table">
                                        <p class="hihi">Total Staked</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                22,400
                                            </div>
                                            <div class="">
                                                SUN
                                            </div>
                                        </div>
                                        <p class="hihi">My Staked</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                --
                                            </div>
                                            <div class="">
                                                HT/TRX LP
                                            </div>
                                        </div>
                                        <p class="hihi">Pending Claim</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                --
                                            </div>
                                            <div class="">
                                                SUN
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="sun__item-footer">
                                    <div class="sun__item-footer">
                                        <div class="sun__item-footer-link">
                                            <a class="type-link gray">Claim & Unstake</a>
                                        </div>
                                        <div class="sun__item-footer-button">
                                            <button class="buton-click">Continue mining for more profits</button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            </section>
                            <section>
                                <div class="sun__item">
                                    <div class="over">Ended</div>
                                    <div class="sun__item-header">
                                        <div class="sun__item-header-img">
                                            <img src="src/assets/t-logo.png" alt="" class="sun">
                                            <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                        </div>
                                        <div class="sun__item-header-text">
                                            <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                            <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                <span class="x">4x</span>
                                                <span>SUN</span>
                                            </span>
                                        </div>
                                    </div>
                                    <div class="sun__item-body">
                                        <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                        <div class="sun__item-body-table">
                                            <p class="hihi">Total Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    22,400
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                            <p class="hihi">My Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    HT/TRX LP
                                                </div>
                                            </div>
                                            <p class="hihi">Pending Claim</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="sun__item-footer">
                                        <div class="sun__item-footer">
                                            <div class="sun__item-footer-link">
                                                <a class="type-link gray">Claim & Unstake</a>
                                            </div>
                                            <div class="sun__item-footer-button">
                                                <button class="buton-click">Continue mining for more profits</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </section>
                        </div>
                    </div>
                    <div class="pass-2"> 
                        <div class="body-2">
                            <section>
                            <div class="sun__item">
                                <div class="over">Ended</div>
                                <div class="sun__item-header">
                                    <div class="sun__item-header-img">
                                        <img src="src/assets/cc-logo.png" alt="" class="sun">
                                        <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                    </div>
                                    <div class="sun__item-header-text">
                                        <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                        <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                            <span class="x">4x</span>
                                            <span>SUN</span>
                                        </span>
                                    </div>
                                </div>
                                <div class="sun__item-body">
                                    <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                    <div class="sun__item-body-table">
                                        <p class="hihi">Total Staked</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                22,400
                                            </div>
                                            <div class="">
                                                SUN
                                            </div>
                                        </div>
                                        <p class="hihi">My Staked</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                --
                                            </div>
                                            <div class="">
                                                HT/TRX LP
                                            </div>
                                        </div>
                                        <p class="hihi">Pending Claim</p>
                                        <div class="sun__item-body-table-test">
                                            <div class=""> 
                                                --
                                            </div>
                                            <div class="">
                                                SUN
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="sun__item-footer">
                                    <div class="sun__item-footer-link">
                                        <a class="type-link gray">Claim & Unstake</a>
                                    </div>
                                    <div class="sun__item-footer-button">
                                        <button class="buton-click">Continue mining for more profits</button>
                                    </div>
                                </div>
                            </div>
                            </section>
                            <section>
                                <div class="sun__item">
                                    <div class="over">Ended</div>
                                    <div class="sun__item-header">
                                        <div class="sun__item-header-img">
                                            <img src="src/assets/j-logo.png" alt="" class="sun">
                                            <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                        </div>
                                        <div class="sun__item-header-text">
                                            <span class="sun__item-header-text-1"> SUN/TRX LP Pool </span><br>
                                            <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                <span class="x">15x</span>
                                                <span>SUN</span>
                                            </span>
                                        </div>
                                    </div>
                                    <div class="sun__item-body">
                                        <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                        <div class="sun__item-body-table">
                                            <p class="hihi">Total Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    22,400
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                            <p class="hihi">My Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    HT/TRX LP
                                                </div>
                                            </div>
                                            <p class="hihi">Pending Claim</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="sun__item-footer">
                                        <div class="sun__item-footer">
                                            <div class="sun__item-footer-link">
                                                <a class="type-link gray">Claim & Unstake</a>
                                            </div>
                                            <div class="sun__item-footer-button">
                                                <button class="buton-click">Continue mining for more profits</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                </section>
                                <section>
                                    <div class="sun__item">
                                        <div class="over">Ended</div>
                                        <div class="sun__item-header">
                                            <div class="sun__item-header-img">
                                                <img src="src/assets/g-logo.png" alt="" class="sun">
                                                <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                            </div>
                                            <div class="sun__item-header-text">
                                                <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                                <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                    <span class="x">4x</span>
                                                    <span>SUN</span>
                                                </span>
                                            </div>
                                        </div>
                                        <div class="sun__item-body">
                                            <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                            <div class="sun__item-body-table">
                                                <p class="hihi">Total Staked</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        22,400
                                                    </div>
                                                    <div class="">
                                                        SUN
                                                    </div>
                                                </div>
                                                <p class="hihi">My Staked</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        --
                                                    </div>
                                                    <div class="">
                                                        HT/TRX LP
                                                    </div>
                                                </div>
                                                <p class="hihi">Pending Claim</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        --
                                                    </div>
                                                    <div class="">
                                                        SUN
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="sun__item-footer">
                                            <div class="sun__item-footer">
                                                <div class="sun__item-footer-link">
                                                    <a class="type-link gray">Claim & Unstake</a>
                                                </div>
                                                <div class="sun__item-footer-button">
                                                    <button class="buton-click">Continue mining for more profits</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </section>
                            </div>
                        </div> 
                        <div class="pass-2"> 
                            <div class="body-3">
                                <section>
                                <div class="sun__item">
                                    <div class="over">Ended</div>
                                    <div class="sun__item-header">
                                        <div class="sun__item-header-img">
                                            <img src="src/assets/smile-logo.png" alt="" class="sun">
                                            <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                        </div>
                                        <div class="sun__item-header-text">
                                            <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                            <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                <span class="x">4x</span>
                                                <span>SUN</span>
                                            </span>
                                        </div>
                                    </div>
                                    <div class="sun__item-body">
                                        <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                        <div class="sun__item-body-table">
                                            <p class="hihi">Total Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    22,400
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                            <p class="hihi">My Staked</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    HT/TRX LP
                                                </div>
                                            </div>
                                            <p class="hihi">Pending Claim</p>
                                            <div class="sun__item-body-table-test">
                                                <div class=""> 
                                                    --
                                                </div>
                                                <div class="">
                                                    SUN
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="sun__item-footer">
                                        <div class="sun__item-footer-link">
                                            <a class="type-link gray">Claim & Unstake</a>
                                        </div>
                                        <div class="sun__item-footer-button">
                                            <button class="buton-click">Continue mining for more profits</button>
                                        </div>
                                    </div>
                                </div>
                                </section>
                                <section>
                                    <div class="sun__item">
                                        <div class="over">Ended</div>
                                        <div class="sun__item-header">
                                            <div class="sun__item-header-img">
                                                <img src="src/assets/lol.png" alt="" class="sun">
                                                <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                            </div>
                                            <div class="sun__item-header-text">
                                                <span class="sun__item-header-text-1"> SUN/TRX LP Pool </span><br>
                                                <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                    <span class="x">15x</span>
                                                    <span>SUN</span>
                                                </span>
                                            </div>
                                        </div>
                                        <div class="sun__item-body">
                                            <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                            <div class="sun__item-body-table">
                                                <p class="hihi">Total Staked</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        22,400
                                                    </div>
                                                    <div class="">
                                                        SUN
                                                    </div>
                                                </div>
                                                <p class="hihi">My Staked</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        --
                                                    </div>
                                                    <div class="">
                                                        HT/TRX LP
                                                    </div>
                                                </div>
                                                <p class="hihi">Pending Claim</p>
                                                <div class="sun__item-body-table-test">
                                                    <div class=""> 
                                                        --
                                                    </div>
                                                    <div class="">
                                                        SUN
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="sun__item-footer">
                                            <div class="sun__item-footer">
                                                <div class="sun__item-footer-link">
                                                    <a class="type-link gray">Claim & Unstake</a>
                                                </div>
                                                <div class="sun__item-footer-button">
                                                    <button class="buton-click">Continue mining for more profits</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    </section>
                                    <section>
                                        <div class="sun__item">
                                            <div class="over">Ended</div>
                                            <div class="sun__item-header">
                                                <div class="sun__item-header-img">
                                                    <img src="src/assets/t-logo.png" alt="" class="sun">
                                                    <img src="src/assets/token-logo.png " alt="" class="toke"> 
                                                </div>
                                                <div class="sun__item-header-text">
                                                    <span class="sun__item-header-text-1"> HT/TRX LP Pool </span><br>
                                                    <span class="sun__item-header-text-2"> Stake SUN/TRX LP Earn 
                                                        <span class="x">4x</span>
                                                        <span>SUN</span>
                                                    </span>
                                                </div>
                                            </div>
                                            <div class="sun__item-body">
                                                <div class="sun__item-body-time">2020.11.02 02:00:00</div>
                                                <div class="sun__item-body-table">
                                                    <p class="hihi">Total Staked</p>
                                                    <div class="sun__item-body-table-test">
                                                        <div class=""> 
                                                            22,400
                                                        </div>
                                                        <div class="">
                                                            SUN
                                                        </div>
                                                    </div>
                                                    <p class="hihi">My Staked</p>
                                                    <div class="sun__item-body-table-test">
                                                        <div class=""> 
                                                            --
                                                        </div>
                                                        <div class="">
                                                            HT/TRX LP
                                                        </div>
                                                    </div>
                                                    <p class="hihi">Pending Claim</p>
                                                    <div class="sun__item-body-table-test">
                                                        <div class=""> 
                                                            --
                                                        </div>
                                                        <div class="">
                                                            SUN
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="sun__item-footer">
                                                <div class="sun__item-footer">
                                                    <div class="sun__item-footer-link">
                                                        <a class="type-link gray">Claim & Unstake</a>
                                                    </div>
                                                    <div class="sun__item-footer-button">
                                                        <button class="buton-click">Continue mining for more profits</button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </section>
                                </div>
                        </div> 
                </div>
            </div>
            <div class="closeStake">
                <div v-if="check">
                <div class="mask">
                <div class="modal">
                <div class="connect__to-wallet">
                    <div class="connect__to-wallet-title">
                        <span @click.prevent="isStaking = !isStaking" :class="{lols: isStaking }" class="connect__to-wallet-title-1">Stake</span>
                        <span @click.prevent="isStaking = !isStaking" :class="{lols: !isStaking }"  class="connect__to-wallet-title-1">Claim</span>
                        <span @click.prevent="check=!check" class="connect__to-wallet-title-2">
                            <button class="remove">x</button>
                        </span>
                    </div>
                    
                    <div v-if="isStaking" class="connect__to-wallet-body">
                        <p>Enter the amount of Token you want to stake</p>
                        <div class="connect__to-wallet-body-item-1">
                            <div class="item">
                                <input type="text" class="testtt" id="amountStake">
                            </div>
                            <div class="item-text-1">
                                <span>Token</span>
                            </div>
                        </div>
                        <p style="color:#5915e1;">Blance of stake token: {{balanceStake}}</p>
                        <p>Enter the amount of TRX you want to stake</p>
                        <div class="connect__to-wallet-body-item-1">
                            <div class="item">
                                <input type="text" class="testtt" id="amountTRX">
                            </div>
                            <div class="item-text-1">
                                <span>TRX</span>
                            </div>
                        </div>
                        <div  class="connect__to-wallet-body-link">
                            <p>Token Blance: {{balanceOf}}</p>
                            <p>TRX Blance: {{balan}}</p>
                            <button class="buton-click" @click="triggerSmartContract1">stakeToken</button>
                            <button class="buton-click" @click="triggerSmartContract2">stakeTRX</button>
                        </div>
                    </div>
                    <div v-else class="connect__to-wallet-body">
                    <p>UnStaking</p>
                    <div class="connect__to-wallet-body-item-1">
                        <div class="item">
                            <input type="text" class="testtt" id="amount">
                            
                        </div>
                        <div class="item-text-1">
                            <span>Token</span>
                        </div>
                    </div>
                    <p>Index</p>
                    <div class="connect__to-wallet-body-item-1">
                        <div class="item">
                            <input type="text" class="testtt" id="index">
                            
                        </div>
                    </div>
                    
                    <div class="connect__to-wallet-body-link">
                        <p >Balance of stake:{{balanceStake}} </p>
                        <button class="buton-click" @click="withdraww()" > withdraw </button>
                        <button class="buton-click" @click="unStaking()" > Unstake </button>
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
    data: function() {
        return {
            isEnded: true,
            check:true,
            isStaking:true,
            adress:'',
            balan:0,
            Address:'TEfPRoBKPj6zUXNKofQ9asrJoNk8gP9Rd3',
            ad:'TWQ1xAk6EQh2hV1dDZV6e6S31yBfeMiP1A',
            balanceOf:'' ,
            withdrw:0,
            withdrwbank:'',
            unstake:'',
            bank:'TS2RKxkobAQQaxyzK5aEsHLbkyJVGuiZCv',
            bank2:'TKZXntDU8PC9kGF1LNukgDwxXBpDk6M2jV',
            index:'15',
            am:'1000000',
            balanceStake:'',
            Address2:'TWR2i5ERPmPeW86eZ8beb16HbyukgUqdxZ'
        }
    },
    methods: {
             
            async triggerSmartContract1(){
                    const trc20ContractAddress = "TEfPRoBKPj6zUXNKofQ9asrJoNk8gP9Rd3";//contract address
                    var address = "{{adress}}";//msg
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
                    
                },
            async triggerSmartContract2(){
                    const trc20ContractAddress = "TT1d69x3ETgweUmTWFLEVFX1AErVTamGE4";//contract address
                    var address = "{{adress}}";//msg
                    var amountTRX = parseInt(document.getElementById('amountTRX').value);
                    try {
                        let contract = await tronWeb.contract().at(trc20ContractAddress);
                        //Use call to execute a pure or view smart contract method.
                        // These methods do not modify the blockchain, do not cost anything to execute and are also not broadcasted to the network.
                        let result = await contract.stakeTRX(
                            
                        ).send({
                            callValue: amountTRX,
                            feeLimit: 5000000
                        }).then(output => {console.log('- Output:', output, '\n');});
                    } catch(error) {
                        console.error("trigger smart contract error",error)
                    }
                    
                },  
            getbalanceTRX:function(){
                    tronWeb.trx.getBalance('TWQ1xAk6EQh2hV1dDZV6e6S31yBfeMiP1A')
                    .then(result =>this.balan=result/10**6)
                },
            async getBalanceOfToken(){
                let contract = await window.tronWeb.contract().at(this.Address);
                await contract.balanceOf(this.ad).call()
                //.then(result => this.balanceOf = result/10)
                .then(result => this.balanceOf = parseInt(result.balance._hex)/10**6)
                }, 
                gettronweb: function(){
                    if(window.tronWeb && window.tronWeb.defaultAddress.base58){
                    this.adress=window.tronWeb.defaultAddress.base58
                    
                    }
                },
            openStake: function(){
                    var close = document.querySelector('.closeStake')
                    close.classList.add('openStake')
                    this.check = true
                },
            async withdraww(){
                let contract = await window.tronWeb.contract().at(this.Address);
                 let result = await contract.withDraw(this.index).send({feeLimit: 50000000})
                .then(result => this.withdrw = parseInt(result._hex))
            
            },
            /*async withdrawbank(){
                var index = parseInt(document.getElementById("amount").value);
                let contract = await window.tronWeb.contract().at('TS2RKxkobAQQaxyzK5aEsHLbkyJVGuiZCv');
                 await contract.withDraw('TKZXntDU8PC9kGF1LNukgDwxXBpDk6M2jV',amount).send() 
                .then(result => this.withdrwbank = parseInt(result.balances))
            
            },*/
            async unStaking(){
                var amount = parseInt(document.getElementById("amount").value);
                var index = parseInt(document.getElementById("index").value);
                let contract = await window.tronWeb.contract().at(this.Address);
                 await contract.unStaking(amount,index).send() 
                .then(result => this.unStake= parseInt(result.balance)/10**6)
            
            },
            async getBalanceOfStake(){
                let contract = await window.tronWeb.contract().at(this.Address);
                await contract.balanceOfStake(this.ad).call()
                .then(result => this.balanceStake = result/10**6)
                // .then(result => this.balanceStake = parseInt(result.balance._hex))
                },
            /*async UnStaking(){
                    const trc20ContractAddress = "TEfPRoBKPj6zUXNKofQ9asrJoNk8gP9Rd3";//contract address
                    var amountUnStake =  value ;
                    var index =  value ;
                    try {
                        let contract = await tronWeb.contract().at(trc20ContractAddress);
                        let result = await contract.unStaking(
                            amountUnStake,
                            index
                        ).send({
                             
                            
                        }).then(result => this.unStake= parseInt(result.balance)/10**6);
                    } catch(error) {
                        console.error("trigger smart contract error",error)
                    }
                    
                }, */
            },
            created() {
                this.interval = setInterval(() => this.gettronweb(), 1000);
            }
        }
</script>

<style>
.testtt{
    border:none;
}
    .buton{
        border: 0px solid rgb(89,21,225);
        background-color: rgb(89,21,225);
    }
     .color{
        color: #5915e1!important;
        }
    .closeStake{
        display:none;
        }
    .closeStake.openStake{
        display:block;
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
        .connect__to-wallet{
            pointer-events: auto;
            width: 372px;
            height: 525px;
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
            margin-top:-142%;
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
            margin-top:-27%;
        }
        .item{
            width:492px;
            height:90px;
            margin-top:23%
        }
        .item input{
            outline:none;
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
            margin-top:10%;
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
        .lols{
                color:#5915e1!important;
                border-bottom:3px solid blue;
            }
</style>
