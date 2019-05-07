---
title: Huoltojen laskujen ja hyvityslaskujen luominen | Microsoft Docs
description: Lisätietoja laskuista, joilla huollosta maksetaan.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 62fd9e94b810887ecb152bba5a58c2f724b4025b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "913199"
---
# <a name="create-service-invoices-or-credit-memos"></a>Huoltolaskujen ja hyvityslaskujen luominen
Huoltotilausten laskuttamisen helppous on yksi [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tärkeimmistä ominaisuuksista. Voit lähettää laskun asiakkaille milloin tahansa tai voit luoda laskut jaksoittain.  
  
Laskun voi luoda suoraan **Huoltosopimus**-sivulla. Järjestelmän voi myös määrittää niin, että huoltoteknikko voi luoda laskun kentällä, vaikka palvelua ei olisikaan liitetty sopimukseen tai tilaukseen.  

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Huoltosopimuksen laskuttaminen Huoltosopimus -ikkunassa   
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo huoltosopimuslaskuja** ja valitse sitten liittyvä linkki.  
2. Määritä käytettävät suodattimet.  
3. Anna **Kirjauspvm**-kenttään päivämäärä, jota haluat käyttää huoltolaskujen kirjauspäivämääränä.  
4. Anna **Lasku pvm:ään asti** -kenttään päivämäärä, johon asti haluat laskuttaa sopimuksia. Eräajoon sisällytetään sopimukset, joiden seuraava laskutuspäivämäärä on ennen tätä päivämäärää.  
5. Valitse **Toiminto**-kentässä **Luo laskut**.  
6. Luo huoltolaskut valitsemalla **OK**.  
  
  > [!NOTE]  
  >  Et voi luoda huoltosopimuksen huoltolaskuja, kun **Muuta tilaa** -kentän arvoksi on määritetty **Avoin**.  
  
## <a name="to-post-an-invoice-from-a-service-order"></a>Kulutuksen kirjaaminen huoltotilauksesta  
Seuraavassa kuvataan, miten asiakkaalta veloitettava huollon osa määritetään.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten liittyvä linkki.  
2. Valitse laskutettava huoltotilaus ja avaa tilauksen kortti.  
3. Valitse **Huoltorivit**-toiminto.  
4. Etsi tarvittavat tapahtumat ja määritä sitten **Laskutettava määrä** -kentässä määrät, jotka veloitat asiakkaalta.  
  
   > [!NOTE]  
   >  Voit laskuttaa asiakasta rekisteröidystä palvelusta joko kokonaan tai osissa. Jos asiakkaalle halutaan lähettää lasku koko summasta, **Laskutettava määrä** -ja **Määrä**-kentän arvon on oltava sama. Voit lähettää koko laskun yhdessä koko lähetyksen kanssa ja voit kirjata täyden laskun jo aiemmin kirjatulle koko toimitukselle, jota ei ole laskutettu eikä käytetty viime aikoina.  
   >   
   >  Voit määrittää laskun määrän kahdella eri tavalla, kun kirjaat osittaisen laskun. Jos aiot kirjata huollon **Toimitus- ja Lasku**-valinnan kanssa, **Laskutettava määrä** -kentän arvon on oltava sama kuin **Toimitettava määrä** -kentän arvo. Jos haluat laskuttaa aiemmin kirjatun toimituksen, laskun määrä ei saa olla suurempi kuin **Toimitettu määrä** -kentän arvo.  
  
5. Valitse ensin **Kirjaa** ja sitten joko **Lasku** tai **Toimitus ja lasku**. Lisätietoja näistä vaihtoehdoista on kohdassa [Kirjaaminen huoltohallinnassa](service-service-posting.md).  
  
 Valitsemasi huoltorivi kirjataan. Voit kirjata useita huoltorivejä kerralla valitsemalla ne kaikki ja valitsemalla **Kirjaus**. Jos teet näin, varmista, että olet täyttänyt kaikkien kirjattavien rivien tarvittavat tiedot.  
  
 Kun kirjaat tilauksen ilman **Lasku**-valintaa, ohjelma luo kirjatun huoltolaskun sekä vastaavat tapahtumat ja päivittää tilauksen huoltorivien kentät. Ohjelma päivittää myös aiemmin kirjatut toimitusasiakirjat laskutetuilla määrillä. Jos valitset **Toimitus ja lasku** -kirjausvalinnan, ohjelma luo myös kirjatun toimituksen.

## <a name="to-create-a-service-invoice-manually"></a>Huoltolaskun luominen manuaalisesti  
Tavallisesti kun kirjaat huoltotilauksen **Lasku**- tai **Toimitus ja lasku** -valinnan kanssa, ohjelma luo automaattisesti kirjatun huoltolaskun. Silti sinun on ehkä luotava lasku, jota ei ole linkitetty huoltosopimukseen tai huoltotilaukseen. Työvaiheessa kerrotaan, miten lasku luodaan, samalla kun asiakas vastaanottaa huollon.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten liittyvä linkki.  
2. Luo uusi huoltolasku.  
3. Syötä **Nro** -kentässä.  
  
    > [!NOTE]  
    >  Vaihtoehtoisesti jos olet määrittänyt huoltolaskuille numerosarjan **Huoltohallinnon asetukset**-sivulla, voit painaa Enter, jolloin ohjelma syöttää seuraavan saatavilla olevan laskunumeron.  
  
4. Syötä **Asiakasnro** -kentässä asiakkaan tunnus. Valitse asiamukainen asiakas luettelosta.  
  
    Ohjelma täyttää automaattisesti asiakkaaseen liittyvät kentät tiedoilla **Asiakas**-kortilta.  
  
5. Syötä päivämäärä **Kirjauspvm.**-kenttään. Tämä kenttä näkyy kirjatuissa tapahtumissa. Ohjelma täyttää tämän kentän nykyisellä käsittelypäivämäärällä, mutta sitä voi myös muuttaa manuaalisesti.  
6. Täytä **Asiakirjan pvm** -kenttä. Kenttään syöttämäsi päivämäärä näkyy tulostetussa laskussa, ja sen mukaan lasketaan myös eräpäivä.  
7. Täytä laskun huoltorivit. Rekisteröi huollossa käytetyt nimikkeet, resurssit ja/tai kustannukset täyttämällä **Tyyppi**-, **Nro**- ja **Määrä**-kenttä. 

## <a name="to-invoice-posted-shipment-lines"></a>Kirjattujen toimitusrivien laskuttaminen  
Voit luoda huoltolaskun huollolle, joka on jo toimitettu (huoltotilauksista), mutta jota ei ole vielä laskutettu tai kulutettu. Ohjelma mahdollistaa tietyn asiakkaan laskurivien täyttämisen automaattisesti valituilla kirjatuilla toimitusriveillä.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Luo laskurivit toimituille huolloille, jota ei ole laskutettu. Vaihtoehtoisesti voit lisätä kirjatut toimitusrivit laskuun **Hae toimitusrivit** -toiminnolla.  
4. Kirjaa huoltolasku.  
  
 Kirjattu huoltolasku ja vastaavat tapahtumat luodaan. Ohjelma myös päivittää aiemmin kirjatut toimitusasiakirjat laskutetuilla määrillä ja lähdetilausten huoltorivien määrillä.  

## <a name="to-create-a-combined-invoice"></a>Yhdistettyjen laskujen luominen  
Voit laskuttaa asiakkaalta eri huoltotilauksissa toimitettua huoltoa. Ohjelma luo laskurivit nimikkeille, resurssitunneille tai kustannuksille, jotka on jo toimitettu eri huoltotilauksista, mutta joita ei ole vielä laskutettu.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Hae palautustoimitusrivit** -toiminto. **Hae huoltotoimitusrivit** -sivulla näkyy kaikki asiakkaan toimitetut rivit, joita ei ole laskutettu.  
4. Lisää huoltotoimituksen rivit laskuun valitsemalla ensin laskutetun huollon rivit ja sitten **OK**.  

## <a name="to-create-a-service-credit-memo"></a>Uuden huollon hyvityslaskun luominen  
Huollon hyvityslaskuasiakirjaa käytetään yleensä silloin, kun asiakas palauttaa nimikkeen. Sitä voidaan kuitenkin käyttää myös silloin, kun asiakkaalle annetaan korvausta ja kun virheellinen lasku korjataan.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon hyvityslaskut** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Käsittelypäivämäärä näkyy **Kirjauspvm**- ja **Asiakirjapvm**-kentissä. Voit muuttaa sitä tarvittaessa.    
4. Syötä hyvityslaskun riveille tietoja nimikkeistä, jotka on palautettu tai poistettu tai asiakkaalle annettavasta korvauksesta.  

## <a name="see-also"></a>Katso myös
[Huoltolaskujen kirjaaminen](service-how-to-post-service-orders.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huollon kirjaus](service-service-posting.md)  
