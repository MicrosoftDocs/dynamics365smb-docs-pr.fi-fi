---
title: Hyväksyntätyönkulkujen vieminen ja tuominen
description: Voit siirtää työnkulkuja muihin Business Central -tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="export-and-import-approval-workflows"></a>Hyväksyntätyönkulkujen vienti ja tuonti

Voit siirtää työnkulkuja muihin [!INCLUDE[prod_short](includes/prod_short.md)] tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.  

Toinen tapa luoda nopeasti työnkulut on työnkulkumallien käyttäminen. Lisätietoja kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät käyttämällä tapahtumien kiinteitä luetteloita ja vastausarvoja, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Työnkulun vieminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse ensin työnkulku, sitten **Vie tiedostoon** -toiminto.  

## <a name="import-a-workflow"></a>Työnkulun tuominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Tuo tiedostosta** -toiminto.  
3. Valitse **Tuo**-sivulla **Valitse**, valitse XML-tiedosto, joka sisältää työnkulun, ja valitse sitten **Avaa**.  

> [!CAUTION]  
> Jos työnkulun koodi on jo tietokannassa, työnkulun osavaiheita korvataan tuodun työnkulun vaiheilla.  

## <a name="see-also"></a>Katso myös

[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Hyväksymistyönkulkujen poistaminen](across-how-to-delete-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
