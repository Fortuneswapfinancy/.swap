
<!DOCTYPE html> 
<html > 
<head> 
    <meta charset="UTF-8"> 
    <meta http-equiv="X-UA-Compatible" content="IE=edge"> 
    <meta name="viewport" content ="width=device-width, initial-scale=1.0"> 
    <meta name="description" content="Page de vente de jetons"> 

    <title>Vente de jetons</title> 
   
    <script> 
        var test =faux ; // False si les contrats sont sur le réseau principal 
        var contractAddressSale = '0x68310fA2391BAd2ee628272E44CA4F97b6aa2166'; 
        var contractAddressToken = '0xB37f602Be761d01e8f96E9eF072c1c87Cc46e13f'; 
    </script> 
    
    <style> 
        
        body {font-family: Arial, "Helvetica Neue", Helvetica, sans-serif; couleur : #FFFFFF ; couleur d'arrière-plan : #000000 ; taille de la police : 16px ; font-weight: 400;} 

        h1 { font-size: 24px; font-weight: 700;} 
        h2 { font-size: 22px; font-weight: 500;} 

        .small { 
            font-size: 12px; 
        } 

        .err { 
             couleur : rouge ; 
        } 
        
        .vert { 
             couleur : vert; 
        } 
        
        .bleu { 
             couleur : bleu; 
        } 

        * { 
          box-sizing: border-box; 
        } 
        
        un {
          couleur : #FFFFFF ; 
          texte-décoration : aucun ; 
        } 
        
        a:hover { 
          color: #C0C0C0; 
        } 
        
        .clickable { 
            curseur : pointeur ; 
        } 
        
        .clickable:hover { 
            color: #C0C0C0; 
        } 
        
        bouton { 
          background-color: #283747; 
          bordure : aucune ; 
          rayon de bordure : 2px ; 
          Couleur blanche; 
          rembourrage : 5px 20px ; 
          text-align : centre ; 
          texte-décoration : aucun ; 
          taille de la police : 16px ; 
          affichage : bloc en ligne ; 
          marge : 4px 2px ;
          curseur : pointeur ; 
        } 
        
        button:hover { 
          background-color: #008000; 
        } 
        
        bouton [désactivé] { 
          opacité : 0,6 ; 
          curseur : non autorisé ; 
        } 
        
        hr { 
            marge : 20 px ; 
            bordure : 0 ; 
            border-top : 1px en pointillés ; 
        } 
        
        input { 
          text-align: center; 
          taille de la police : 18px ; 
          couleur d'arrière-plan : #000000 ; 
          couleur : #FFFFFF ; 
          bordure:1px solide ; 
          largeur maximale : 100 % ; 
        } 
    </style> 
    
</head>

<body> 
    
    <div style="text-align: center"> 
        <button id="connect" style="font-size: 12px">Connect</button> <button class="switch" id="ajouterMainBSC" style="font-size: 12px;">Vers le réseau principal BSC</button> 
        <span id="nometamask" class="err" style="display: none">Veuillez d'abord installer Metamask...</span> 
        <div class="network small"><span id="curnet "><span class="err">Veuillez utiliser le navigateur/l'extension DApp (par exemple <a target="_blank" href="https://metamask.io">Metamask</a>)</span></span > <span id="myAddr"></span> 
        <span id="referred" style="display:none"><br>Référent : <span id="referrer"></span></span>< /div> 
    </div> 
    
    <div style="text-align: center"> 
        <h1>Informations sur le jeton</h1>
        <h2><span id="nom du jeton"> Échange de fortune</span> (<span class="tokenSymbol">FORTUNE</span>)</h2> 
        <p><a target="_blank" href="https://bscscan.com/token/0xB37f602Be761d01e8f96E9eF072c1c87Cc46e13f0xB37f602Be761d01e8f96E9eF072c1c87Cc46e13f" id="adresse de jeton">0xB37f602Be761d01e8f96E9eF072c1c87Cc46e13f</a></p> 
        <!-- Réservé au cas où vous souhaiteriez afficher les décimales et l'offre totale : Decimals <span id="#tokenDecimals"></span> Approvisionnement total <span id="#tokenSupply"></span>--> 
        <p>N'envoyez pas de BNB au contrat de jeton !</p> 
        <p><button id="addToken" style="text-align: center">Ajouter à Metamask</button> <button id="copyToken" style="text-align: center">Copier l'adresse</button></p> 
    </div> 
    
    <hr> 
    
    <div style="text-align: center"> 
        <h1>Jeton état de la vente</h1> 
        <h1> 
            <span id="active" style="display:none" class="status green">Active</span> 
            <span id="finished" style="display:none" classe ="status green">Terminé</span>
            <span id="addtokens" style="display:none" class="status err"><br>Demandez à l'administrateur de la vente de jetons d'approuver le contrat de vente de jetons ou vérifiez le solde des jetons sur le portefeuille !</span> 
        </h1>
        <p><progress id="progress" value="0" max="100" style="width : 70 %"></progress></p> 
        <p>Élevé : <span id="raised"> </span> de <span class="hardcap">300,0</span> BNB</p> 
        <p>Jetons vendus : <span id="sold"></span> de <span class="saleqty">1200000000000.0</span> <span class="tokenSymbol">FORTUNE</span></p> 
        <p>Reste : <span id="toraise"></span> BNB (~ <span id="unsold"></span> <span class="tokenSymbol">FORTUNEFORTUNE</span>)</p> 
    </div> 
    <hr> 
    
    <div style="text-align: center"> 
        <h1>Acheter des jetons</h1> 
        <p>1 BNB = <span class="rate" >4000000000.0</span> <span class="tokenSymbol">FORTUNE</span></p> 
        <p><input type="number" id="buyAmount" value="0" min="0"> BNB</p> 
        <p>Vous obtenez : <span id=" get">0</span> <span class="tokenSymbol">FORTUNEFORTUNEFORTUNE</span></p> 
        <p><button id="buyBtn" style="text-align: center">Acheter</button></p> 
        <p>Dans mon portefeuille : <span id="myTokens "></span> <span class="tokenSymbol">FORTUNE</span></p> 
    </div> 
    <hr> 
    
    <div style="text-align: center"> 
        <h1>Informations sur la vente de jetons</h1> 
        <p>Hardcap : <span class="hardcap">300,0</span> BNB (~ <span class="saleqty">1200000000000.0</span> <span class="tokenSymbol">FORTUNE</span>)</p> 
        <p>Tarif : 1 BNB = <span class="rate">4000000000.0</span> <span class="tokenSymbol">FORTUNE</span> (~ <span class="prix">2.5e-10</span> BNB/<span class="tokenSymbol">FORTUNE</span>)</p> 

    </div> 
    <hr> 
    
    <div style="text-align: center"> 
        <h1>Contrat de vente</h1> 
        <p>Vous pouvez également acheter des jetons en envoyant des BNB directement depuis votre portefeuille à ce contrat<br> 
        (veuillez augmenter la limite de gaz à 200 000 ou même plus pour les jetons avec des fonctions spéciales comme l'autoLP, les échanges, etc.)</p> 
        <p><a href="https://bscscan.com/address/0x68310fA2391BAd2ee628272E44CA4F97b6aa2166" target="_blank" id="saleAddress">0x68310fA2391BAd2ee628272E44CA4F97b6aa2166</a> <button id="copySale" style="text-align: center">Copier l'adresse</button></p> 
            <div style="text-align: center" id="saleqr"></ div> 
    </div> 
    <hr> 
    
    <div id="refarea" style="text-align: center"> 
        <h1>Programme de 
        parrainage </h1> <p>Partagez votre lien de parrainage et soyez payé instantanément sur votre portefeuille pour chaque achat de jeton référé.</p> 
        <p>Total payé aux référents : <span id="refTotal"></span> BNB</p> 
        <p>Commission de parrainage : <span id="refPercent">30</span>%</p> 
        <p>Vos revenus de parrainage : <span id="refMy"></span> BNB</p> 
        
        <p>Partagez votre lien de parrainage ou votre code QR et obtenez une commission pour les achats de jetons parrainés instantanément dans votre portefeuille.</p> 
        <p><input type="text" id="referLink" size="70" readonly="true"> <button id="copyreflink">Copier le lien</button>< /p> 
        <div id="refqrcode"> 
            <div style="text-align: center" id="refqr"></div> 
        </div> 
        <p id="refErr" class="err" style= "afficher : aucun">Veuillez connecter votre portefeuille sur Binance Smart Chain pour générer votre lien de parrainage !</p> 
    </div> 
    
<script src='https://dappbuilder.org/js/jquery-3.6.0.min.js' type=" texte/javascript" charset="utf-8"></script>
<script src='https://dappbuilder.org/js/ethers-5.0.umd.min.js' type="text/javascript" charset="utf-8"></script> 
<script src='https ://dappbuilder.org/bsc/tokensalewithreferral2/js/tokensale.ui.js' type="text/javascript" charset="utf-8"></script> 

</body> 
</html>
