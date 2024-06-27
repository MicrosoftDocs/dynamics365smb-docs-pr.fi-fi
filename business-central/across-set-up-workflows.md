---
title: Määritä hyväksymistyönkulut
description: 'Määritä työnkulut, työnkulun käyttäjät ja hyväksynnän käyttäjät yhdistääksesi näiden eri käyttäjien suorittamat liiketoimintaprosessin järjestelmätehtävät.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-approval-workflows"></a>Määritä hyväksymistyönkulut

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Hyväksyntätyönkulkujen käyttäminen](across-use-workflows.md).

Ennen kuin voit aloittaa hyväksyntätyönkulkujen käyttämisen, sinun on määritettävä työnkulun ja hyväksynnän käyttäjät miten käyttäjät saavat ilmoituksia työnkulun osavaiheista ja luotava työnkulut.

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.

[!INCLUDE[workflow](includes/workflow.md)]

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Työnkulun käyttäjien ja käyttäjäryhmien määrittäminen.|[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)|  
|Määritä työnkulun käyttäjät, jotka osallistuvat hyväksynnän työnkulkuihin.|[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)|  
|Määritä, miten työnkulun käyttäjät saavat ilmoituksia työnkulun osavaiheista, mukaan lukien hyväksyntäpyynnöistä.|[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)|  
|Määritä, ilmoitetaanko käyttäjille sähköpostitse tai käyttämällä huomautusta. Määritä myös, miten usein ilmoitukset lähetetään.|[Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Voit mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla Raportti 1320:n sähköposti-ilmoitusta.|[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)|  
|[!INCLUDE[prod_short](includes/prod_short.md)]in sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen|[Sähköpostin määrittäminen](admin-how-setup-email.md)|
|Määritä työnkulun eri vaiheet yhdistämällä työnkulun tapahtumat työnkulun vastauksiin.|[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)|  
|Käytä työnkulkumalleja luomaan uusia työnkulkumalleja.|[Hyväksyntätyönkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)|  
|Jaa työnkulkuja muiden [!INCLUDE[prod_short](includes/prod_short.md)]in tietokantojen kanssa.|[Hyväksyntätyönkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md)|  
|Opi määrittämään myyntiasiakirjojen työnkulkujen hyväksyntäpyyntöjä päästä päähän -menetelmällä.|[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Esimerkki hyväksymistyönkulusta

Tässä videossa kerrotaan, miten määritetään työnkulku, joka edellyttää käyttäjältä jonkun toisen hyväksynnän pyytämistä, ennen kuin on mahdollista muuttaa olemassa olevan asiakkaan tietoja tai luoda uutta asiakasta.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Katso myös

[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Business Centralin käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
