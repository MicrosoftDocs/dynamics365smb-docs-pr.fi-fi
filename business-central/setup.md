---
title: "Business Central -sovelluksen määritystehtävien yleiskatsaus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tehtävistä, jolla Business Central asennetaan, alustetaan ja määritetään omia tarpeita vastaavaksi."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: configure, initialize
ms.date: 03/22/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f669e4b4dd43a6ac32fafc0dc1e408e1b87be98b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-included365finincludesd365finmdmd"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää vakiomääritykset useimmille liiketoimintaprosesseille. Voit muuttaa määritykset yrityksen tarpeita vastaaviksi.

Esimerkiksi tilikarttaan on kerätty käyttövalmiita kirjaustilejä. Voit tietysti muuttaa tilikarttaa liiketoimintasi vaatimalla tavalla. Lisätietoja on kohdassa [Rahoitus](finance.md).

Roolisivulla on avustettuja asennusoppaita, joiden avulla voit määrittää tiettyjä skenaarioita sekä lisätä ominaisuuksia [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan. Lisätietoja siitä, miten käytät kaikkia avustettuja sekä manuaalisia määritysikkunoita löydät ohjeesta [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

> [!NOTE]
> Voit määrittää uuden yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa RapidStart Services -palvelun kanssa. RapidStart Services -palvelun on työkalu, joka on suunniteltu lyhentämään käyttöönottoa, parantamaan toteutuksen laatua, esittelemään toistettavia lähestymistapoja toteutuksiin, ja lisäämään tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md).

Tietyt joko yleiset tai erityiset liiketoimintaprosessien toiminnot voidaan määrittää manuaalisesti tai avustetusti. Seuraavassa luettelossa on joitakin manuaalisesti määritettäviä toimintoja.

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
|Lisätietoja parhaista käytännöistä, kun nimikkeitä määritetään varaston arvostusta ja tuotantosuunnittelua varten.|[Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)|
|[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman sisäisen ja ulkoisen sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen| [Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen](admin-how-setup-email.md)|
| Määritä tietueille, kuten korteille, asiakirjoille ja päiväkirjan riville, yksilölliset tunnuskoodit, joilla tietueita voi seurata järjestelmässä. |[Numerosarjojen luominen](ui-create-number-series.md) |
|Määritä ja liitä peruskalenteri yrityksellesi ja sen liiketoimintakumppaneille, esimerkiksi asiakkaille, toimittajille tai sijainneille. Toimituksen ja vastaanoton päivämäärät lasketaan tuleville myyntitilaus-, ostotilaus-, siirtotilaus- ja tuotantotilausriveille kalenteriin määritettyjen työpäivien mukaisesti.|[Peruskalenterien määrittäminen](across-how-to-assign-base-calendars.md)|  

Joidenkin alueiden edellytyksenä on, että käyttäjä on [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen järjestelmänvalvoja. Lisätietoja on kohdassa [Hallinta](admin-setup-and-administration.md).  

## <a name="see-also"></a>Katso myös
[Hallinta](admin-setup-and-administration.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Projektinhallinta](projects-manage-projects.md)  
[Käyttöomaisuus](fa-manage.md)    
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Hallinta](admin-setup-and-administration.md)  
[Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa](about-new-company.md)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

