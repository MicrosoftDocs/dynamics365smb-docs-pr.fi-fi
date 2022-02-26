---
title: Konsernin asiakirjojen ja päiväkirjojen kirjaaminen
description: Tämä aihe selitää, miten voit kirjata tapahtumat konsernikumppanien kanssa konsernin asiakirjojen tai päiväkirjojen avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 610
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 903a0b1770bb29cb744f2aa8dc9510541ca7539c
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029402"
---
# <a name="work-with-intercompany-documents-and-journals"></a>Konserniasiakirjojen ja -päiväkirjojen käyttäminen
Voit kirjata tapahtumat konsernikumppanien kanssa konsernin asiakirjojen tai päiväkirjojen avulla. Kun kirjaat konsernin asiakirja- tai päiväkirjarivin omassa yrityksessä, vastaava asiakirja- ja päiväkirjarivi luodaan konsernin Lähtevät-kansioon kumppanille lähettämistä varten. Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.

Myynti- ja ostoasiakirjoissa oleva kyseisen asiakkaan tai toimittajan konsernikumppanikoodi varmistaa, että kaikki näihin yrityksiin liittyville tapahtumille muodostetut tilaukset ja laskut luovat vastaavat asiakirjat kumppaniyrityksessä. Tällä tavoin varmistetaan, että tilit täsmäytyvät oikein.

Konsernin yleisen päiväkirjan riville ei tarvitse määrittää yksittäisten tilijoukkojen tilejä ei tarvitse määrittää vaan kumppaniyrityksen tunnus riittää. Vastaavat konsernin yleisen päiväkirjan rivit luodaan sitten kumppaniyrityksessä siten, että kummankin tapahtuneen osallistuneen yrityksen tilit täsmäytetään.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Voit täyttää ja lähettää konsernin myyntitilauksen seuraavasti
Voit lähettää myynti- ja ostotilauksia sekä palauttaa tilauksia ennen kirjaamista. Laskut ja hyvityslaskut voi lähettää vasta, kun ne on kirjattu.

Seuraavissa ohjeissa neuvotaan, kuinka voit täyttää ja lähettää konsernin myyntitilauksen. Samat ohjeet koskevat myös konsernin osto- ja palautustilauksia sekä kirjattuja konsernin laskuja ja hyvityslaskuja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi myyntitilaus valitsemalla **Uusi**. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Varmista, että asiakas konsernikumppani.
5. Voit lähettää myyntitilauksen ennen sen kirjaamista valitsemalla **Lähetä konsernin myyntitilaus** -toiminto.

> [!NOTE]
> Jos et tee vaihetta 4, myyntitilaus siirretään konsernin Lähtevät-kansioon, josta voit lähettää sen myöhemmin. Lisätietoja on kohdassa [Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Voit täyttää ja kirjata konsernin päiväkirjan seuraavasti
Kun kirjaat konsernin yleisen päiväkirjan rivin omassa yrityksessä, vastaava päiväkirjarivi luodaan konsernin Lähtevät-kansioon kumppanille lähettämistä varten. Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin yleiset päiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa käsiteltävä päiväkirjaerä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).
3. Täytä tarvittavat kentät.
4. Anna **Konsernikumppanin KP-tilinro** kentässä se konsernin kirjanpitotilin numero, jolle summa kirjataan kumppaniyrityksessä.

    > [!NOTE]
    > Tämä kenttä on täytettävä, jos rivin **Tilinro**- tai **Vastatilin nro** -kentässä on pankkitili tai kirjanpitotili.  
5. Valitse **Kirjaa**-toiminto.

Kyseiset tapahtumat kirjataan omaan yritykseen ja päiväkirjaan. Lisäksi vastaavat tapahtumat luodaan konsernin Lähtevät-kansioon, josta voit lähettää ne kumppaniyritykselle. Lisätietoja on kohdassa [Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md).

## <a name="see-also"></a>Katso myös
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]