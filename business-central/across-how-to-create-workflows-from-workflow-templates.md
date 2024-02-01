---
title: Työnkulkujen luominen työnkulkumalleista
description: 'Voit säästää aikaa luodessasi uusia hyväksyntätyönkulkuja luomalla ei-muokattavia työnkulkuja työnkulkumalleista, joiden etuliitteenä on "MS".'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Työnkulkujen luominen työnkulkumalleista

Voit säästää aikaa uusien hyväksyntätyönkulkujen luomisessa käyttämällä työnkulkumalleja.  

Työnkulkumallit ovat [!INCLUDE[prod_short](includes/prod_short.md)] -oletusversion työnkulkuja, joita ei voi muokata. Työnkulkumallien koodit, jotka Microsoft on luonut, sisältävät etuliitteen "MS-".  

Työnkulun voi nopeasti myös tuomalla aiemmin luodun työnkulun, joka on [!INCLUDE[prod_short](includes/prod_short.md)]in ulkopuolisessa tiedostossa. Lisätietoja on kohdassa [Työnkulkujen vieminen ja tuominen](across-how-to-export-and-import-workflows.md).  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## Työnkulun luominen työnkulkumallista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Uusi työnkulku mallista** -toiminto. **Työnkulkumallit**-sivu avautuu.  
3. Valitse työnkulkumalli, sitten **OK**.  

   Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään esimerkiksi ”-01”, joka osoittaa, että kyseessä on ensimmäinen työnkulkumallista luotu työnkulku.  
4. Jatka työnkulun luontia muokkaamalla työnkulun vaiheita tai lisäämällä uusia vaiheita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## Katso myös

[Hyväksymistyönkulkujen luominen](across-how-to-create-workflows.md)  
[Hyväksymistyönkulkujen vieminen ja tuominen](across-how-to-export-and-import-workflows.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Hyväksymistyönkulkujen poistaminen](across-how-to-delete-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
