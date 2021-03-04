---
title: Työnkulun ilmoitukset
description: Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: 1dd64213bc38d5d98e6369e97257e53cef04bbd0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753023"
---
# <a name="workflow-notifications"></a>Työnkulun ilmoitukset

Määritä työnkulut ilmoittamaan käyttäjille automaattisesti, kun työnkulun vaihe vaatii heidän huomionsa. Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee ilmoituksia sähköpostina ja sisäisinä muistiinpanoina.  

> [!IMPORTANT]  
> Kaikki työnkulun ilmoitukset lähetetään työjonon kautta. Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja että **Käynnistä automaattisesti palvelimelta** -valintaruutu on valittu. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Ilmoitusten määrittäminen

Työnkulun ilmoitusten osatekijöitä määritetään seuraavissa paikoissa:  

* Hyväksyjän ilmoitus

    Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -sivulla kullekin työnkulkuun osallistuvalle käyttäjälle.  

    Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 1. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
* Ilmoitusaikataulut

    Täyttämällä **Ilmoitusaikataulu**-sivu kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Sähköposti-ilmoitusten mukauttaminen

    Voit halutessasi mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  
* Vastausvaihtoehdot

    Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua. Se tehdään valitsemalla **Työnkulun vastausvaihtoehdot** -sivulla asetuksia ilmoitusta edustavalle työnkulun vastaukselle. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

* Ilmoita lähettäjälle

    Hyväksymistyönkuluille voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)  
[Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Työnkulkujen luominen](across-how-to-create-workflows.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Sähköpostin määrittäminen](admin-how-setup-email.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]