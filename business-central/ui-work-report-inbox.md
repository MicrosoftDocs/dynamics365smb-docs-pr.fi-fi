---
title: Raporttien jakaminen ja vieminen Saapuneet raportit -toiminnon avulla
description: 'Saapuneet raportit -sivun avulla voit ladata, jakaa ja viedä raportteja Business Centralissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="share-and-export-reports-with-the-report-inbox"></a>Raporttien jakaminen ja vieminen Saapuneet raportit -toiminnon avulla

**Saapuneet raportit** -sivulla on käyttäjän sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)] luomat ajoitetut raportit. Sitä voidaan käyttää luotujen raporttien käyttämisen lisäksi myös tiedostojen jakamisessa ja avaamisessa OneDrive for Business -ratkaisussa.

> [!TIP]
> Seuraavat toiminnot ovat myös käytettävissä **Saapuneet raportit** -osassa roolikeskuksessa. Jos osaa ei näytetä liittymässäsi, löydät ohjeita roolikeskuksen mukauttamiseen täältä: [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="download-generated-reports"></a>Luotujen raporttien lataaminen

Voit tallentaa aiemmat raportit avaamalla **Saapuneet raportit** -sivun seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuneet raportit** ja valitse vastaava linkki.  
2. Valitse **Saapuneet raportit** -sivulla haluamasi raportti.

> [!NOTE]
> Sivulla ei ole aiempia raportteja, jotka on luotu **Tulosta**-toiminnon avulla tai tallennettu tiedostona **Raportit**-valikossa.
>
> Luodut tiedostot tallennetaan muodossa, joka on määritetty raportin ajoituksen yhteydessä. Sen voi muuttaa **Työjonotapahtumat**-sivulla yhdessä toisto- ja muiden asetusten kanssa. Lisätietoja raportin tiedostomuodon muuttamisesta ja lisäasetusten määrittämisestä on kohdassa [Aikataulutettujen toistuvien raporttien hallinta](ui-work-report.md#manage-scheduled-recurring-reports).

## <a name="open-generated-reports-in-onedrive"></a>Luotujen raporttien avaaminen OneDrivessa

Voit viedä raporttitiedoston Microsoft OneDrive for Businessiin valitsemalla raportin **Saapuneet raportit** -sivulla ja valitsemalla **Avaa OneDrivessa** -toiminnon. Raportti kopioidaan tämän jälkeen sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] kansioon OneDrivessa ja avataan uudessa selainikkunassa, jossa voit tulostaa asiakirjatiedoston ja hallita sitä.

> [!IMPORTANT]
>
> Raportteja, jotka on määritetty vanheneviksi **Raportin aikataulutus** -sivulla ja kopioitu OneDriveen, ei automaattisesti poisteta jaetusta kansiosta.

## <a name="share-scheduled-reports"></a>Aikataulutettujen raporttien jakaminen

Raporttien jakaminen yhteistyökumppaneiden kanssa on mahdollista myös **Saapuneet raportit** -sivulla. Valitse raportti ja valitse sitten **Jaa**-toiminto. Valitse **Lähetä linkki** -sivu, valitse käyttäjä, joka voi avata tiedoston, määritä muokkausoikeudet ja lähetä linkki tallennetun raportin käyttämistä varten valitsemalla **Lähetä**.

> [!NOTE]
> Jos haluat lisätietoja OneDrive-integroinnista ja -ominaisuuksista sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)], mukaan lukien ensimmäisenä tehtävät asetukset ja vaihtoehdot nimiristiriitojen ratkaisemiseksi, lue [Tiedostojen avaaminen ja jakaminen OneDrivessa](across-share-onedrive.md) -artikkeli.
>
> **Jaa**-toiminnon käyttäminen määrittää luodun raporttitiedoston muiden käyttäjien saataville vain OneDrive for Businessissa. Se ei määritä ajoitettua raporttia heidän **Saapuneet raportit** -kohdan luetteloon.

## <a name="see-also"></a>Katso myös

[Raporttien suorittaminen ja tulostaminen](ui-work-report.md)  
[Käytettävissä olevat raportit kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Raporttien käyttäminen päivittäisessä työssä](reports-use-reports.md)  
[Business Intelligencen ja raportoinnin yleiskuva](reports-bi-reporting.md)  
[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  
[Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]- ja OneDrive-integrointi](across-onedrive-overview.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
