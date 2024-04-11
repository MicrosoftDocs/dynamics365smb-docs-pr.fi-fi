---
title: Työnkulkujen luominen työnkulkumalleista
description: Voit säästää aikaa uusien hyväksymistyönkulkujen luomisessa luomalla työnkulut työnkulkumalleista.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dajoo
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Työnkulkujen luominen työnkulkumalleista

Voit luoda **Työnkulku**-sivulla työnkulun luomalla riveillä työnkulkuvaiheiden sarjan. Jokainen vaihe koostuu työnkulun tapahtumasta (Kun - tapahtuma), jota valvotaan tapahtuman ehtojen mukaan (Ehto) ja työnkulun vastauksesta (Sitten-vastaus), jota valvotaan vastausvaihtoehtojen mukaan. Työnkulkurivien kentissä on kiinteä luettelo tapahtumien ja vastausten arvoja, jotka ilmaisevat tuettuja [!INCLUDE [prod_short](includes/prod_short.md)]-skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).

Uusien hyväksymistyönkulkujen luonnissa säästyy aikaa, sillä [!INCLUDE [prod_short](includes/prod_short.md)] sisältää työnkulkumalleja. Mallit on saatavana **Työnkulkumallit**-sivulla. Malleja voi käyttää sellaisenaan tai ne voidaan muokata omia tarpeita vastaaviksi. Microsoftin työnkulkumallien koodien etuliitteenä on **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Jos työnkulkumallia muutetaan, jota myöhemmin kadutaan, työnkulun alkuperäinen asetus voidaan palauttaa **Palauta Microsoft-mallit** -toiminnolla.

> [!CAUTION]
> **Palauta Microsoft-mallit** -toiminto palauttaa kaikki Microsoftin työnkulkumallit. Yhden mallin palauttaminen ei ole mahdollista.  

Työnkulku voidaan luoda nopeasti myös tuomalla se esimerkiksi tuomalla se toisesta [!INCLUDE[prod_short](includes/prod_short.md)] -esiintymästä. Lisätietoja on kohdassa [Työnkulkujen vieminen ja tuominen](across-how-to-export-and-import-workflows.md).  

## Työnkulun luominen työnkulkumallista

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Uusi työnkulku mallista** -toiminto. **Työnkulkumallit**-sivu avautuu.  
3. Valitse työnkulkumalli, sitten **OK**.  

   Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään esimerkiksi ”-01”, joka osoittaa, että kyseessä on ensimmäinen työnkulkumallista luotu työnkulku.  
4. Työnkulku mukautetaan muokkaamalla työnkulun vaiheita tai lisäämällä uusia vaiheita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

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
