---
title: Ostolaskun luominen ja ostojen kirjaaminen | Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten varastonimikkeitä ja muita kuin varastonimikkeitä tai resursseja ostetaan luomalla ja kirjaamalla ostolaskuja tai -tilauksia.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 845b552141f5637893bb0f0041b3247bce023c5f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758490"
---
# <a name="record-purchases"></a>Ostojen kirjaus
Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Jos haluat hallita varastoa, myös ostolaskuja ja -tilauksia käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, kuten palvelukulut, ja varastoarvot, jotka aiheutuvat ostolaskujen tai -tilausten kirjaamisesta, vaikuttavat tuottolukuihin ja muihin talouden KPI-arvoihin roolikeskuksessasi.

Varaston arvostukseen vaikuttavien fyysisten nimikkeiden (**Varasto**-nimiketyyppi) ostamisen lisäksi voit ostaa palveluita, jotka osoitetaan aikayksiköiden avulla. Voit tehdä tämän joko **Palvelu**-nimiketyypin tai **Resurssi**-rivityypin avulla.

> [!NOTE]  
> Ostotilauksia on käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), ostotilauksia on käytettävä. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut. Seuraava toimenpide perustuu ostolaskuun. Vaiheet ovat samankaltaisia ostotilaukselle.

Kun varastonimikkeitä vastaanotetaan tai ostettu palvelu on valmis, ostolasku tai -tilaus kirjataan varasto- ja taloustietueiden päivittämiseksi ja laskun aktivoimiseksi toimittajalle maksuehtojen mukaan. Lisätietoja on kohdissa [Ostojen kirjaaminen](ui-post-purchases.md) ja [Maksujen tekeminen](payables-make-payments.md).

> [!CAUTION]  
> Älä kirjaa ostolaskun fyysisiä nimikkeitä, ennen kuin vastaanotat nimikkeet ja tiedät oston lopullisen kustannuksen, mahdolliset lisäkustannukset mukaan lukien. Muussa tapauksessa varaston arvo ja voittoluvut voivat olla virheelliset.

Voit helposti korjata tai peruuttaa kirjatun ostolaskun ennen kuin maksua toimittajalle. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa. Lisätietoja on kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Jos olet jo maksanut kirjatun ostolaskun nimikkeet tai palvelut, sinun on luotava ostohyvityslasku oston peruuttamiseksi. Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** ja **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei säilytetä varastossa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md). Ostolaskuprosessi on sama kaikille kolmelle nimiketyypeille.

> [!NOTE]
> **Resurssi**-ostorivityypin avulla voit ostaa myös ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja on kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).<br /><br />
> Jos haluat käyttää ostettua resurssia, resurssin kapasiteetti on mahdollisesti määritettävä ja liitettävä manuaalisesti työhön. Resurssin ostaminen luo resurssitapahtuman. Resurssitapahtumia ei kuitenkaan seurata määrän ja arvon osalta kuten esimerkiksi nimikkeitä. Jos määrän ja arvon seuranta on pakollista, kannattaa harkita muiden rivinimiketyyppien käyttämistä.

Voit täyttää ostolaskun toimittajan kentät kahdella tavalla sen mukaan, onko toimittaja jo rekisteröity.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="to-create-a-purchase-invoice"></a>Ostolaskun kirjaamiseksi
Seuraavassa kerrotaan, miten ostolasku luodaan. Vaiheet ovat samankaltaisia ostotilaukselle. Tärkein ero on se, että ostotilauksilla on lisäkenttiä ja -toimintoja nimikkeiden fyysistä käsittelemistä varten.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.  
2. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.

    Muut **Ostolasku**-sivun kentät täytetään nyt valitun toimittajan vakiotiedoilla. Jos toimittajaa ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Toimittaja**-kenttään uuden toimittajan nimi.
4. Valitse uuden toimittajan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden toimittajan malli** -sivulla malli uuden toimittajakortin perusteella ja valitse sitten **OK**-painike.
6. Uuden toimittajan kortti avautuu esitäytettynä valitun toimittajamallin tiedoilla. **Nimi**-kenttään esitäytetään uuden toimittajan nimi, jonka syötit ostolaskulle.
7. Jatka täyttämällä toimittajan kortin jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien toimittajien rekisteröinti](purchasing-how-register-new-vendors.md).  
8. Kun olet määrittänyt toimittajakortin, valitse **OK**-painike palataksesi **Ostolasku**-sivulle.

    Useat kentät **Ostolasku** -sivulla täytetään tiedoilla, jotka olet määrittänyt uuden toimittajan kortissa.
9. Täytä tarvittaessa jäljellä olevat kentät **Ostolasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Voit nyt täyttää ostolaskurivit nimikkeillä tai resursseilla, joita olet ostanut toimittajalta.

    > [!NOTE]  
    >   Jos olet määrittänyt toimittajalle toistuvien ostojen rivin, kuten kuukausittaisen täydennystilauksen, voit lisätä nämä rivit laskuun valitsemalla **Hae toistuvat ostorivit** -toiminnon.
10. Syötä **Rivit**-pikavälilehden **Nimikenro**-kenttään varastonimikkeen tai palvelun numero.
11. Syötä **Määrä**-kenttään ostettavien nimikkeiden lukumäärä.

    > [!NOTE]  
    >   Jos nimikkeen tyyppi on **Palvelu** ja rivien tyyppi on **Resurssi**, määrä on aikayksikkö, kuten tunnit, rivin **Mittayksikön koodi** -kentän mukaisesti.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Välitön yksikkökustannus** -kentän arvo **Määrä**-kentän arvolla.

    Hinta ja rivin summa näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitsit **Hinnat verojen kanssa** -kenttään toimittajan kortissa.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

    > [!NOTE]
    > Kirjatut summat ovat harvoin erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon liittyvistä pyöristyslaskelmista.<br /><br />Voit tarkistaa kirjattavat summat käyttämällä **Tilastot**-sivua. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.

12. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään laskun alaosan **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    > [!NOTE]  
    >   Jos toimittajalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Toimittajan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma** -kenttään.
13. Kun vastaanotat ostettuja nimikkeitä tai palveluita, valitse **Kirjaa**.

Osto vaikuttaa nyt varastoon, resurssitapahtumiin ja taloustietueisiin, ja myyjän maksu on aktivoitu. Ostolasku poistetaan ostolaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen ostolaskujen luettelosta.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Resurssien määrittäminen](projects-how-setup-resources.md)  
[Ostojen kirjaaminen](ui-post-purchases.md)  
[Tarjousten pyytäminen](purchasing-how-request-quotes.md)  
[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Suoratoimitusten valmisteleminen](sales-how-drop-shipment.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]