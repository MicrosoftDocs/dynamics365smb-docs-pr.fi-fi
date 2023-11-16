---
title: Kokoonpanon kirjauksen kumoaminen
description: Tietoja kirjatussa kokoonpanotilauksissa olevien virheiden korjaamisesta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="undo-assembly-posting"></a>Kokoonpanon kirjauksen kumoaminen

Korjaa virhe kumoamalla kokoonpanotilauksen kirjaus tai poista ei-toivottu kirjaus.

Kirjattua kokoonpanotilausta kumotessa alkuperäisille nimiketapahtumille luodaan korjaavat vastakirjaukset. Kokoonpanonimikkeen kukin positiivinen kulutustapahtuma kumotaan negatiivisella kulutustapahtumalla. Kokoonpano-osan kukin negatiivinen kulutustapahtuma kumotaan positiivisella kulutustapahtumalla. Kiinteiden kustannusten kohdistaminen luodaan korjaavien ja alkuperäisten tapahtumien välille automaattisesti. Näin varmistetaan todellisten kustannusten peruuttaminen.  

Täysin kirjattua kokoonpanotilausta kumottaessa alkuperäinen tilaus voidaan luoda uudelleen. Tällä tavoin korjaukset voidaan sitten tehdä, ennen kuin se kirjataan uudelleen.  

Osittain kirjattua kokoonpanotilausta kumottaessa kaikki määräkentät, kuten **Kokoonpantu määrä**, **Kulutettu määrä** ja **Jäljellä oleva määrä**, palautetaan arvoihin, jotka niissä oli ennen kirjausta.  

Kokoonpanotilausten luominen uudelleen tai niiden palauttaminen edellyttää, että alkuperäisen kirjauksen nimike täyttää seuraavat ehdot:  

* Nimike on edelleen varastossa. Sitä ei siis saa olla myyty eikä muuten kulutettu lähtevissä tapahtumissa.  
* Nimikettä ei ole varattu.  
* Se on varastopaikassa, johon se on alun perin asetettiin.  

Kokoonpanotilaukset voidaan palauttaa vain, jos alkuperäisen kokoonpanotilauksen rivien määrää ja järjestystä ei ole muutettu.  

> [!TIP]  
> Riveillä tapahtuneiden muutosten aiheuttamat ristiriidat ratkaistaan palauttamalla kyseiset rivimuutokset manuaalisesti ennen kirjatun kokoonpanotilauksen kumoamista. Kokoonpanotilaus voidaan kirjata ja luoda se sitten uudelleen, kun kirjaus kumotaan.  

Seuraavassa ohjeessa neuvotaan, miten kumotaan varastoon kokoonpantuja nimikkeitä sisältävät kirjatut kokoonpanotilaukset. Jos kumottavissa kirjatuissa kokoonpanotilauksissa on tilausta varten kokoonpantuja nimikkeitä, liittyvissä kirjatussa toimituksessa käytetään **Peruuta toimitus** -toimintoa. Lisätietoja toimitusten peruuttamisesta on kohdassa [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md). Kirjattu kokoonpanotilaus kumotaan siten tässä artikkelissa kuvatulla tavalla.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Kumoa kokoonpanotilauksen kirjaus

Kokonaan tai osittain kirjatut kokoonpanotilaukset voidaan kumota.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut kokoonpanotilaukset** ja valitse sitten vastaava linkki.  

   Jokainen osittainen kirjaus luo erillisen kirjatun kokoonpanotilauksen.  
2. Avaa kumottava kirjattu kokoonpanotilaus ja valitse sitten **Kumoa kokoonpano** -toiminto.  

    Jos kirjattu kokoonpanotilaus liittyy poistettuun, täysin kirjattuun kokoonpanotilaukseen, tilaus voidaan ensin luoda uudelleen ja sitten poistaa. Tilaus saatetaan luoda uudelleen esimerkiksi siksi, että se halutaan käsitellä uudelleen.  
3. Kokoonpanotilaus luodaan uudelleen valitsemalla **Kyllä**. Kirjaus kumotaan luomatta kokoonpanotilausta uudelleen valitsemalla **Ei**.  

Kokoonpanotilauksen **Peruutettu**-otsikkokentän arvoksi muuttuu **Kyllä**. Kokoonpanotilauksen kirjaus on nyt peruutettu. Jos kokoonpanotilaus päätetään luoda uudelleen, koko tilaus voidaan käsitellä. Vaihtoehtoisesti alkuperäiseen tilaan palautettu kokoonpanotilaus voidaan avata.  

> [!NOTE]  
> Jos määrät halutaan palauttaa kokoonpanotilauksessa, jossa on tehty useita osittaisia kirjauksia, kaikki kirjatut kokoonpanotilaukset on kumottava vaiheiden 1–3 mukaisesti.  

## <a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md)  
[Myynnin palautusten tai peruutusten käsittely](sales-how-process-sales-returns-cancellations.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
