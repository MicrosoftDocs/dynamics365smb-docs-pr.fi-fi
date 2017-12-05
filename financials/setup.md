---
title: "Dynamics 365 Business editionin määritystehtävien yleiskatsaus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tehtävistä, joilla Dynamics 365 Business edition asennetaan, alustetaan ja määritetään omia tarpeita vastaavaksi."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: configure, initialize
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 68a4563aab0edc6a0ac5b8cbcc5e053c449f20f8
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-included365finlongincludesd365finlongmdmd"></a>[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -sovelluksen määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää vakiomääritykset useimmille liiketoimintaprosesseille. Voit muuttaa määritykset yrityksen tarpeita vastaaviksi.

Esimerkiksi tilikarttaan on kerätty käyttövalmiita kirjaustilejä. Voit tietysti muuttaa tilikarttaa liiketoimintasi vaatimalla tavalla. Lisätietoja on kohdassa [Rahoitus](finance.md).

Aloitussivulla on avustettuja asennusoppaita, joiden avulla voit määrittää tiettyjä skenaarioita sekä lisätä ominaisuuksia [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja siitä, miten käytät kaikkia avustettuja sekä manuaalisia määritysikkunoita löydät ohjeesta [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

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
| Määritä tietueille, kuten korteille, asiakirjoille ja päiväkirjan riville, yksilölliset tunnuskoodit, joilla tietueita voi seurata järjestelmässä. |[Numerosarjojen luominen](ui-create-number-series.md) |
| Määritä **SMTP-sähköpostiasetukset** -ikkunassa, miten [!INCLUDE[d365fin](includes/d365fin_md.md)]issa lähetetään ja vastaanotetaan sähköposteja asiakirjoista. |[Toimintaohje: Sähköpostin määrittäminen](madeira-how-setup-email.md) |
| Määritä yksilölliset tunnuskoodit. |[Toimintaohje: Numerosarjojen luominen](ui-create-number-series.md) |

Joidenkin alueiden edellytyksenä on, että käyttäjä on [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen järjestelmänvalvoja. Lisätietoja on kohdassa [Asetukset ja hallinto [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -ohjelmassa](admin-setup-and-administration.md).  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)
[Ostot](purchasing-manage-purchasing.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Projektinhallinta](projects-manage-projects.md)
[Käyttöomaisuus](fa-manage.md)    
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Asetukset ja hallinto [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa](admin-setup-and-administration.md)  
[Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa](about-new-company.md)  
[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

