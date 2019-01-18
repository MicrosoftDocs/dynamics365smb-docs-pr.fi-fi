---
title: "Maksujen vienti sähköiseen maksutiedostoon| Microsoft Docs"
description: "Voit tehdä toimittajamaksuja ottamalla käyttöön pankkitietojen muuntopalvelun, viemällä pankkitiedoston ja lataamalla tiedoston sähköiselle pankkitilille varojen siirtoa varten."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 14015c089e3cd6db19a12fe4eed72d523f3aefc5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="export-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon
Kun olet valmis suorittamaan maksut toimittajille tai hyvitykset työntekijöille, voit viedä tiedoston ja päiväkirjan rivien maksutiedot **Maksupäiväkirja**-sivulla. Voit sitten ladata tiedoston pankkiin kyseisten rahansiirtojen käsittelyä varten.

[!INCLUDE[d365fin](includes/d365fin_md.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjoisamerikkalaisessa versioissa maksutiedostot voidaan lähettää samalla palvelulla sähköisenä rahansiirtona, joskin prosessi on hieman erilainen. Lisätietoja on Maksujen vienti pankkitiedostoon -osan vaiheessa 6.    

> [!NOTE]  
>   Määritä liittyvän pankkitilin sähköinen muoto ennen maksutiedostojen vientiä maksupäiväkirjasta ja ota pankkitietojen muuntopalvelu käyttöön. Lisätietoja on kohdissa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md) ja [Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md). Valitse myös **Salli maksun vienti** -valintaruutu **Yleisen päiväkirjan erät** -sivulla. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

Voit tarkastella maksupäiväkirjasta vietyjä maksutiedostoja **Hyvityksen siirron rekisterit** -sivulla. Voit myös viedä sivulla maksutiedostot uudelleen, jos tekniset virheet tai tiedostomuutokset vaativat sitä. Huomaa kuitenkin, että viedyt sähköiset rahansiirtotiedostot eivät näy tällä sivulla eikä niitä voi viedä uudelleen.  

## <a name="to-export-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon
Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä. Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Täytä maksupäiväkirjan rivit. Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Jos käytät sähköistä rahansiirtoa, sinun on valittava joko **Sähköinen maksu** tai **Sähköinen maksu – IAT** **Pankkimaksun tyyppi** -kentässä. Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti**- ja **Toimittajan pankkitilin kortti** -sivuilla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.

3. Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Vie**-toiminto.
4. Täytä **Vie sähköiset maksut** -sivun kentät tarpeen mukaan.

    Virheilmoituksia näkyy **Maksutiedoston virheet** -tietoruudussa, jossa voit myös nähdä yksityiskohtaiset tiedot virheviestistä. Kaikki virheet on ratkaistava ennen maksutiedoston vientiä.

    > [!TIP]  
    >   Pankkitietojen muuntopalvelua käytettäessä yleinen virheilmoitus kertoo, että pankkitilin numeron pituus ei täytä pankin vaatimuksia. Voit välttää tämän virheen tai ratkaista sen poistamalla **IBAN**-kentän **Pankkitilin kortti** -sivulla ja antamalla sitten pankkitilin numeron **Pankkitilin nro** -kentässä pankin edellyttämässä muodossa.

5. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

    > [!NOTE]  
    >   Jos käytät sähköistä rahansiirtoa, tallenna saatava toimittajan maksusuorituslomake Word-asiakirjana tai valitse sen lähettäminen suoraan toimittajalle. Maksut on nyt lisätty **Luo sähköinen rahansiirtotiedosto** -sivulle, jossa voit luoda samanaikaisesti useita maksutilauksia, mikä säästää lähetyskustannuksia. Lisätietoja on seuraavissa vaiheissa:
6. Valitse **Maksupäiväkirja**-sivulla **Luo sähköinen rahansiirtotiedosto** -toiminto.

    **Luo sähköinen rahansiirtotiedosto** -sivulla kaikki sähköistä rahansiirtoa varten määritetyt maksut, jotka on viety maksupäiväkirjasta määritetylle pankkitilille mutta joita ei ole vielä muodostettu, on mainittu **Rivit**-pikavälilehdessä.
7. Vie kaikki sähköiset rahansiirtomaksut sisältävä tiedosto valitsemalla **Luo sähköinen rahansiirtotiedosto** -toiminto.
8. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

Pankin maksutiedosto viedään määrittämääsi sijaintiin ja voit jatkaa sen lataamista verkkopankkitilille ja suorittaa todelliset maksut. Voit sitten kirjata viedyn maksupäiväkirjan rivit.

## <a name="to-plan-when-to-post-exported-payments"></a>Vietyjen maksujen kirjaamisajankohdan suunnitteleminen
Jos et halua kirjata viedyn maksun maksupäiväkirjan riviä, koska esimerkiksi odotat pankin vahvistusta tapahtuman käsittelystä, voit poistaa päiväkirjan rivin. Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety. Lisäksi saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen, joka avaa vietyjen maksutiedostojen tiedot.

Jos noudatat prosessia, jossa maksut kirjataan vasta sen jälkeen, kun pankin suorittamasta maksujen käsittelystä on saatu vahvistus, voit hallita tätä kahdella eri tavalla.

* Maksupäiväkirjan ehdotettujen maksurivien kohdalla voit lajitella joko **Viety maksutiedostoon** -sarakkeen tai **Viety summa yhteensä**-kentän mukaan ja sitten poistaa maksuehdotukset avoimilta laskuilta, jotka on jo maksettu ja joita et halua maksaa.
* Voit valita **Ehdota toimittajamaksuja** -sivulla, jossa määrität maksupäiväkirjaan lisättävät maksut, **Ohita viedyt maksut** -valintaruudun, jos et halua lisätä päiväkirjarivejä jo viedyille maksuille.

Saat lisätietoja viedyistä maksuista valitsemalla **Maksujen vientihistoria** -toiminnon.

## <a name="to-re-export-payments-to-a-bank-file"></a>Maksujen vieminen uudelleen pankkitiedostoon
Voit viedä maksutiedostot uudelleen **Hyvityksen siirron rekisterit** -sivulla. Ennen kuin poistat tai kirjaat maksupäiväkirjan rivejä, voit myös viedä maksutiedoston uudelleen **Maksupäiväkirja**-sivulla yksinkertaisesti viemällä sen uudelleen. Jos olet poistanut tai kirjannut maksupäiväkirjan rivit viennin jälkeen, voit viedä saman maksutiedoston uudelleen **Hyvityksen siirron rekisterit** -sivulla. Valitse rivi tilisiirtojen erälle, jonka haluat viedä uudelleen, ja käyttämällä sitten **Vie maksut uudelleen tiedostoon** -toimintoa.

> [!NOTE]  
>   Viedyt sähköiset rahansiirtotiedostot eivät näy **Hyvityksen siirron rekisterit** -sivulla, eikä niitä voi viedä uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Hyvityksen siirron rekisterit** ja valitse sitten liittyvä linkki.
2. Valitse ensin uudelleenvietävä maksun vienti ja sitten **Vie maksut uudelleen tiedostoon** -toiminto.

## <a name="see-also"></a>Katso myös
[Maksujen suorittaminen](payables-make-payments.md)  
[Ostovelat](payables-manage-payables.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

