---
title: Käyttöomaisuuden käytöstä poistaminen
description: 'Kun myyt tai muuten luovutat käyttöomaisuuden, luovutusarvo on kirjattava voiton tai tappion laskemista ja tallentamista varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä

Kun myyt tai muuten luovutat käyttöomaisuuden, luovutusarvo on kirjattava voiton tai tappion laskemista ja tallentamista varten. Luovutustapahtuman tulee olla viimeinen tapahtuma, joka käyttöomaisuudelle on kirjattu. Osittain luovutetun käyttöomaisuuden osalta voidaan kirjata useampi kuin yksi luovutustapahtuma. Kaikkien kirjattujen luovutussummien kokonaissumman tulee olla kredit-summa.  

> [!NOTE]  
> Jos käyttöomaisuuserä vaihdetaan toiseen, sekä vanhan käyttöomaisuuserän myynti (luovutus) että uuden käyttöomaisuuserän osto (hankinta) tulee tallentaa. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).  

Seuraavissa vaiheissa oletetaan, että kirjausryhmät on määritetty **KO:n kirjausryhmät** -sivulla. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Luovutuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirjat** ja valitse sitten liittyvä linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **KO:n kirjaustyyppi** -kentässä **Luovutus**.  
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty luovutuksen kirjaamista varten.  

    > [!NOTE]  
    >  Vaihe 4 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Luovutustili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Luovutuksen vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle vastatilitapahtumien arvonkorotus kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valitse **Kirjaa**-toiminto.  

Jos myyt osan käyttöomaisuudesta tai muuten luovut osasta käyttöomaisuutta, omaisuuserä tulee jakaa ennen kuin luovutustransaktion voi tallentaa. Lisätietoja on kohdassa [Käyttöomaisuuden siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Luovutustapahtumien katsominen

Kun myyt tai luovutat käyttöomaisuutta, luovutusarvo kirjataan pääkirjanpitoon, jossa tulosta voi tarkastella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.  
2. Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.  
3. Valitse poistokirja, jonka tapahtumia haluat tarkastella. Valitse sitten **Tapahtumakirjaukset**-toiminto.  
4. Valitse **KO:n kirjausluokka** -kentässä rivi, joka sisältää **luovutuksen**. Valitse sitten **Etsi kirjaukset**-toiminto.  
5. Valitse **Etsi kirjaukset**-sivulla pääkirjanpidon tapahtuman rivi ja valitse sitten **Näytä liittyvät kirjaukset**-toiminto.  

Näyttöön tulee **Pääkirjanpidon tapahtumat** -sivu, jossa näkyvät tapahtumat, joiden tuloksena on luovutuksen kirjaaminen.  

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Etsi tapahtumat](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
