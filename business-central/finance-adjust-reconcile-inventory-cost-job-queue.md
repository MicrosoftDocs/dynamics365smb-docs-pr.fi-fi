---
title: Ajoita työt varaston kustannusten täsmäytystä ja oikaisua varten
description: Lisätietoja siitä, miten voit siirtää työjonon avulla tehtäviä, jotka liittyvät varaston kustannusten säätämiseen tai sen täsmäyttämisessä taustalla KP:n kanssa. Esimerkiksi jos yrityksesi suorittaa useita tehtäviä tai käsittelee useita tapahtumia.
author: AndreiPanko
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: 461
ms.date: 09/23/2021
ms.author: andreipa
ms.openlocfilehash: 4dda49e125445ab754ce63dc6b2fc530ca59fcc4
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516976"
---
# <a name="schedule-jobs-for-adjusting-and-reconciling-inventory-cost-with-the-general-ledger"></a>Ajoita työt varaston kustannusten täsmäytystä ja oikaisua varten pääkirjanpitoon.

Jos haluat optimoida käyttökokemuksen, automaattinen kustannusten muuttaminen ja kirjaaminen pääkirjanpitoon ovat käytössä oletusarvoisesti. Tiedot kuitenkin kerääntyvät ajan mittaan, mikä saattaa vaikuttaa suorituskykyyn. Sovelluksen kuormituksen vähentämiseksi on usein hyödyllistä käyttää työjonotapahtumia, kun haluat siirtää tehtäviä suoritettavaksi taustalla.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Siirrä nimikekustannusten säätämisen tehtävä taustalle ohjatun määrityksen avulla

Työjonotapahtumien luominen voi olla hankalaa myös kokeneelle konsultille, joten meillä on avusteinen käyttöönotto-opas, joka helpottaa prosessia nimikekustannusten muuttamiseksi.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.  
2. Vaihda **Varaston asetukset** -sivulla **Automaattinen kustannusten kirjaus** -kentän arvo tai määritä **Ei koskaan** **Automaattinen kustannusten muuttaminen** -kentässä.  
3. Valitse sivun yläosassa olevassa ilmoituksessa **Ajoita työjonotapahtuma** -linkki. Tämä avaa ohjatun **Ajoita kustannusten täsmäytys ja oikaisu** -määritysoppaan.  
4. Määritä ajoitettava tehtävä.  

  > [!NOTE]
  > Et voi luoda uutta työjonotapahtumaa, jos määritetyn tehtävän työjonotapahtuma on jo olemassa.

5. Valitse **Näytä työjonotapahtumat, kun valmis** -kenttä ja tarkista ja säädä asetukset. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Työjonotapahtuman luominen varaston kustannusten manuaalista säätöä ja täsmäyttämistä varten

Vaihtoehtoisesti voit luoda työjonotapahtumia manuaalisesti. Seuraavassa kuvataan , miten **Muuta kustann. - Nimiketapaht.** -eräajo asetetaan suoritettavaksi automaattisesti päivittäin, mutta samat työvaiheet koskevat **Kirjaa varaston kust. KP:oon** -eräajoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työjonotapahtumat** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Suoritettavan objektin tyyppi** -kentässä *Raportti*.  
4. Valitse **Suoritettavan objektin tunnus** -kentässä *795*, **Muuta kustann. - Nimiketapaht.**.  
5. Syötä **Seuraavan suorituspäivän kaava** -kenttään *1D*.
6. Anna **Aloitusaika**-kentässä arvoksi *14.00*.
7. Valitse **Määritä tilaksi valmis** -toiminto.

Nyt varaston kustannukset päivittyvät joka ilta.  

Kun haluat ajoittaa tehtävän varaston täsmäyttämiseksi pääkirjanpitoon, valitse koodiyksikkö 2846 **Kirjaa varaston kust. KP:oon**.

> [!TIP]
> Jos haluat välttää lukitsemisen, älä ajoita **Muuta kust.-nimike tapahtumat** -eräajoa, **Kirjaa varaston kustannus KP:oon** -koodiyksikköä ja tehtäviä, joiden avulla kirjaat myynti-tai ostotransaktioita, samaan aikaan. Varmista myös, että ne käyttävät samaa työjonoluokkaa

## <a name="see-also"></a>Katso myös

[Nimikekustannusten muuttaminen](inventory-how-adjust-item-costs.md)  
[Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käsittele kohdetta [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
