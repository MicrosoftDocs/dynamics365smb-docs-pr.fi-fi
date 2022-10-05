---
title: Dynamics 365 Business Centralin työnkulut
description: Sisäisen työnkulun ominaisuuksien avulla voit määrittää hyväksyntätyönkulkuja, jotka täydentävät Power Automateen perustuvia automatisoituja työnkulkuja. Voit määrittää vaiheet, joiden avulla tehtäviä määritetään eri henkilöille osana liiketoimintaprosessien eri tehtäviä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585619"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Dynamics 365 Business Centralin työnkulut

Voit määrittää ja käyttää työnkulkuja yhdistääksesi eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio tukee kolmentyyppisiä työnkulkuja:

* Sisäisiin työnkulkumalleihin perustuvat hyväksyntätyönkulut

  **Työnkulkumallit**-sivulla näkyvät kaikki käytettävissä olevat työnkulut. [!INCLUDE[prod_short](includes/prod_short.md)]in kokeiluversio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda uusia. Kun avaat mallin **Työnkulunmallit**-sivulta ja työnkulun nimi alkaa kirjaimilla *MS-*, Microsoft lisää mallin.
  
* Itse määrittämäsi Power Automate -työnkulut

  Microsoft Power Automatella luodut työnkulkumallit lisätään [!INCLUDE[prod_short](includes/prod_short.md)]in työkulkumalleihin. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md). 
  
* **Automaattisen** toiminnon (vain [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa) manuaalisesti käynnistämät pikatyönkulut.

  Luo ja manuaalisesti käynnistää Power Automate -työnkulun [!INCLUDE[prod_short](includes/prod_short.md)] -tietueesta, kuten asiakkaasta, nimikkeestä tai myyntitilauksesta, jolla voi käsitellä tietoja sekä sisäisesti että ulkoisesti (käyttämällä integroituja työkaluja). Katso lisätietoja [Pikatyönkulut](across-how-use-financials-data-source-flow.md#instant-flows)-osasta.

## <a name="power-automate-flows"></a>Power Automate -työnkulut

Käyttämällä [!INCLUDE [prod_short](includes/prod_short.md)] online-tilaa voit kirjautua Power Automateen luodaksesi tehokkaita automaattisia työnkulkuja. Voit käyttää työnkulkuja [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen sisältä yhdistämällä sisäisiä ja ulkoisia tietolähteitä ja työkaluja ilman koodaustaitoa.

Power Automate -työnkulkuja voidaan käynnistää tapahtumilla (kuten tietueen tai asiakirjan luominen, muokkaaminen tai poistaminen) ja suorittaa käyttäjän määrittämän aikataulun mukaan tai pyynnöstä (tunnetaan nimellä **pikatyönkulku**).

## <a name="approval-workflows"></a>Hyväksyntätyönkulut

Voit luoda hyväksymistyönkulun luettelemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät käyttämällä tapahtumien kiinteitä luetteloita ja vastausarvoja, jotka edustavat sovelluskoodin tukemia skenaarioita.<!--What are the "values"? Can we give an example?-->

Esimerkkejä hyväksyntätyönkulkutapahtumista ovat muun muassa myynti- tai ostotilausten/tarjousten/laskujen luominen, hintojen muutokset sekä myyjän tai asiakkaan muokkaukset.

[!INCLUDE[workflow](includes/workflow.md)]

| **Tehtävä** | **Katso** |
|--|--|
| Luo hyväksyntätyönkulun käyttäjiä, määritä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja. (Halutessasi määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.) | [Määritä hyväksymistyönkulut](across-set-up-workflows.md) |
| Ota käyttöön hyväksyntätyönkulkuja ja käsittele työnkulun ilmoituksia, mukaan lukien työnkulun vaiheen pyytäminen ja hyväksyminen. Arkistoi ja poista työnkulkuja. | [Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md) |
| Integroi yrityksen tiedot Power Automate -työnkulkujen avulla sekä sisäisten että ulkoisten lähteiden ja tapahtumien avulla, kun luot ja automatisoit tehtäviä tai työnkulkuja. | [[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-workflows/)

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Projektien hallinta](projects-manage-projects.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
