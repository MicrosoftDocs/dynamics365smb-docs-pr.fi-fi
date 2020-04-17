---
title: Business Central -sovelluksen määritystehtävien yleiskatsaus | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan tehtävistä, jolla Business Central asennetaan, alustetaan ja määritetään omia tarpeita vastaavaksi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: configure, initialize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 80f33734365ad52b59e77d89e35af81d5a798fcb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194665"
---
# <a name="setting-up-prodshort"></a>[!INCLUDE[prodshort](includes/prodshort.md)] -sovelluksen määrittäminen

[!INCLUDE[prodshort](includes/prodshort.md)] sisältää vakiomääritykset useimmille liiketoimintaprosesseille. Voit muuttaa määritykset organisaatiosi tarpeita vastaaviksi.

Esimerkiksi tilikarttaan on kerätty käyttövalmiita kirjaustilejä. Voit tietysti muuttaa tilikarttaa liiketoimintasi vaatimalla tavalla. Lisätietoja on kohdassa [Rahoitus](finance.md).

Voit avata ![Asetukset-valikko](media/ui-experience/settings_icon_small.png) -valikon ketju pyörä kuvakkeesta ja käyttää asetusten ohjattuja määritysoppaita, jotka auttavat tiettyjen skenaarioiden määrittämisessä ja ominaisuuksien lisäämiseen [!INCLUDE[prodshort](includes/prodshort.md)]. Lisätietoja siitä, miten käytät kaikkia avustettuja sekä manuaalisia määrityssivuja, on ohjeessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

Tietyt joko yleiset tai erityiset liiketoimintaprosessien toiminnot voidaan määrittää manuaalisesti tai asetusten ohjattuna määrityksenä. Seuraavassa luettelossa on joitakin manuaalisesti määritettäviä toimintoja.

| Toiminta | Katso |
| --- | --- |
| Määritä maksutavat, valuutat ja tilikartta. Määritä myös rahoitustapahtumien hallinnan säännöt ja oletusarvot. |[Rahoituksen määrittäminen](finance-setup-finance.md) |
| Määritä oman pankkitilisi ja toimittajien pankkitilit sekä ota käyttöön pankkitiedostojen tuonti- ja vientipalvelut. |[Pankkitoiminnan määrittäminen](bank-setup-banking.md) |
| Määritä yrityksen myyntikäytäntöjä koskevat säännöt ja arvot, rekisteröi uudet asiakkaat ja määritä asiakkaiden kanssa käytettävät viestintätavat. |[Myynnin määrittäminen](sales-setup-sales.md) |
| Määritä yrityksen ostokäytäntöjä koskevat säännöt, rekisteröi uudet toimittajat ja priorisoi toimittajat maksujen käsittelyä varten. |[Ostojen määrittäminen](purchasing-setup-purchasing.md) |
| Määritä yrityksen varastokäytäntöjä koskevat säännöt, määritä sijainnit, josta varasto jakautuu useisiin fyysisiin varastoihin, sekä paranna hakua ja lajittelua luokittelemalla nimikkeet. |[Varaston määrittäminen](inventory-setup-inventory.md) |
| Hallitse projekteja määrittämällä resurssit, aikaraportit ja projektityöt. |[Projektinhallinnan määrittäminen](projects-setup-projects.md) |
| Määritä käyttöomaisuuden vakuuttaminen, kunnossapito ja poistot sekä tapa, jolla käyttöomaisuuden kustannukset kirjataan yrityskirjoihin. |[Käyttöomaisuuden määrittäminen](fa-setup.md) |
|Määritä varastointiprosessien yleiset säännöt ja arvot sekä sijaintikohtainen käsittely.|[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)|
|Valmistele tuotannon tuoterakenteet ja reititykset määrittämään loppunimikkeiden tuotantotapa. Valmistele myös kuormituskeskukset tai tuotantosolut suorittamaan tarvittavat toiminnot.|[Tuotannon määrittäminen](production-configure-production-processes.md)|
|Muodosta vakiohuollot, oireet ja vikakoodit sekä määritä huoltonimikkeet, resurssit ja dokumentaatio, joiden avulla asiakkaille voidaan tarjota huoltoa.|[Huoltohallinnon määrittäminen](service-setup-service.md)|
|Lisätietoja parhaista käytännöistä, kun nimikkeitä määritetään varaston arvostusta ja tuotantosuunnittelua varten.|[Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)|
|Paranna toteutuksen laatua ja lyhennä käyttöönottoa käyttämällä työkaluja, jolla uusi yritys määritetään ohjattujen toimintojen, mallien, työkirjojen ja asiakaskyselyjen avulla.|[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)|
|Asiakas-, toimittaja-, varasto- ja pankkitilitietojen siirtäminen toisesta järjestelmästä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin|[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).|
|Voit tarkastella Business Centralin Outlook-apuohjelmien avulla asiakkaisiin ja toimittajiin liittyviä taloustietoja tai luoda ja lähettää talousasiakirjoja, kuten tarjouksia ja laskuja.|[Business Central -sovelluksen käyttäminen yrityssähköpostina Outlookissa](admin-outlook.md)|
|Saat lisätietoja Business Central -tiedoista Power BI:n ja Business Centralin sisältöpakettien avulla.|[Yritystietojen ottaminen käyttöön Power BI:tä varten](admin-powerbi.md)|
|Käytä Business Central -tietoja Power Automate -työnkulun osana.|[Business Central -sovelluksen käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)|
|Ota Business Central -tiedot käyttöön Power Appsin tietolähteenä.|[Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Appsin avulla](across-how-use-financials-data-source-powerapps.md)|
|Käytä erityisiä Quickbooksin siirto-oppaita.|[Vaihtaminen QuickBooks-sovelluksesta Business Centraliin](across-quickbooks-to-business-edition.md)|
|Käytä Business Central -tietoja mobiililaitteella.|[Business Central -sovelluksen hakeminen mobiililaitteeseen](install-mobile-app.md)|
|Massalaskuta Bookingsissa luodut tapaamiset.|[Microsoft Bookingsin massalaskutus](finance-bookings.md)|
|[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman sisäisen ja ulkoisen sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen| [Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen](admin-how-setup-email.md)|
| Määritä tietueille, kuten korteille, asiakirjoille ja päiväkirjan riville, yksilölliset tunnuskoodit, joilla tietueita voi seurata järjestelmässä. |[Numerosarjojen luominen](ui-create-number-series.md) |
|Määritä ja liitä peruskalenteri yrityksellesi ja sen liiketoimintakumppaneille, esimerkiksi asiakkaille, toimittajille tai sijainneille. Toimituksen ja vastaanoton päivämäärät lasketaan tuleville myyntitilaus-, ostotilaus-, siirtotilaus- ja tuotantotilausriveille kalenteriin määritettyjen työpäivien mukaisesti.|[Peruskalenterien määrittäminen](across-how-to-assign-base-calendars.md)|  

Joidenkin alueiden edellytyksenä on, että käyttäjä on [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen järjestelmänvalvoja. Lisätietoja on kohdassa [Hallinta](admin-setup-and-administration.md).  

> [!NOTE]
> Järjestelmänvalvojana voit määrittää uuden yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa RapidStart Servicesin avulla. RapidStart Services on työkalu, joka on suunniteltu lyhentämään käyttöönottoa, parantamaan toteutuksen laatua, esittelemään toistettavia lähestymistapoja toteutuksiin sekä lisäämään tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md).

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Varasto](inventory-manage-inventory.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Käyttöomaisuus](fa-manage.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa](about-new-company.md)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
