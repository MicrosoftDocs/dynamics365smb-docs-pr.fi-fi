---
title: "Toimintaohje: Maksujen tarkasteleminen tai kohdistaminen manuaalisesti automaattisen kohdistuksen jälkeen| Microsoft Docs"
description: "Toimintaohje: Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d5515a3814d2fbd4dfb7accc16d9f8ffda44317
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-review-or-apply-payments-manually-after-automatic-application"></a>Toimintaohje: Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen
Voit avata kullekin maksua esittävälle päiväkirjan riville **Maksujen täsmäytyskirjauskansio** -ikkunassa **Maksun kohdistus** -ikkunan ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. Lisätietoja automaattisesta kohdistuksesta on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

**Tärkeää**: Kun täsmäytettävien maksujen pankkitili on määritetty käyttämään paikallista valuuttaa, **Maksun kohdistus** -ikkunassa näkyvät kaikki avoimet tapahtumat paikallisena valuuttana, mukaan lukien niiden asiakirjojen avoimet tapahtumat, jotka alun perin laskutettiin ulkomaan valuutassa. Maksut, jotka on kohdistettu tapahtumiin muunnetuilla valuutoilla, voidaan tämän vuoksi kirjata eri summilla kuin alkuperäinen asiakirja, koska pankki ja [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttävät eri vaihtokursseja.

Siksi on suositeltavaa etsiä ulkomaan valuuttakoodit **Valuuttakoodi**-kentästä **Maksun kohdistus** -ikkunasta ja tarkistaa perustuvatko kohdistukset muunnettuihin valuuttoihin. Voit tarkastaa alkuperäisen asiakirjan summan ulkomaan valuutassa ja tarkastella vaihtokurssia valitsemalla **Kohdistetaan tap. nroon** -kentän ja valitsemalla sitten pikavalikosta siirtymispainikkeen ja avaamalla **Asiakastapahtumat**- tai **Toimittajatapahtumat**-ikkunan.

[!INCLUDE[d365fin](includes/d365fin_md.md)] ei käsittele automaattisesti mitään valuutan muunnosten edellyttämiä voiton ja tappion mukautuksia.

**Huomautus**: Tapahtumia, joissa on eri etumerkki kuin maksussa, ei voi käyttää. Esimerkiksi, suljettaessa sekä negatiivinen hyvityslasku että sitä vastaava positiivinen lasku on ensin liitettävä hyvityslasku laskuun ja sitten liitettävä maksu laskuun, joka sisältää jäljelle jääneen loppusumman.

**Varoitus**: Jos käytät maksualennuksia ja jos maksupäivämäärä on ennen maksun eräpäivää, **Jäljellä oleva summa sis. alennuksen** -kenttää **Maksukohdistus**-ikkunassa käytetään kohdistukseen. Muussa tapauksessa käytetään **Jäljellä oleva summa** -kentän arvoa. Jos maksu on suoritettu jäljellä olevalla määrällä maksun eräpäivän jälkeen tai koko summa on maksettu, mutta alennus on myönnetty, summa ei täsmää.

**Huomautus**: Maksun voi kohdistaa vain yhteen tiliin. Jos haluat jakaa kohdistuksen useisiin avoimiin tapahtumiin, esimerkiksi kertasuorituksen käyttämiseksi, avointen tapahtumien on oltava samalle tilille. Lisätietoja on tämän ohjeaiheen menettelytavan vaiheiden 7 ja 8 mukaisesti.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Maksujen täsmäytyskirjauskansio** ja valitse sitten liittyvä linkki.
2. Avaa sen pankkitilin maksun täsmäytyspäiväkirja jolle haluat täsmäyttää maksut. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Maksujen täsmäytyskirjauskansio** -ikkunassa maksu, jonka haluat tarkistaa tai kohdistaa manuaalisesti yhteen tapahtumaan tai useisiin tapahtumiin. Valitse sitten **Kohdista manuaalisesti** -toiminto.
4. Valitse **Kohdistettu**-valintaruutu sen avoimen tapahtuman rivillä johon haluat käyttää maksua.
5. Maksusumma, joka näkyy myös **Tapahtuman summa** -kentässä **Maksun kohdistus** -ikkunassa, lisätään **Kohdistettu summa** -kenttään, mutta voit muuttaa kenttää esimerkiksi silloin, kun haluat kohdistaa summan useaan avoimeen tapahtumaan.
6. Voit kohdistaa osan maksetusta summasta tilin toiseen avoimeen tapahtumaan, esimerkiksi kertasumman kohdistamiseksi, valitsemalla rivin **Kohdistettu**-valintaruudun. Kohdistettu summa vähennetään automaattisesti tapahtumien summasta vastaamaan jakautumista kahteen avoimeen tapahtumaan.
7. Voit kohdistaa osan maksusta yhteen tai useaan avoimeen tapahtumaan, joka ei ole tietokannassa, luomalla uuden rivin saman tilin riville. Syötä **Kohdistettu summa** -kenttään uudelle riville kohdistettava summa ja säädä sitten olemassa olevan rivin **Kohdistettu summa** -kenttää.
8. Toista vaiheet 5, 6 tai 7 niiden muiden avointen tapahtumien osalta, joihin haluat kohdistaa täyden tai osittaisen maksusumman.
9. Kun olet tarkistanut maksun kohdistuksen tai kohdistanut manuaalisesti yhteen tai useampaan tapahtumaan valitse **Hyväksy kohdistus** -toiminto.

**Maksun kohdistus** -ikkuna sulkeutuu. **Maksujen täsmäytyskirjauskansio** -ikkunan **Vastaavuuden luotettavuus** -kentän arvoksi tulee **Hyväksytty**. Se osoittaa, että olet tarkistanut maksun tai ottanut sen käyttöön manuaalisesti.

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

