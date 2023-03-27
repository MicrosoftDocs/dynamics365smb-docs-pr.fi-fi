---
title: Dynamics 365 Business Centralin työnkulut
description: 'Sisäisen työnkulun ominaisuuksien avulla voit määrittää hyväksyntätyönkulkuja, jotka täydentävät Power Automateen perustuvia automatisoituja työnkulkuja. Voit määrittää vaiheet, joiden avulla tehtäviä määritetään eri henkilöille osana liiketoimintaprosessien eri tehtäviä.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# Dynamics 365 Business Centralin työnkulut

Voit määrittää ja käyttää työnkulkuja yhdistääksesi eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä, kuten automaattinen kirjaus, voidaan sisällyttää työnkulkuihin. Käyttäjätehtävät voivat edeltää tai seurata järjestelmätehtäviä. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio tukee kolmentyyppisiä työnkulkuja:
  
* Power Automate -työnkulut

  * Automaattiset työnkulut käynnistyvät tapahtumien, (kuten tietueiden tai asiakirjojen luonnin, muuttamisen tai poistamisen avulla) [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Mukana ovat myös Power Automatessa luodut hyväksymistyönkulut, jotka käynnistyvät kun hyväksyntää pyydetään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.
  * Pikatyönkulut, jotka käynnistetään manuaalisesti **Automaattinen**-toiminnolla luetteloista, korteista ja asiakirjasivuilta.

    Luo ja manuaalisesti käynnistää Power Automate -työnkulun [!INCLUDE[prod_short](includes/prod_short.md)] -tietueesta, kuten asiakkaasta, nimikkeestä tai myyntitilauksesta, jolla voi käsitellä tietoja sekä sisäisesti että ulkoisesti (käyttämällä integroituja työkaluja).

* Sisäisiin työnkulkumalleihin perustuvat hyväksyntätyönkulut

  **Työnkulkumallit**-sivulla näkyvät kaikki käytettävissä olevat työnkulut. [!INCLUDE[prod_short](includes/prod_short.md)]in kokeiluversio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda uusia. Kun avaat mallin **Työnkulunmallit**-sivulta ja työnkulun nimi alkaa kirjaimilla *MS-*, Microsoft lisää mallin.

## Power Automate -työnkulut

[!INCLUDE [prod_short](includes/prod_short.md)] online-tilan avulla voit kirjautua Power Automateen luodaksesi tehokkaita automaattisia työnkulkuja. Nämä työnkulut suoritetaan [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmasta. Työnkulut voivat yhdistämää sisäisiä ja ulkoisia tietolähteitä ja työkaluja ilman koodaustaitoa.

|**Tehtävä** |**Katso**|
|-------|-------|
|Aloita Power Automaten käyttäminen ja työnkulkujen luominen, pikatyönkulkujen suorittaminen|[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md)|
|Lisätietoja työnkulkujen luomisesta, muokkaamisesta ja hallinnasta|[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) ja [Pikatyönkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Määritä Power Automate -integrointi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmalla käyttäjille ylläpitäjänä|[Power Automate -integraation määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## Hyväksyntätyönkulut

Luo hyväksymistyönkulku määrittämällä, mikä työnkulun aloittaa ja mitä tapahtuu seuraavaksi:

* Tapahtumaehtojen avulla muokattu työnkulkutapahtuma.
* Työnkulun vastaus, jota valvotaan vastausasetuksilla.

Määrittääksesi työnkulun, täytä työnkulkurivien kentät käyttämällä tapahtumien ja vastausten arvoja, jotka edustavat tuettuja skenaarioita.

Esimerkkejä hyväksyntätyönkulkutapahtumista ovat myynti- tai ostotilausten/tarjousten/laskujen luominen, hintojen muutokset sekä myyjän tai asiakkaan muokkaukset, jne.

[!INCLUDE[workflow](includes/workflow.md)]

| **Tehtävä** | **Katso** |
|--|--|
| Luo hyväksyntätyönkulun käyttäjiä, määritä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja. (Halutessasi määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.) | [Määritä hyväksymistyönkulut](across-set-up-workflows.md) |
| Ota käyttöön hyväksyntätyönkulkuja ja käsittele työnkulun ilmoituksia, mukaan lukien työnkulun vaiheen pyytäminen ja hyväksyminen. Arkistoi ja poista työnkulkuja. | [Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-workflows/)

## Katso myös

[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Projektien hallinta](projects-manage-projects.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
