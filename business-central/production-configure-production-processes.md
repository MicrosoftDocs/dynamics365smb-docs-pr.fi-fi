---
title: "Tuotantoprosessien määrittäminen | Microsoft Docs"
description: "Jotta materiaalit voidaan muuntaa tuotetuiksi lopullisiksi nimikkeiksi, järjestelmässä on määritettävä tuotantoresurssit, kuten tuoterakenteet, reititykset, koneenkäyttäjät ja koneet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e167935f1bb4815093a1a9bd345da8213219ca08
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-manufacturing"></a>Tuotannon määrittäminen
Jotta materiaalit voidaan muuntaa tuotetuiksi lopullisiksi nimikkeiksi, järjestelmässä on määritettävä tuotantoresurssit, kuten tuoterakenteet, reititykset, koneenkäyttäjät ja koneet.

Koneenkäyttäjät ja koneet esitetään järjestelmässä kuormitusryhminä, jotka on voitu järjestää tuotantosoluiksi ja tuotantosoluryhmiksi. Kun nämä resurssit on muodostettu, ne voidaan ladata toiminnoilla, jotka perustuvat nimikkeen määritettyyn materiaali- eli tuotantorakenteeseen ja käsittely- eli reititysrakenteeseen sekä kuormitusryhmän tai tuotantosolun kapasiteettiin. Voit myös määrittää jokaisen resurssin tuotantokapasiteetin. Kapasiteetti on määritetty koneen ja tuotantosolujen saatavilla olevana työaikana, ja sitä valvotaan kalentereissa kullakin tasolla. Tuotantosolun kalenterissa määritetään työpäivät ja -tunnit, työvuorot, lomapäivät sekä poissaolot, jotka määräävät tuotantosolun käytettävissä olevan kokonaiskapasiteetin (yleensä minuutteina). Tämä määräytyy tehokkuuden ja kapasiteettiarvojen mukaan.  

Kun tuotanto on määritetty, voit suunnitella ja toteuttaa tuotantotilauksia. Lisätietoja on kohdissa [Suunnittelu](production-planning.md) ja [Tuotanto](production-manage-manufacturing.md).  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä tuotantotoiminnot, joihin kuuluvat esimerkiksi tuotannon työtuntien määrittäminen sekä suunnitteluperiaatteiden valitseminen.|**Tuotannon asetukset** -ikkuna.|  
|Määritä tuotanto-osaston vakiotyöviikko määrittämällä kunkin työpäivän alku- ja loppuajat sekä työvuorot.|[Tuotantokalenterien luominen](production-how-to-create-work-center-calendars.md)|  
|Järjestä tuotantoresurssien kiinteät arvot ja vaatimukset tuotantosoluina tai kuormitusryhmien tuotoksen hallintaa varten.|[Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md)|
|Järjestä tuotantotoiminnot vaadittuun järjestykseen ja määritä tuotantosoluihin ja kuormitusryhmiin vaadituin työajoin.|[Uusien reititysten luominen](production-how-to-create-routings.md)|
|Järjestä tuotannon komponentit tai osakokoonpanot tuotettuun päänimikkeeseen ja hyväksy tuotantosolujen toteutuksen tuoterakenne.|[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)|
|Varmista, että käytettävissä on oikea komponenttimäärä, kun tuotetut nimikkeet varastointii käytetään yhtä mittayksikköä mutta tuotantoon toista.|[Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Säästä kulutuksessa määrittämällä tuotantonimikeperheitä, joilla on samantyyppiset tuotantoprosessit. Esimerkiksi saman nimikkeen neljä kappaletta voidaan tuottaa yhdestä lomakkeesta ja toisen, eri nimikkeen, 10 kappaletta yhtä aikaa.|[Tuotantoperheiden käsitteleminen](production-how-work-family.md)|
|Yksinkertaista reitityksen luontia vakiotehtävillä, jotka liittävät lisätiedot nopeasti toistuviin toimintoihin.|[Vakioreititysrivien määrittäminen](production-how-set-up-standard-routing-lines.md)|  
|Valmistele tuotantosolut ja reititykset alihankintana toteutettuja tuotantotoimintoja edustaviksi.|[Tuotanto alihankintana](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Katso myös
[Tuotanto](production-manage-manufacturing.md)    
[Suunnittelu](production-planning.md)   
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

