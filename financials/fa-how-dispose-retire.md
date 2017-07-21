---
title: "Käyttöomaisuuden käytöstä poistaminen| Microsoft Docs"
description: "Käyttöomaisuudelle on kirjattava poistoarvo, kun se hävitetään, myydään tai poistetaan käytöstä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 5fc65c97e7c95a37d54b4084aaf8616169b625db
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>Toimintaohje: Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä
Kun myyt tai muuten luovutat käyttöomaisuuden, luovutusarvo on kirjattava voiton tai tappion laskemista ja tallentamista varten. Luovutustapahtuman tulee olla viimeinen tapahtuma, joka käyttöomaisuudelle on kirjattu. Osittain luovutetun käyttöomaisuuden osalta voidaan kirjata useampi kuin yksi luovutustapahtuma. Kaikkien kirjattujen luovutussummien kokonaissumman tulee olla kredit-summa.  

> [!NOTE]  
>   Jos käyttöomaisuuserä vaihdetaan toiseen, sekä vanhan käyttöomaisuuserän myynti (luovutus) että uuden käyttöomaisuuserän osto (hankinta) tulee tallentaa. Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden hankinta](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Luovutuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **KO:n kirjaustyyppi** -kentässä **Luovutus**.  
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty luovutuksen kirjaamista varten.  

    > [!NOTE]  
>   Vaihe 4 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -ikkunan **Luovutustili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Luovutuksen vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle vastatilitapahtumien arvonkorotus kirjataan. Lisätietoja on "Käyttöomaisuuden kirjausryhmien määrittäminen" -osassa kohdassa [Toimintaohje: Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).  
5. Valitse **Kirjaa**-toiminto.  

    Jos myyt osan käyttöomaisuudesta tai muuten luovut osasta käyttöomaisuutta, omaisuuserä tulee jakaa ennen kuin luovutustransaktion voi tallentaa. Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Luovutustapahtumien katsominen
Kun myyt tai luovutat käyttöomaisuutta, luovutusarvo kirjataan pääkirjanpitoon, jossa tulosta voi tarkastella.  

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Käyttöomaisuus** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.  
3. Valitse poistokirja, jonka tapahtumia haluat tarkastella. Valitse sitten **Tapahtumakirjaukset**-toiminto.  
4. Valitse **KO:n kirjausluokka** -kentässä rivi, joka sisältää **luovutuksen**. Valitse sitten **Navigoi**-toiminto.  
5. Valitse **Navigointi**-ikkunassa pääkirjanpidon tapahtuman rivi ja valitse sitten **Näytä**-toiminto.  

Näyttöön tulee **Pääkirjanpidon tapahtumat** -ikkuna, jossa näkyvät tapahtumat, joiden tuloksena on luovutuksen kirjaaminen.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

