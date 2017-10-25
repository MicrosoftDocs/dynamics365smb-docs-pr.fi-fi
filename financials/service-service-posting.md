---
title: Huollon kirjaaminen | Microsoft Docs
description: "Huollon kirjaustoiminnon avulla voit käsitellä asiakirjoja tehokkaasti ja ylläpitää onnistunutta asiakkaiden huoltomenettelyä. Tämän ominaisuuden avulla ohjelma voi luoda ja päivittää kirjattuja asiakirjoja, luoda tapahtumia huoltoalueella sekä muissa moduuleissa asianmukaisen päivityksen varmistamiseksi."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d82961b41266f645f87b79555171891cd2ce828f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="service-posting"></a>Huollon kirjaus
Huollon kirjaustoiminnon avulla voit käsitellä asiakirjoja tehokkaasti ja ylläpitää onnistunutta asiakkaiden huoltomenettelyä. Tämän ominaisuuden avulla ohjelma voi luoda ja päivittää kirjattuja asiakirjoja, luoda tapahtumia huoltoalueella sekä muissa moduuleissa asianmukaisen päivityksen varmistamiseksi.  

> [!NOTE]  
>  Seuraavassa ohjeessa neuvotaan, miten huoltokirjauksia tehdään riippumatta siitä, miten kohteita käsitellään fyysisessä varastossa.  
>   
>  Jos fyysisen varaston käsittely ei ole pakollista sijainnissa, tee kirjaustoiminnot suoraan **Huoltorivit**-ikkunassa. Sijainneissa, joissa käytetään fyysisen varaston käsittelyä, kuvatut kirjaustoiminnot (toimitusta ja kulutusta lukuun ottamatta) suoritetaan suoraan muuttuvien fyysisen varaston toimitustoimintojen kautta asetusten perusteella. Lisätietoja on kohdassa [Toimintaohje: Nimikkeiden poiminta varaston poiminnassa](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Toimitus  
Toimitusvaihtoehdon avulla voit rekisteröidä ohjelmassa nimikkeet ja huoltotilauksen riveille huollon suorituksen jälkeen syötetyt ajat. Ohjelma luo kirjatun toimituksen ja päivittää varastomoduulin ja muut [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman moduulit sen mukaan, mitä nimikkeitä on otettu varastosta ja lähetetty asiakkaalle. Ohjelma tuottaa erityisesti nimiketapahtumia, arvotapahtumia, huoltotapahtumia ja takuutapahtumia.  

Jos sijainti on määritetty niin, että fyysisen varaston käsittely on pakollinen, huoltonimikerivien toimitus ja siirtäminen tapahtuu samalla tavalla kuin muissa lähdeasiakirjoissa. Ainoa ero on, että huoltorivin nimikkeet voidaan käyttää joko ulkoisesti tai sisäisesti, johon tarvitaan kaksi eri vapautustoimintoa.

## <a name="invoice"></a>Lasku  
Sinun on käytettävä laskutusvalintaa, kun laskutat asiakkaalta huollon. Yleensä **Kirjaa toimitus** -toiminnon avulla rekisteröidyn toimitetun määrän ja **Kirjaa kulutus** -toiminnon avulla rekisteröidyn kulutetun määrän ero on laskutettava määrä. Et voi laskuttaa määrää, jota ei ole toimitettu. Kun suoritat **Kirjaa lasku** -toiminnon, ohjelma luo kirjatun huoltolaskun ja päivittää kirjatut asiakirjat, ennen kuin niistä tehdään lähetetyn laskun määrien mukaisia. Ohjelma luo asianmukaiset tapahtumat, esim. KP-tapahtumat, kuten muissa kirjausprosesseissa.  

## <a name="ship-and-invoice"></a>Toimitus ja lasku  
Toimitus- ja laskutusvaihtoehdon avulla voit luoda sekä palvelutoimituksen että laskun samaan aikaan.  

## <a name="ship-and-consume"></a>Toimitus ja kulutus  
Toimita- ja kuluta -vaihtoehdon avulla voit rekisteröidä ja kirjata nimikkeitä, kustannuksia tai tunteja, jotka on käytetty huollossa, mutta joita ei voi sisällyttää asiakkaalle lähetettävään laskuun. Ohjelma ei lähetä laskua, mutta mahdollistaa huoltotoimituksen ja huollon kulutuksen lähettämisen samanaikaisesti, jolloin nähdään, että osa nimikkeistä/tunneista on ollut asiakkaalle ilmaisia. Vastaavia tapahtumia luodaan myös, jotta kulutus voidaan rekisteröidä.  

> [!NOTE]  
>  Huollon kirjausprosessi mahdollistaa osittaisen kirjauksen. Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja  **Laskutettava määrä** -kentät huoltotilausten yksittäisillä huoltoriveillä ennen kirjausta. Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu. Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt rekisteröidä toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.  

Kirjauksen jälkeen voit katsella kirjattuja huoltoasiakirjoja niitä vastaavista ikkunoista **Kirjattu huoltotoimitus** ja **Kirjattu huoltolasku**. Luodut kirjatut tapahtumat ovat näkyvissä erilaisissa kirjattuja tapahtumia (**KP-tapahtumia**, **nimiketapahtumia**, **fyysisen varaston tapahtumia**, **huoltotapahtumia**, **projektitapahtumia**, **takuutapahtumia** jne.) sisältävissä ikkunoissa.  

## <a name="to-view-information-about-a-posted-service-document"></a>Kirjattujen huoltoasiakirjojen tarkasteleminen  
Kun kirjaat huoltolaskun, huoltotoimituksen tai huollon hyvityslaskun, asiakirjan tiedot siirretään **Kirjattu huoltolasku**-, **Kirjattu huoltotoimitus**- tai **Kirjattu huollon hyvityslasku** -ikkunaan. Et voi syöttää mitään näihin ikkunoihin tai muuttaa tai poistaa niistä mitään. Näissä ikkunoissa voi tulostaa toimituksen, laskun tai hyvityslaskun.  

Seuraavassa ohjeessa käytetään esimerkkinä kirjattua huoltolaskua, mutta samaa menettelyä voidaan käyttää kirjattuihin toimituksiin sekä palvelu- ja hyvityslaskuihin.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjattu huoltolasku** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa kirjattu huoltolasku, jonka haluat nähdä.  
3. Valitse **Tilastot**-toiminto, jos haluat yleiskuvan kirjatusta laskusta.  

    Avaa **Huoltotilaustilastot**-ikkuna. Ikkunassa on muun muassa seuraavat kirjatun asiakirjan tiedot: määrä, summa, ALV, kustannus, tuotto ja asiakkaan luottoraja.

## <a name="see-also"></a>Katso myös  
[Huoltotilauksien kirjaaminen](service-how-to-post-service-orders.md)   
[Toimintaohje: Huoltotilausten luominen](service-how-to-create-service-orders.md)

