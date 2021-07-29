---
title: Automaattisesti kohdistettujen maksujen tarkistaminen ja maksujen kohdistaminen uudelleen manuaalisesti | Microsoft Docs
description: Kun maksut on kohdistettu automaattisesti, voit tarkastella maksun kaikkia tapahtumia ja kohdistaa manuaalisesti uudelleen virheellisesti kohdistetut maksut.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dce6cdfdf70d968ae06c88ad4d567ad5cde803dd
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443239"
---
# <a name="review-and-apply-payments-manually-after-automatic-application"></a>Maksujen tarkasteleminen ja kohdistaminen automaattisen kohdistuksen jälkeen
Voit avata kullekin **Maksujen täsmäytyskirjauskansio** -sivulla maksua esittävälle päiväkirjan riville **Maksun kohdistus** -sivun ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. Lisätietoja automaattisesta kohdistuksesta on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Kun täsmäytettävien maksujen pankkitili on määritetty käyttämään paikallista valuuttaa, kaikki avoimet tapahtumat näkyvät **Maksun kohdistus** -sivulla paikallisena valuuttana, mukaan lukien niiden asiakirjojen avoimet tapahtumat, jotka alun perin laskutettiin ulkomaan valuuttana. Maksut, jotka on kohdistettu tapahtumiin muunnetuilla valuutoilla, voidaan tämän vuoksi kirjata eri summilla kuin alkuperäinen asiakirja, koska pankki ja [!INCLUDE[prod_short](includes/prod_short.md)] käyttävät eri vaihtokursseja.

Siksi on suositeltavaa etsiä ulkomaan valuuttakoodit **Valuuttakoodi**-kentästä **Maksun kohdistus** -sivulla ja tarkistaa perustuvatko kohdistukset muunnettuihin valuuttoihin. Voit tarkastaa alkuperäisen asiakirjan summan ulkomaan valuuttana ja tarkastella vaihtokurssia valitsemalla **Kohdistetaan tap. nroon** -kentän ja valitsemalla sitten pikavalikossa porautumispainikkeen, joka avaa **Asiakastapahtumat**- tai **Toimittajatapahtumat**-sivun.

[!INCLUDE[prod_short](includes/prod_short.md)] ei käsittele automaattisesti mitään valuutan muunnosten edellyttämiä voiton ja tappion mukautuksia.

> [!NOTE]  
>   Tapahtumia, joissa on eri etumerkki kuin maksussa, ei voi käyttää. Esimerkiksi, suljettaessa sekä negatiivinen hyvityslasku että sitä vastaava positiivinen lasku on ensin liitettävä hyvityslasku laskuun ja sitten liitettävä maksu laskuun, joka sisältää jäljelle jääneen loppusumman.

> [!WARNING]  
>   Jos käytät maksualennuksia ja jos maksupäivämäärä on ennen maksun eräpäivää, **Maksukohdistus**-sivun **Jäljellä oleva summa sis. alennuksen** -kenttää käytetään kohdistukseen. Muussa tapauksessa käytetään **Jäljellä oleva summa** -kentän arvoa. Jos maksu on suoritettu jäljellä olevalla määrällä maksun eräpäivän jälkeen tai koko summa on maksettu, mutta alennus on myönnetty, summa ei täsmää.

> [!NOTE]  
>   Voit nyt kohdistaa maksun yhteen tiliin. Jos haluat jakaa kohdistuksen useisiin avoimiin tapahtumiin, esimerkiksi kertasuorituksen käyttämiseksi, avointen tapahtumien on oltava samalle tilille. Lisätietoja on tämän ohjeaiheen menettelytavan vaiheiden 7 ja 8 mukaisesti.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Avaa sen pankkitilin maksun täsmäytyspäiväkirja jolle haluat täsmäyttää maksut. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Maksujen täsmäytyskirjauskansio** -sivulla maksu, jonka haluat tarkistaa tai kohdistaa manuaalisesti yhteen tapahtumaan tai useisiin tapahtumiin. Valitse sitten **Kohdista manuaalisesti** -toiminto.
4. Valitse **Kohdistettu**-valintaruutu sen avoimen tapahtuman rivillä johon haluat käyttää maksua.
5. Maksusumma, joka näkyy myös **Tapahtuman summa** -kentässä **Maksun kohdistus** -sivulla, lisätään **Kohdistettu summa** -kenttään, mutta voit muuttaa kenttää esimerkiksi silloin, kun haluat kohdistaa summan useaan avoimeen tapahtumaan.
6. Voit kohdistaa osan maksetusta summasta tilin toiseen avoimeen tapahtumaan, esimerkiksi kertasumman kohdistamiseksi, valitsemalla rivin **Kohdistettu**-valintaruudun. Kohdistettu summa vähennetään automaattisesti tapahtumien summasta vastaamaan jakautumista kahteen avoimeen tapahtumaan.
7. Voit kohdistaa osan maksusta yhteen tai useaan avoimeen tapahtumaan, joka ei ole tietokannassa, luomalla uuden rivin saman tilin riville. Syötä **Kohdistettu summa** -kenttään uudelle riville kohdistettava summa ja säädä sitten olemassa olevan rivin **Kohdistettu summa** -kenttää.
8. Toista vaiheet 5, 6 tai 7 niiden muiden avointen tapahtumien osalta, joihin haluat kohdistaa täyden tai osittaisen maksusumman.
9. Kun olet tarkistanut maksun kohdistuksen tai kohdistanut manuaalisesti yhteen tai useampaan tapahtumaan valitse **Hyväksy kohdistus** -toiminto.

**Maksun kohdistus** -sivu sulkeutuu. **Maksujen täsmäytyskirjauskansio** -sivun **Vastaavuuden luotettavuus** -kentän arvoksi tulee **Hyväksytty**. Se osoittaa, että olet tarkistanut maksun tai ottanut sen käyttöön manuaalisesti.

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]