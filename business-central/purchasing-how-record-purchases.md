---
title: Ostojen kirjaaminen ostolaskujen avulla (sisältää videon)
description: Tässä artikkelissa kerrotaan, miten varastonimikkeitä ja muita kuin varastonimikkeitä tai resursseja ostetaan luomalla ja kirjaamalla ostolaskuja tai -tilauksia.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: e6f918a33b81ab7986fd0f2ec6bddb9dcc62fcc3
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460830"
---
# <a name="record-purchases-with-purchase-invoices"></a>Ostojen kirjaaminen ostolaskujen avulla

Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Ostolaskuja ja -tilauksia käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, kuten palvelukulut, ja varastoarvot, jotka aiheutuvat ostolaskujen tai -tilausten kirjaamisesta, vaikuttavat tuottolukuihin ja muihin talouden suorituskykyilmaisimiin (KPI) roolikeskuksessasi.

## <a name="create-purchase-invoices"></a>Luo ostolaskuja

Varaston arvostukseen vaikuttavien fyysisten nimikkeiden (**Varasto**-nimiketyyppi) ostamisen lisäksi voit ostaa palveluita, jotka osoitetaan aikayksiköiden avulla. Voit tehdä tämän joko **Palvelu**-nimiketyypin tai **Resurssi**-rivityypin avulla.

Kun varastonimikkeitä vastaanotetaan tai ostettu palvelu on valmis, ostolasku tai -tilaus kirjataan varasto- ja taloustietueiden päivittämiseksi ja laskun aktivoimiseksi toimittajalle maksuehtojen mukaan. Lisä tietoja on kohdissa [ostosten kirjaaminen](ui-post-purchases.md), [nimikkeiden vastaanotto](warehouse-how-receive-items.md) ja [maksujen tekeminen](payables-make-payments.md).

> [!CAUTION]  
> Älä kirjaa ostolaskun fyysisiä nimikkeitä, ennen kuin vastaanotat nimikkeet ja tiedät oston lopullisen kustannuksen, mahdolliset lisäkustannukset mukaan lukien. Muussa tapauksessa varaston arvo ja voittoluvut voivat olla virheelliset.

### <a name="create-a-purchase-invoice"></a>Luo ostolasku

Seuraavassa kerrotaan, miten ostolasku luodaan. Vaiheet ovat samankaltaisia ostotilaukselle. Tärkein ero on se, että ostotilauksilla on lisäkenttiä ja -toimintoja nimikkeiden fyysistä käsittelemistä varten.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut**, valitse sitten vastaava linkki.  
2. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.

    Muut **Ostolasku**-sivun kentät täytetään nyt valitun toimittajan vakiotiedoilla. Jos toimittajaa ei ole rekisteröity, toimi seuraavasti:

    1. Syötä **Toimittaja**-kenttään uuden toimittajan nimi.
    2. Valitse uuden toimittajan rekisteröimisen valintaikkunassa **Kyllä**.
    3. Lue lisätietoja toimittajan kortin täyttämisestä kohdasta [Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md).  
    4. Kun olet määrittänyt toimittajakortin, valitse **OK** palataksesi **Ostolasku**-sivulle.

3. Täytä tarvittaessa jäljellä olevat kentät **Ostolasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Voit nyt täyttää ostolaskurivit nimikkeillä tai resursseilla, joita olet ostanut toimittajalta.

    > [!NOTE]  
    > Jos olet määrittänyt toimittajalle toistuvien ostojen rivin, kuten kuukausittaisen täydennystilauksen, voit lisätä nämä rivit laskuun valitsemalla **Hae toistuvat ostorivit** -toiminnon.
4. Syötä **Rivit**-pikavälilehden **Nimikenro**-kenttään varastonimikkeen tai palvelun numero.
5. Syötä **Määrä**-kenttään ostettavien nimikkeiden lukumäärä.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Välitön yksikkökustannus** -kentän arvo **Määrä**-kentän arvolla.

    Hinta ja rivin summa näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitsit **Hinnat verojen kanssa** -kenttään toimittajan kortissa.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

6. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään laskun alaosan **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    > [!NOTE]  
    > Jos toimittajalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Toimittajalaskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa syötetään **Laskun alennussumma** -kenttään.
7. Kun vastaanotat ostettuja nimikkeitä tai palveluita, valitse **Kirjaa**.

Osto vaikuttaa nyt varastoon, resurssitapahtumiin ja taloustietueisiin, ja myyjän maksu on aktivoitu. Ostolasku poistetaan ostolaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen ostolaskujen luettelosta.  

> [!NOTE]
> Kirjatut summat ovat harvoin erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon (ALV) liittyvistä pyöristyslaskelmista.
>
> Voit tarkistaa kirjattavat summat menemällä **Tilastotiedot**-sivulle. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.

## <a name="when-to-use-purchase-orders"></a>Ostotilausten käyttö

Ostotilauksia on käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä. Jos toimitat nimekkeitä suoraan toimittajalta asiakkaalle suoratoimituksena, ostotilauksia on käytettävä. Lisätietoja on kohdassa [Tee suoratoimituksia](sales-how-drop-shipment.md).

Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut. Seuraava toimenpide perustuu ostolaskuun. Vaiheet ovat samankaltaisia ostotilaukselle.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="purchasing-non-inventory-items"></a>Muiden kuin varastonimikkeiden osto

Ostolaskun rivejä voivat olla **Resurssi**- tai **Nimike**-tyyppiä. Tuotekortit voidaan luokitella edelleen **varasto**-, **palvelu**- tai **ei-varasto**-tyyppiin, mikä määrittää, onko tuote fyysinen varastoyksikkö, työaikayksikkö (koskee myös resursseja) vai fyysinen yksikkö, jota ei säilytetä inventaarioon. Lisätietoja on kohdassa [Uusien nimikkeiden rekisteröinti](inventory-how-register-new-items.md). Ostolaskuprosessi on sama kaikille mainituille nimiketyypeille.

> [!NOTE]
> **Resurssi**-ostorivityypin avulla voit ostaa myös ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).
>
> Jos haluat käyttää ostettua resurssia, resurssin kapasiteetti on mahdollisesti määritettävä ja liitettävä manuaalisesti työhön. Resurssin ostaminen luo resurssitapahtuman. Resurssitapahtumia ei kuitenkaan seurata määrän ja arvon osalta kuten esimerkiksi nimikkeitä. Jos määrän ja arvon seuranta on pakollista, kannattaa harkita muiden rivinimiketyyppien käyttämistä.

## <a name="posted-invoices"></a>Kirjatut laskut

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Voit helposti korjata tai peruuttaa kirjatun ostolaskun ennen kuin maksua toimittajalle. Tästä on hyötyä, jos sinun täytyy korjata kirjoitusvirhe tai muuttaa ostoa tilausprosessin alkuvaiheessa. Lisätietoja kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Jos olet jo maksanut kirjatun ostolaskun nimikkeet tai palvelut, sinun on luotava ostohyvityslasku oston peruuttamiseksi. Lisätietoja kohdassa [Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md).

[Avaa **Kirjatut ostolaskut** -luettelo](https://businesscentral.dynamics.com/?page=146) [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa.

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/processing-invoices-dynamics-365-business-central/index).

## <a name="see-also"></a>Katso myös

[Ostojen kirjaaminen](ui-post-purchases.md)  
[Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md)  
[Tarjousten pyytäminen](purchasing-how-request-quotes.md)  
[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md)  
[Suoratoimitusten valmisteleminen](sales-how-drop-shipment.md)  
[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Resurssien määrittäminen](projects-how-setup-resources.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
