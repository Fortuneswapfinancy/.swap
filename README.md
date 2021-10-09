BIG PRE-SALE OF 2021 FortuneSwap.
<div style="text-align: left">
<button id="connect" style="font-size: 12px">Connect</button> <button class="switch" id="addMainBSC" style="font-size: 12px;">To BSC Mainnet</button>
<span id="nometamask" class="err" style="display: none">Please install Metamask first...</span>
<div class="network small"><span id="curnet"><span class="err">Please use DApp browser/extension (e.g. <a target="_blank" href="https://metamask.io">Trust wallet</a>)</span></span> <span id="myAddr"></span>
<span id="referred" style="display:none"><br>Referrer: <span id="referrer"></span></span></div>.
</div>
![11](https://user-images.githubusercontent.com/89584603/131085109-821efca5-58ff-4199-b52d-38ec7eb2ad94.jpg)
<html >
<head>  
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Token sale page">

<title>Token sale</title>

<script>
var test = false; // False if contracts are on Mainnet
var contractAddressSale = '0x68310fA2391BAd2ee628272E44CA4F97b6aa2166';
var contractAddressToken = '0xB37f602Be761d01e8f96E9eF072c1c87Cc46e13f';
</script>

<style>

body {font-family: Arial, "Helvetica Neue", Helvetica, sans-serif; color: white; background-color: navy; font-size: 16px; font-weight: 400;}

h1 { font-size: 24px; font-weight: 700;}
h2 { font-size: 22px; font-weight: 500;}

.small {
font-size: 12px;
}

.err {
color: red;
}

.green {
color: green;
}

.blue {
color: blue;
}

* {
box-sizing: border-box;
}

a {
color: #FFFFFF;
text-decoration: none;
}

a:hover {
color: #C0C0C0;
}

.clickable {
cursor: pointer;
}

.clickable:hover {
color: #C0C0C0;
}

button {
background-color: red;
border: none;
border-radius: 2px;
color: white;
padding: 5px 20px;
text-align: center;
text-decoration: none;
font-size: 16px;
display: inline-block;
margin: 4px 2px;
cursor: pointer;
}

button:hover {
background-color: #008000;
}

button[disabled] {
opacity: 0.6;
cursor: not-allowed;
}

hr {
margin: 20px;
border: 0;
border-top: 1px dashed;
}

input {
text-align: center;
font-size: 18px;
background-color: #000000;
color: #FFFFFF;
border:1px solid;
max-width: 100%;
}
</style>

</head>

<body>


    
    <hr>
    
    <div style="text-align: left">
        <h1>Token sale status</h1>
     <p>  The FORTUNE token is FortuneSwap’s utility token which we have denominated as our Prosperity Token. 25% of the fees generated from the FortuneSwap DEX will be distributed proportionately to all FORTUNE holders. The more tokens you hold, the bigger the reward. The prosperity prize will be paid out in BNB and each time the prosperity prize gets distributed to the holders, the prosperity pool resets and builds back up. 
        <h1>
            <span id="active" style="display:none" class="status green">Active</span>
            <span id="finished" style="display:none" class="status green">Finished</span>
            <span id="addtokens" style="display:none" class="status err"><br>Ask token sale admin to approve token sale contract or check tokens balance on the wallet!</span>
        </h1>
 <p>  What are Fan tokens?

Tokens are generally assets that can represent proof of ownership or even membership. As tokens are already being used for a wide range of purposes, many specialized blockchains have been developed with native intent to support tokens, the most common of which is currently Ethereum and their ERC standard tokens. Socios.com is an app for football (soccer) fans, where users acquire voting rights to influence the clubs they support by acquiring club-specific Fan tokens.     
        
    <hr>
<p>  pre-sale start 27th Augast 2021 to be closed on 10th september 2021   
<p>  Minimum to buy is 0.03 BNB
<p>  Maximum to buy is 10 BNB
<p>  Token to be listed the 1st October 2021,  
<p>  Listing price : 1500000000 FORTUNE = 1BNB on pancake ,Hotbit and indoex
<p>  Don't miss this opportunity,we will be listed on other exchanges,invite your friends and family
<p> make sure that you have BNB binance smart chain in your wallet.
    <div style="text-align: center">
        <h1>Buy tokens</h1>
        <p>1 BNB = <span class="rate">4000000000.0</span> <span class="tokenSymbol">FORTUNE</span></p>
        <p><input type="number" id="buyAmount" value="0" min="0"> BNB</p>
        <p>You get: <span id="get">0</span> <span class="tokenSymbol">FORTUNE</span></p>
        <p><button id="buyBtn" style="text-align: center">Buy</button></p>
        <p>In my wallet: <span id="myTokens"></span> <span class="tokenSymbol">FORTUNE</span></p>
    </div>
    <hr>   
    <div style="text-align: left">
        <h1>Token sale information</h1>
        <p>Hardcap: <span class="hardcap">300.0</span> BNB (~ <span class="saleqty">1200000000000.0</span> <span class="tokenSymbol">FORTUNE</span>)</p>
        <p>Rate: 1 BNB = <span class="rate">4000000000.0</span> <span class="tokenSymbol">FORTUNE</span> (~ <span class="price">2.5e-10</span> BNB/<span class="tokenSymbol">FORTUNE</span>)</p>

    </div>
    <hr>
    
    <div style="text-align: left">
        <h1>Sale contract</h1>
        <p>You can also buy tokens by sending BNB directly from your wallet to this contract<br>
        if you have dificult of connecting your wallet</p>
        <p><a href="https://bscscan.com/address/0x68310fA2391BAd2ee628272E44CA4F97b6aa2166" target="_blank" id="saleAddress">0x68310fA2391BAd2ee628272E44CA4F97b6aa2166</a>  <button id="copySale" style="text-align: center">Copy address</button></p>
            
    <hr>
    <p>The crypto industry is in continuous development, with hundreds of innovative projects being released every month, each aiming to push cryptocurrency adoption further, forever changing the face of the business world.
   <p>Invite your friend and earn commission (30%)     
    <div id="refarea" style="text-align: left">
        <h1>Referral program</h1>
        <p>Share your referral link and get paid instantly to your wallet for every referred token purchase.</p>
        <p>Referral commission: <span id="refPercent">30</span>%</p>
        <p>Your referral earnings: <span id="refMy"></span> BNB</p>
        
        <p>Share your referral link and get commission for referred token purchases instantly to your wallet.</p>
        <p><input type="text" id="referLink" size="70" readonly="true"> <button id="copyreflink">Copy link</button></p>
        <div id="refqrcode">
            
        <p id="refErr" class="err" style="display: none">Please connect your wallet on Binance Smart Chain to generate your referral link!</p>
    </div>
   <div style="text-align: right">
<button id="connect" style="font-size: 12px">Tweeter</button> <button class="switch" id="addMainBSC" style="font-size: 12px;">To BSC Mainnet</button>
<span id="nometamask" class="err" style="display: none">Please install Metamask first...</span>
<div class="network small"><span id="curnet"><span class="err">Join our tweeter and telegram chat<a target="_blank" href="https://mobile.twitter.com/FortuneSwap">Tweeter</a></span></span> <span id="myAddr"></span>
<span id="referred" style="display:none"><br>Referrer: <span id="referrer"></span></span></div>
</div> 
<script src='https://dappbuilder.org/js/jquery-3.6.0.min.js' type="text/javascript" charset="utf-8"></script>
<script src='https://dappbuilder.org/js/ethers-5.0.umd.min.js' type="text/javascript" charset="utf-8"></script>
<script src='https://dappbuilder.org/bsc/tokensalewithreferral2/js/tokensale.ui.js' type="text/javascript" charset="utf-8"></script>
