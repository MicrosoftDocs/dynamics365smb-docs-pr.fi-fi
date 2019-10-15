---
title: Työnkulkuilmoitusten määrittäminen | Microsoft Docs
description: Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cab856000763e351046c4a81e8da6149c11e3c71
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308291"
---
# <a name="setting-up-workflow-notifications"></a>Työnkulkuilmoitusten määrittäminen
Monet työnkulun vastaukset ilmoittavat käyttäjälle toimia edellyttävistä tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee ilmoituksia sähköpostina ja sisäisinä muistiinpanoina.  

> [!IMPORTANT]  
>  Kaikki työnkulun ilmoitukset lähetetään työjonon kautta. Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja että **Käynnistä automaattisesti palvelimelta** -valintaruutu on valittu. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

Työnkulun ilmoitusten osatekijöitä määritetään seuraavissa paikoissa:  

1.  Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -sivulla kullekin työnkulkuun osallistuvalle käyttäjälle. Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 1. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
2.  Täyttämällä **Ilmoitusaikataulu**-sivu kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Voit halutessasi mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin tai asiakirjan mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  
4.  Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua. Se tehdään valitsemalla **Työnkulun vastausvaihtoehdot** -sivulla asetuksia ilmoitusta edustavalle työnkulun vastaukselle. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

## <a name="see-also"></a>Katso myös  
 [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
 [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)   
 [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Raporttien tai asiakirjojen mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)   
 [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md)   
 [Sähköpostin määrittäminen](admin-how-setup-email.md)   
 [Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Työnkulku](across-workflow.md)   
