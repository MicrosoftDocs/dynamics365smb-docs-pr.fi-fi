---
title: "Työnkulkujen määrittäminen| Microsoft Docs"
description: "Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 6beb70ad41fa32043e9b8afea67d390929533007
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="setting-up-workflows"></a>Työnkulkujen määrittäminen
Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).  

 Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun ja hyväksynnän käyttäjät miten käyttäjät saavat ilmoituksia työnkulun osavaiheista, luotava työnkulut ja tehtävä mahdolliset koodin mukautukset.  

 **Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

 Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, Microsoft-kumppanin on toteutettava se mukauttamalla sovelluksen koodia. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Työnkulun käyttäjien ja käyttäjäryhmien määrittäminen.|[Toimintaohje: Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)|  
|Määritä työnkulun käyttäjät, jotka osallistuvat hyväksynnän työnkulkuihin.|[Toimintaohje: Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)|  
|Määritä, miten työnkulun käyttäjät saavat ilmoituksia työnkulun osavaiheista, mukaan lukien hyväksyntäpyynnöistä.|[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)|  
|Määritä, milloin käyttäjät saavat ilmoituksia ja ovatko ilmoitukset koottuja tietyltä aikaväliltä ilmoitusten määrän vähentämiseksi.|[Toimintaohje: Määritä, milloin ja miten käyttäjät saavat ilmoituksia](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Määritä uusien työnkulun sähköposti-ilmoitusten asettelu ja yleinen sisältö tai vie, muokkaa ja tuo takaisin olemassa olevia malleja.|[Toimintaohje: Ilmoitusmallien hallinta](across-how-to-manage-notification-templates.md)|  
|[!INCLUDE[d365fin](includes/d365fin_md.md)]in sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen|[Toimintaohje: Sähköpostin määrittäminen](madeira-how-setup-email.md)|
|Määritä työnkulun eri vaiheet yhdistämällä työnkulun tapahtumat työnkulun vastauksiin.|[Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md)|  
|Käytä työnkulkumalleja luomaan uusia työnkulkumalleja.|[Ohje: Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)|  
|Jaa työnkulkuja muiden [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietokantojen kanssa.|[Toimintaohje: työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md)|  
|Opi määrittämään myyntiasiakirjojen työnkulkujen hyväksyntäpyyntöjä päästä päähän -menetelmällä.|[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Lisää tuki business skenaariolle, joka vaatii uuden työnkulun tapahtumat tai vastaukset, mukauttamalla sovelluksen koodi.|[Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Katso myös  
 [Työnkulkujen käyttäminen](across-use-workflows.md)   
 [Työnkulku](across-workflow.md)   
 [Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Financialsin käyttäminen](ui-work-product.md)

