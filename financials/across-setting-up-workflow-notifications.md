---
title: "Työnkulkuilmoitusten määrittäminen | Microsoft Docs"
description: "Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 351c079df25516a83de42d5fa12954b25ba5e63e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflow-notifications"></a>Työnkulkuilmoitusten määrittäminen
Monet työnkulun vastaukset ilmoittavat käyttäjälle toimia edellyttävistä tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee ilmoituksia sähköpostina ja sisäisinä muistiinpanoina.  

> [!IMPORTANT]  
>  Kaikki työnkulun ilmoitukset lähetetään työjonon kautta. Varmista, että ratkaisussa on työjono. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

Työnkulun ilmoitusten osatekijöitä määritetään seuraavissa paikoissa:  

1.  Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -ikkunassa kullekin työnkulkuun osallistuvalle käyttäjälle. Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 1. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
2.  Täyttämällä **Ilmoitusaikataulu**-ikkuna kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Ilmoitusten yleinen sisältö ja asettelu määritetään **Ilmoitusmallit**-ikkunassa määrittämällä ilmoitusmallit (koskee myös ilmoituksia myöhässä olevista työnkulun vastauksista). Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusmalleja.  
4.  Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua. Se tehdään valitsemalla **Työnkulun vastausvaihtoehdot** -ikkunassa asetuksia ilmoitusta edustavalle työnkulun vastaukselle. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

## <a name="see-also"></a>Katso myös  
 [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
 [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)   
 [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Ilmoitusmallien hallinta](across-how-to-manage-notification-templates.md)   
 [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md)   
 [Sähköpostin määrittäminen](madeira-how-setup-email.md)   
 [Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Työnkulku](across-workflow.md)   
