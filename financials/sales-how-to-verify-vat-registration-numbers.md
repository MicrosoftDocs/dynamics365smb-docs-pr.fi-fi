---
title: "ALV-rekisteröintinumeroiden tarkistaminen | Microsoft Docs"
description: "EU:n web-palvelun avulla voit varmistaa, että ALV-rekisteröintinumerot, jotka syötät asiakas-, toimittaja- tai kontaktikortteihin, ovat voimassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Toimintaohje: ALV-rekisteröintinumeroiden tarkistaminen
EU:n verkkopalvelun avulla voit varmistaa, että asiakas-, toimittaja- tai kontaktikortteissa annettavat ALV-rekisteröintinumerot ovat voimassa.  

 Kun muokkaat **ALV-rekisterinro**-kenttää kortissa, jonka **Maa-/aluekoodi**-kentän arvona on EU-maa tai -alue, uusi ALV-rekisteröintinumero ja käyttäjätunnuksesi kirjataan **ALV-rekisteröintiloki**-ikkunaan. Voit tarkistaa ALV-numeron valitsemalla **Tarkista ALV-numero** -painikkeen **ALV-rekisteröintiloki**-ikkunassa. Uusi rivi luodaan aina, kun käytät tarkistustoimintoa. Jos numero on voitu vahvistaa, **Tila**-kentän arvona on **Kelvollinen**. Jos numeroa ei voitu vahvistaa, **Tila**-kentän arvona on **Virheellinen** ja sinun on muutettava numeroa kortin **ALV-rekisteröintinumero**-kentässä sekä käynnistää vahvistaminen uudelleen.  

 Oletusarvoisen web-palvelun URL-osoite on määritetty **ALV-numeron tarkistus-URL** -kenttään **Pääkirjanpidon asetukset** -ikkunassa.  

 Voit muuttaa **ALV-rekisterinron muoto** -taulukossa kullekin maalle tai alueelle sellaiset ALV-rekisteröintinumeron muodot, jotka käyttäjä saa antaa **ALV-rekisterinro**-kenttään.  

> [!WARNING]  
>  Tämä web-palvelu käyttää http-protokollaa, mikä tarkoittaa sitä, että palvelun kautta siirretyt tiedot eivät ole salattuja.  

> [!NOTE]  
>  Tämä palvelu saattaa ajoittain olla poissa käytöstä, koska palvelu on osa EU:n laajaa kansallisten ALV-rekistereiden verkostoa. Microsoft ei ole vastuussa palvelun käytettävyydestä.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>ALV-rekisteröintinumeron tarkistaminen asiakaskortista  
Seuraavaksi käsitellään asiakkaan ALV-rekisterinumeron tarkistaminen. Vaiheet ovat samankaltaisia toimittajalle ja kontaktille.   
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.  

2.  Avaa sen asiakkaan kortti, jonka ALV-rekisteröintinumeron haluat tarkistaa.  

    > [!NOTE]  
    >  Asiakaskortin **Maa-/aluekoodi**-kentässä on oltava EU-maa tai -alue.  
3.  Valitse **Laskutus**-pikavälilehdessä Siirtyminen-painike **ALV-rekisterinro** -kentän vierestä.  

    **ALV-rekisteröintiloki** -ikkuna avautuu näyttäen yhden rivin, jossa **Tila**-kentän arvona on **Tarkistamaton**.  
4.  Valitse **Tarkista rekisterinro** -toiminto.  

     Uusi rivi luodaan, kun **Tila**-kentän arvona on joko **kelvollinen** tai **virheellinen**.  
5.  Jos **Tila**-kentän arvona on **Virheellinen**, vaihda numero kortin **ALV-rekisterinro**-kentässä ja toista vaiheet 3 ja 4.  

## <a name="see-also"></a>Katso myös  
[Rahoitus](finance.md)  
[Toimintaohje: Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)  
[Toimintaohje: Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

