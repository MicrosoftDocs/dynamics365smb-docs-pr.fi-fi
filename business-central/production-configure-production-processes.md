---
title: Tuotantoprosessien määrittäminen
description: 'Jotta materiaalit voidaan muuntaa tuotetuiksi lopullisiksi nimikkeiksi, järjestelmässä on määritettävä tuotantoresurssit, kuten tuoterakenteet, reititykset, koneenkäyttäjät ja koneet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000768, 99000779, 99000780, 99000866'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-manufacturing"></a>Tuotannon määrittäminen

Jotta materiaalit voidaan muuntaa tuotetuiksi lopullisiksi nimikkeiksi, järjestelmässä on määritettävä tuotantoresurssit, kuten tuoterakenteet, reititykset, koneenkäyttäjät ja koneet.

Koneenkäyttäjät ja koneet esitetään järjestelmässä kuormitusryhminä, jotka on voitu järjestää tuotantosoluiksi ja tuotantosoluryhmiksi. Kun nämä resurssit on muodostettu, ne voidaan ladata toiminnoilla, jotka perustuvat nimikkeen määritettyyn materiaali- eli tuotantorakenteeseen ja käsittely- eli reititysrakenteeseen sekä kuormitusryhmän tai tuotantosolun kapasiteettiin. Voit myös määrittää jokaisen resurssin tuotantokapasiteetin. Kapasiteetti on määritetty koneen ja tuotantosolujen saatavilla olevana työaikana, ja sitä valvotaan kalentereissa kullakin tasolla. Tuotantosolun kalenterissa määritetään työpäivät ja -tunnit, työvuorot, lomapäivät sekä poissaolot, jotka määräävät tuotantosolun käytettävissä olevan kokonaiskapasiteetin (yleensä minuutteina). Tämä määräytyy tehokkuuden ja kapasiteettiarvojen mukaan.  

Kun tuotanto on määritetty, voit suunnitella ja toteuttaa tuotantotilauksia. Lisätietoja on kohdissa [Suunnittelu](production-planning.md) ja [Tuotanto](production-manage-manufacturing.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä tuotantotoiminnot, joihin kuuluvat esimerkiksi tuotannon työtuntien määrittäminen sekä suunnitteluparametrien valitseminen.|**Tuotannon asetukset** -sivu|
|Määritä **Tuotannon asetukset** -sivun **Suunnitelma**-välilehdessä Yleiset suunnitelmaparametrit, jotka ohittavat yksittäisten nimikkeiden korteissa määritetyt parametrit.|[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)|
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
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
