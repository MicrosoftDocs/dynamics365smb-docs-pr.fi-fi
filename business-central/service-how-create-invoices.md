---
title: Huoltojen laskujen ja hyvityslaskujen luominen
description: Opi luomaan palveluillesi saumattomasti laskuja ja hyvityslaskuja Business Centralin avulla.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Huoltolaskujen ja hyvityslaskujen luominen
Huoltotilausten laskuttamisen helppous on yksi [!INCLUDE[prod_short](includes/prod_short.md)]:n tärkeimmistä ominaisuuksista. Järjestelmän voi määrittää kohteen [!INCLUDE[prod_short](includes/prod_short.md)] niin, että huoltoteknikko voi luoda laskun kentällä, vaikka palvelua ei olisikaan liitetty sopimukseen tai tilaukseen. Vaihtoehtoisesti voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman niin, että laskutat huoltosopimukset jaksoittain. Kunkin sopimuksen laskutusjakso määrää, kuinka usein sopimus laskutetaan.

## Useiden huoltosopimusten laskuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo huoltosopimuslaskuja** ja valitse sitten vastaava linkki.  
2. Määritä käytettävät suodattimet.  
3. Anna **Kirjauspvm**-kenttään päivämäärä, jota haluat käyttää huoltolaskujen kirjauspäivämääränä.  
4. Anna **Lasku pvm:ään asti** -kenttään päivämäärä, johon asti haluat laskuttaa sopimuksia. Eräajoon sisällytetään sopimukset, joiden seuraava laskutuspäivämäärä on ennen tätä päivämäärää.  
5. Valitse **Toiminto**-kentässä **Luo laskut**.  
6. Luo huoltolaskut valitsemalla **OK**.  
  
Huoltosopimus voidaan laskuttaa myös suoraan **Huoltosopimus**-sivulta, jos sopimuksen seuraava laskutuspäivämäärä on aikaisempi kuin käsittelypäivämäärä.

## Huoltosopimuksen laskuttaminen Huoltosopimus -ikkunassa   
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.  
2. Valitse laskutettava huoltosopimus ja avaa sopimuksen kortti.  
3. Valitse **Luo huoltolasku** -toiminto. 
4. Luo huoltolaskut valitsemalla **Kyllä**.  
  
  > [!NOTE]  
  > Et voi luoda huoltosopimuksen huoltolaskuja, kun **Muuta tilaa** -kentän arvoksi on määritetty **Avoin**.  

## Kulutuksen kirjaaminen huoltotilauksesta  
Seuraavassa kuvataan, miten asiakkaalta veloitettava huollon osa määritetään.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse laskutettava huoltotilaus ja avaa tilauksen kortti.  
3. Valitse **Huoltorivit**-toiminto.  
4. Etsi tarvittavat tapahtumat ja määritä sitten **Laskutettava määrä** -kentässä määrät, jotka veloitat asiakkaalta.  
  
   > [!NOTE]  
   > Voit laskuttaa asiakasta rekisteröidystä palvelusta joko kokonaan tai osissa. Jos asiakkaalle halutaan lähettää lasku koko summasta, **Laskutettava määrä** -ja **Määrä**-kentän arvon on oltava sama. Voit lähettää koko laskun yhdessä koko lähetyksen kanssa ja voit kirjata täyden laskun jo aiemmin kirjatulle koko toimitukselle, jota ei ole laskutettu eikä käytetty viime aikoina.  
   >  
   > Voit määrittää laskun määrän kahdella eri tavalla, kun kirjaat osittaisen laskun. Jos aiot kirjata huollon **Toimitus- ja Lasku**-valinnan kanssa, **Laskutettava määrä** -kentän arvon on oltava sama kuin **Toimitettava määrä** -kentän arvo. Jos haluat laskuttaa aiemmin kirjatun toimituksen, laskun määrä ei saa olla suurempi kuin **Toimitettu määrä** -kentän arvo.  
  
5. Valitse ensin **Kirjaa** ja sitten joko **Lasku** tai **Toimitus ja lasku**. Lisätietoja näistä vaihtoehdoista on kohdassa [Kirjaaminen huoltohallinnassa](service-service-posting.md).  
  
 Valitsemasi huoltorivi kirjataan. Voit kirjata useita huoltorivejä kerralla valitsemalla ne kaikki ja valitsemalla **Kirjaus**. Jos teet näin, varmista, että olet täyttänyt kaikkien kirjattavien rivien tarvittavat tiedot.  
  
 Kun kirjaat tilauksen ilman **Lasku**-valintaa, ohjelma luo kirjatun huoltolaskun sekä vastaavat tapahtumat ja päivittää tilauksen huoltorivien kentät. Ohjelma päivittää myös aiemmin kirjatut toimitusasiakirjat laskutetuilla määrillä. Jos valitset **Toimitus ja lasku** -kirjausvalinnan, ohjelma luo myös kirjatun toimituksen.

## Huoltolaskun luominen manuaalisesti  
Tavallisesti kun kirjaat huoltotilauksen **Lasku**- tai **Toimitus ja lasku** -valinnan kanssa, ohjelma luo automaattisesti kirjatun huoltolaskun. Silti sinun on ehkä luotava lasku, jota ei ole linkitetty huoltosopimukseen tai huoltotilaukseen. Työvaiheessa kerrotaan, miten lasku luodaan, samalla kun asiakas vastaanottaa huollon.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltolasku.  
3. Syötä **Nro** -kentässä.  
  
    > [!NOTE]  
    >  Jos taas olet määrittänyt huoltolaskuille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit valita seuraavan saatavilla olevan laskunumeron <kbd>Enter</kbd>-näppäimellä.  
  
4. Syötä **Asiakasnro** -kentässä asiakkaan tunnus. Valitse asiamukainen asiakas luettelosta.  
  
    Ohjelma täyttää automaattisesti asiakkaaseen liittyvät kentät tiedoilla **Asiakas**-kortilta.  
  
5. Syötä päivämäärä **Kirjauspvm.**-kenttään. Tämä kenttä näkyy kirjatuissa tapahtumissa. Ohjelma täyttää tämän kentän nykyisellä käsittelypäivämäärällä, mutta sitä voi myös muuttaa manuaalisesti.  
6. Täytä **Asiakirjan pvm** -kenttä. Kenttään syöttämäsi päivämäärä näkyy tulostetussa laskussa, ja sen mukaan lasketaan myös eräpäivä.  
7. Täytä laskun huoltorivit. Rekisteröi huollossa käytetyt nimikkeet, resurssit ja/tai kustannukset täyttämällä **Tyyppi**-, **Nro**- ja **Määrä**-kenttä. 

## Voit luoda laskun, joka yhdistää kirjatut toimitusrivit yhdestä tai useammasta huoltotilauksesta 
Voit luoda huoltolaskun huollolle, joka on jo toimitettu (huoltotilauksista), mutta jota ei ole vielä laskutettu tai kulutettu. Ohjelma mahdollistaa tietyn asiakkaan laskurivien täyttämisen automaattisesti valituilla kirjatuilla toimitusriveillä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten vastaava linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Luo laskurivit toimituille huolloille, jota ei ole laskutettu. Vaihtoehtoisesti voit lisätä kirjatut toimitusrivit laskuun **Hae toimitusrivit** -toiminnolla.  
4. Kirjaa huoltolasku.  
  
 Kirjattu huoltolasku ja vastaavat tapahtumat luodaan. Ohjelma myös päivittää aiemmin kirjatut toimitusasiakirjat laskutetuilla määrillä ja lähdetilausten huoltorivien määrillä.  

## Uuden huollon hyvityslaskun luominen  
Huollon hyvityslaskuasiakirjaa käytetään yleensä silloin, kun asiakas palauttaa nimikkeen. Sitä voidaan kuitenkin käyttää myös silloin, kun asiakkaalle annetaan korvausta ja kun virheellinen lasku korjataan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon hyvityslaskut** ja valitse sitten vastaava linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Käsittelypäivämäärä näkyy **Kirjauspvm**- ja **Asiakirjapvm**-kentissä. Voit muuttaa sitä tarvittaessa.    
4. Syötä hyvityslaskun riveille tietoja nimikkeistä, jotka on palautettu tai poistettu tai asiakkaalle annettavasta korvauksesta.  

## Katso myös
[Huoltolaskujen kirjaaminen](service-how-to-post-service-orders.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huollon kirjaus](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]