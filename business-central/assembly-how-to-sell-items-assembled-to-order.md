---
title: Kokoonpano tilausta varten -nimikkeiden myyminen | Microsoft Docs
description: Jos kyse on kokoonpano tilausta varten -määritetystä nimikkeestä, nimikkeen ei odoteta olevan varastossa ja se on koottava myyntitilauksen mukaisesti. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan automaattisesti ja linkitetään myyntitilaukseen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92a1faa77132e4f26c1999411f6d8304c24dd8f7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772902"
---
# <a name="sell-items-assembled-to-order"></a>Kokoonpano tilausta varten -nimikkeiden myyminen
Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano tilausta varten** -kohdan, nimikettä ei oleteta olevan varastossa, vaan se on koottava myyntitilausta varten. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan automaattisesti ja linkitetään myyntitilaukseen.  

> [!NOTE]  
>  Jos kokoonpano tilausta varten -nimikkeet ovat jo varastossa, voit vähentää kokoonpanotilauksen määrää ja varata sen varastosta. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Tässä toimenpiteessä käsittelet asiakkaan pyytämien määrittelyjen mukaan koottavan nimikkeen myyntiä. Vaiheita ovat myyntitilausrivin käynnistäminen, kokoonpanonimikkeen mukauttaminen muokkaamalla sen osia ja resursseja, saatavuuden tarkistaminen toimituspäivämäärän määrittämiseksi ja myyntitilauksen vapauttaminen kokoonpanoa ja välitöntä toimitusta varten.  

> [!NOTE]  
>  Seuraavassa toimenpiteessä ei tehdä myyntitilauksen vakiovaiheita ennen, kuin koontitilausnimike syötetään myyntitilauksen riville.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Myy nimike, jok aon kokoonpano tilausta varten  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Luo myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3.  Valitse **Nro**-kenttään nimike, jolle on määritetty kokoonpano tilausta varten.  
4.  Määritä **Sijaintikoodi**-kentässä sijainti, josta nimike myydään. Kokoonpanoprosessi tapahtuu kyseisessä sijainnissa.  
5.  Määritä **Määrä**-kentässä, miten monta yksikköä haluat myytävän.  

    > [!NOTE]  
    >  Jos vähintään yksi pyydetyn kokoonpanon nimikkeen määrän komponenteista ei ole saatavana, näyttöön avautuu yksityiskohtaisia saatavuustietoja sisältävä varoitussivu. Lisätietoja on kohdassa Kokoonpanon saatavuus.  

    Kokoonpanotilaus luodaan nyt automaattisesti ja linkitetään myyntitilauksen riviin. Kokoonpanotilauksen eräpäivä synkronoidaan myyntitilausrivin lähetyspäivämäärän kanssa.  

    Myytävä määrä on kopioitu **Kokoonpantava määrä tilausta varten** -kentästä, joka ilmaisee, että nimikkeen asennus vaatii myyntirivillä olevan täyden määrän kokoonpanon tilausta varten. Voit vähentää kokoonpano tilausta varten -määrää, jos tiedät, että jotkin osat ovat jo saatavilla. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Jos asiakas haluaa tuotepakettiin lisänimikkeen, valitse **Rivit** -pikavälilehdessä ensin **Rivi**-toiminto, sitten **Kokoonpano tilausta varten** -toiminto ja lopuksi **Kokoonpano tilausta varten -rivit** -toiminnon. Voit nyt tarkastella ja muuta vakiokokoonpanon komponentteja. Voit myös valita **Kokoonpantava määrä tilausta varten** -kentän.  
7.  Luo **Kokoonpano tilausta varten -rivit** -sivulla pyydettyä lisäkokoonpanosisältöä varten uusi rivi, jonka tyyppi on **Nimike**. Rivi vastaa ylimääräistä kokoonpano-osaa.  

    Voit myös mukauttaa tilauksen kasvattamalla yhden perusnimikkeen paketin määrää. Voit tehdä tämän lisäämällä arvon **Määrä per** -kentässä tietylle kokoonpanon tilausriville.  

    > [!NOTE]  
    >  **Kokoonpano tilausta varten -rivit** -sivulla näytetään vain perustietokentät, joita myyjän on tarkoitus käyttää osaluettelon mukauttamiseen, nimikkeen seurantanumeroiden lisäämiseen tai osien saatavuuden ongelmanratkaisuun. Katso lisää kokoonpanotilauksen tietoja, kuten kokoonpanotilauksen aloituspäivämäärä, valitsemalla **Näytä asiakirjat**. Tämä avaa myyntitilausriviin linkitetyn kokoonpanotilauksen koko näkymän. Et voi muuttaa useimpien kenttien sisältöä kokoonpanotilauksen otsikossa, etkä voi kirjata kokoonpanon tuotosta siitä, koska koska sinun täytyy käyttää myyntitilausrivin tilauksen kirjausta.  
    >   
    >  Linkitettyjen kokoonpanotilausten otsikossa vain **Aloituspvm**-kenttää voidaan muuttaa niin, että kokoonpanotyöntekijät voivat määrittää päivämäärän, joka on ennen eräpäivää, kun he aloittavat prosessin. Linkitetyn kokoonpanotilauksen rivien kaikki kentät voidaan muuttaa siten, että varaston työntekijät voivat syöttää kulutuksen lukuja prosessin aikana.  

8.  Tarkista tai reagoi komponenttien saatavuusongelmiin. Valitse esimerkiksi saatavilla oleva korvaava nimike tai määritä myöhempi eräpäivä.  
9. Sulje **Kokoonpano tilausta varten -rivit** -sivu. Linkitetty kokoonpanotilaus on nyt valmiina mukautettujen nimikkeiden kokoonpanon aloittamiseen eräpäivään mennessä.  
10. Valitse myyntitilauksessa **Vapauta**-toiminto, jos haluat ilmoittaa kokoonpano-osastolle, että kokoonpanoprosessi voidaan aloittaa.  
11. Suorita kokoonpanoosastossa niiden nimikkeiden kokoamisvaiheet, jotka myydään tässä käsittelyssä. Lisätietoja on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]