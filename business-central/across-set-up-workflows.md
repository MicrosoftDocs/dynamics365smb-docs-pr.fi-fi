---
title: Työnkulkujen määrittäminen (sisältää videon)
description: Määritä työnkulut, työnkulun käyttäjät ja hyväksynnän käyttäjät yhdistääksesi näiden eri käyttäjien suorittamat liiketoimintaprosessin järjestelmätehtävät.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 5be16c0d7cbd035d28a15967270cf982870acd78
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940799"
---
# <a name="set-up-workflows"></a>Työnkulkujen määrittäminen

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).  

 Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun ja hyväksynnän käyttäjät miten käyttäjät saavat ilmoituksia työnkulun osavaiheista, luotava työnkulut ja tehtävä mahdolliset koodin mukautukset.  

 Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

 Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, Microsoft-kumppanin on toteutettava se koodin avulla tai määrittämällä työnkulku Power Automaten avulla. Lisätietoja on kehittäjän ohjeiden kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md) tai [AL-tapahtumat](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al).

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Työnkulun käyttäjien ja käyttäjäryhmien määrittäminen.|[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)|  
|Määritä työnkulun käyttäjät, jotka osallistuvat hyväksynnän työnkulkuihin.|[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)|  
|Määritä, miten työnkulun käyttäjät saavat ilmoituksia työnkulun osavaiheista, mukaan lukien hyväksyntäpyynnöistä.|[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)|  
|Määritä, ilmoitetaanko käyttäjille sähköpostitse tai käyttämällä huomautusta. Määritä myös, miten usein ilmoitukset lähetetään.|[Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Voit mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla raportin 1320 sähköposti-ilmoitusta.|[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)|  
|[!INCLUDE[prod_short](includes/prod_short.md)]in sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen|[Sähköpostin määrittäminen](admin-how-setup-email.md)|
|Määritä työnkulun eri vaiheet yhdistämällä työnkulun tapahtumat työnkulun vastauksiin.|[Työnkulkujen luominen](across-how-to-create-workflows.md)|  
|Käytä työnkulkumalleja luomaan uusia työnkulkumalleja.|[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)|  
|Jaa työnkulkuja muiden [!INCLUDE[prod_short](includes/prod_short.md)]in tietokantojen kanssa.|[Työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md)|  
|Opi määrittämään myyntiasiakirjojen työnkulkujen hyväksyntäpyyntöjä päästä päähän -menetelmällä.|[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Esimerkki hyväksymistyönkulusta
Tässä videossa kerrotaan, miten määritetään työnkulku, joka edellyttää jonkun toisen hyväksyntää, ennen kuin on mahdollista muuttaa olemassa olevan asiakkaan tietoja tai luoda uutta asiakasta.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Katso myös  
 [Työnkulkujen käyttäminen](across-use-workflows.md)   
 [Työnkulku](across-workflow.md)   
 [Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Business Central -sovelluksen käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]