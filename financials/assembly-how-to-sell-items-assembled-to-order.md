---
title: Kokoonpano tilausta varten -nimikkeiden myyminen | Microsoft Docs
description: "Jos kyse on kokoonpano tilausta varten -määritetystä nimikkeestä, nimikkeen ei odoteta olevan varastossa ja se on koottava myyntitilauksen mukaisesti. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan automaattisesti ja linkitetään myyntitilaukseen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 74822d77b45f0ba1aaf8b255f611a54d051c1f52
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-sell-items-assembled-to-order"></a>Kokoonpano tilausta varten -nimikkeiden myyminen
Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano tilausta varten** -kohdan, nimikettä ei oleteta olevan varastossa, vaan se on koottava myyntitilausta varten. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan automaattisesti ja linkitetään myyntitilaukseen.  

> [!NOTE]  
>  Jos kokoonpano tilausta varten -nimikkeet ovat jo varastossa, voit vähentää kokoonpanotilauksen määrää ja varata sen varastosta. Lisätietoja on kohdassa [Toimintaohje: Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Tässä toimenpiteessä käsittelet asiakkaan pyytämien määrittelyjen mukaan koottavan nimikkeen myyntiä. Vaiheita ovat myyntitilausrivin käynnistäminen, kokoonpanonimikkeen mukauttaminen muokkaamalla sen osia ja resursseja, saatavuuden tarkistaminen toimituspäivämäärän määrittämiseksi ja myyntitilauksen vapauttaminen kokoonpanoa ja välitöntä toimitusta varten.  

> [!NOTE]  
>  Seuraavassa toimenpiteessä ei tehdä myyntitilauksen vakiovaiheita ennen, kuin koontitilausnimike syötetään myyntitilauksen riville.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Myy nimike, jok aon kokoonpano tilausta varten  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo myyntitilaus. Lisätietoja on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md).  
3.  Valitse **Nro**-kenttään nimike, jolle on määritetty kokoonpano tilausta varten.  
4.  Määritä **Sijaintikoodi**-kentässä sijainti, josta nimike myydään. Kokoonpanoprosessi tapahtuu kyseisessä sijainnissa.  
5.  Määritä **Quantity**-kentässä, miten monta yksikköä haluat myytävän.  

    > [!NOTE]  
    >  Jos vähintään yksi pyydetyn kokoonpanon nimikkeen määrän komponenteista ei ole saatavana, näyttöön avautuu yksityiskohtaisia saatavuustietoja sisältävä varoitusikkuna. Lisätietoja on kohdassa Kokoonpanon saatavuus.  

    Kokoonpanotilaus luodaan nyt automaattisesti ja linkitetään myyntitilauksen riviin. Kokoonpanotilauksen eräpäivä synkronoidaan myyntitilausrivin lähetyspäivämäärän kanssa.  

    Myytävä määrä on kopioitu **Kokoonpantava määrä tilausta varten** -kentästä, joka ilmaisee, että nimikkeen asennus vaatii myyntirivillä olevan täyden määrän kokoonpanon tilausta varten. Voit vähentää kokoonpano tilausta varten -määrää, jos tiedät, että jotkin osat ovat jo saatavilla. Lisätietoja on kohdassa [Toimintaohje: Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa.](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  

6.  Jos asiakas haluaa tuotepakettiin lisänimikkeen, valitse **Rivit** -pikavälilehdessä ensin **Rivi**-toiminto, sitten **Kokoonpano tilausta varten** -toiminto ja lopuksi **Kokoonpano tilausta varten -rivit** -toiminnon. Voit nyt tarkastella ja muuta vakiokokoonpanon komponentteja. Voit myös valita **Kokoonpantava määrä tilausta varten** -kentän.  
7.  Luo **Kokoonpano tilausta varten -rivit** -ikkunassa pyydettyä lisäkokoonpanoisisältöä varten uusi rivi, jonka tyyppi on **Nimike**. Rivi vastaa ylimääräistä kokoonpano-osaa.  

    Voit myös mukauttaa tilauksen kasvattamalla yhden perusnimikkeen paketin määrää. Voit tehdä tämän lisäämällä arvon **Määrä per** -kentässä tietylle kokoonpanon tilausriville.  

    > [!NOTE]  
    >  **Kokoonpano tilausta varten -rivit** -ikkunassa näytetään vain perustietokentät, joita myyjän on tarkoitus käyttää osaluettelon mukauttamiseen, nimikkeen seurantanumeroiden lisäämiseen tai osien saatavuuden ongelmanratkaisuun. Katso lisää kokoonpanotilauksen tietoja, kuten kokoonpanotilauksen aloituspäivämäärä **Koti** -välilehdessä **Prosessi** -ryhmässä valitsemalla **Näytä asiakirjat**. Tämä avaa myyntitilausriviin linkitetyn kokoonpanotilauksen koko näkymän. Et voi muuttaa useimpien kenttien sisältöä kokoonpanotilauksen otsikossa, etkä voi kirjata kokoonpanon tuotosta siitä, koska koska sinun täytyy käyttää myyntitilausrivin tilauksen kirjausta.  
    >   
    >  Linkitettyjen kokoonpanotilausten otsikossa vain **Aloituspvm**-kenttää voidaan muuttaa niin, että kokoonpanotyöntekijät voivat määrittää päivämäärän, joka on ennen eräpäivää, kun he aloittavat prosessin. Linkitetyn kokoonpanotilauksen rivien kaikki kentät voidaan muuttaa siten, että varaston työntekijät voivat syöttää kulutuksen lukuja prosessin aikana.  

8.  Tarkista tai reagoi komponenttien saatavuusongelmiin. Valitse esimerkiksi saatavilla oleva korvaava nimike tai määritä myöhempi eräpäivä.  
9. Sulje **Kokoonpano tilausta varten -rivit** -ikkuna. Linkitetty kokoonpanotilaus on nyt valmiina mukautettujen nimikkeiden kokoonpanon aloittamiseen eräpäivään mennessä.  
10. Valitse myyntitilauksessa **Vapauta**-toiminto, jos haluat ilmoittaa kokoonpano-osastolle, että kokoonpanoprosessi voidaan aloittaa.  
11. Suorita kokoonpanoosastossa niiden nimikkeiden kokoamisvaiheet, jotka myydään tässä käsittelyssä. Lisätietoja on kohdassa [Toimintaohje: Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Toimintaohje: Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

