---
title: Hyväksyntätyönkulkujen poistaminen
description: 'Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä. Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="delete-approval-workflows"></a>Hyväksymistyönkulkujen poistaminen

Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä. Kaikkien työnkulun osavaiheiden instanssilla pitää olla **Valmis**-tila.

> [!CAUTION]
> Kun poistat työnkulun, kaikki työnkulun tiedot menetetään.

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät käyttämällä tapahtumien kiinteitä luetteloita ja vastausarvoja, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Hyväksyntätyönkulkujen luominen](across-how-to-create-workflows.md).

## <a name="delete-a-workflow"></a>Työnkulun poistaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.
2. Valitse työnkulku, jonka haluat poistaa.
3. Valitse **Poista**-toiminto.
4. Voit myös avata työnkulun, jonka haluat poistaa.
5. Valitse **Työnkulku**-sivulla **Poista**-toiminto.

> [!NOTE]
> Työnkulun poistaminen edellyttää sen poistamista käytöstä. Voit poistaa työnkulun käytöstä avaamalla sen **Työnkulut**-sivulla ja poistamalla **käytössä**-vaihtoehdon käytöstä.

## <a name="see-also"></a>Katso myös

[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Hyväksymistyönkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
