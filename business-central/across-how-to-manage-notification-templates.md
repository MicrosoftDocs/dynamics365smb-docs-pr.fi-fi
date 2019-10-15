---
title: Ilmoitusmallien hallinta | Microsoft Docs
description: Työnkulun käyttäjille lähetetään ilmoituksia suoritettavista osavaiheista sekä työnkulun osavaiheiden tilasta. Ilmoituksen vastaanottaja ja lähetysaika asetetaan määrittämällä hyväksynnän käyttäjät, käyttäjien ilmoitusaikataulu sekä tarvittavat työnkulun vastaukset.
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
redirect_url: across-how-to-specify-when-and-how-to-receive-notifications
ms.openlocfilehash: c195ffa8b798f13d92f78896f101a84b07728d08
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305354"
---
# <a name="manage-notification-templates"></a>Ilmoitusmallien hallinta
Työnkulun käyttäjille lähetetään ilmoituksia suoritettavista osavaiheista sekä työnkulun osavaiheiden tilasta. Ilmoituksen vastaanottaja ja lähetysaika asetetaan määrittämällä hyväksynnän käyttäjät, käyttäjien ilmoitusaikataulu sekä tarvittavat työnkulun vastaukset. Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).  

 Ilmoitukset perustuvat malleihin, jotka määrittävät ilmoitusten sisällön ja asettelun. Voit viedä ilmoitusmallin sisällön, muokata sitä ja tuoda takaisin samaan tai uuteen ilmoitusmalliin. Tämä kuvataan seuraavissa menettelytavoissa.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)]in yleisessä versiossa on kolme ilmoitusmallia. Yksi niistä on tarkoitettu hyväksyntäpyynnöille, yksi uusista tietueista ilmoittamiseen ja yksi myöhässä olevista hyväksyntäpyynnöistä ilmoittamiseen. Kolmen ennalta määritetyn ilmoitusmallin ilmoitusmenetelmänä voi käyttää **sähköpostia** ja **muistiinpanoa**. Jos haluat tarkastella näiden kolmen ilmoitusmallin sisältöä, katso lisätietoja tämän ohjeaiheen kohdasta "Ilmoitusmallien sisältö".

## <a name="to-create-a-new-notification-template"></a>Uuden ilmoitusmallin luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ilmoitusmallit** ja valitse sitten liittyvä linkki.  
2.  Valitse **Ilmoitusmallit**-sivulla **Uusi**-toiminto.  
3.  Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Tunnista ilmoitusmalli.|  
    |**Kuvaus**|Kuvaa ilmoitusmallia.|  
    |**Ilmoitusmenetelmä**|Määritä, lähetetäänkö ilmoitus sähköpostitse vai muistiinpanona.|  
    |**Tyyppi**|Määritä liiketoimintaprosessi, johon ilmoitusta käytetään.<br /><br /> Valitse jokin seuraavista tyypeistä:<br /><br /> -   **Hyväksyntä** määrittää, että mallia käytetään ilmoittamaan käyttäjille hyväksynnän työnkuluista.<br />-   **Uusi tietue** määrittää, että mallia käytetään ilmoittamaan hyväksyjille uudesta tietueesta (kuten asiakaskortista), joka vaatii käyttäjän hyväksyntää.<br />-   **Erääntynyt** määrittää, että mallia käytetään ilmoittamaan käyttäjille myöhässä olevista hyväksyntäpyynnöistä.|  
    |**Oletus**|Määritä, käytetäänkö ilmoitusmallia oletuksena.|  

## <a name="to-modify-a-notification-template"></a>Ilmoitusmallin muokkaaminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ilmoitusmallit** ja valitse sitten liittyvä linkki.  
2.  Valitse **Ilmoitusmallit**-sivulla muokattava ilmoitusmalli.  
3.  Valitse **Vie mallin sisältö** -toiminto.  
4.  Valitse **Vie tiedosto** -sivulla **Tallenna**-painike. Nimeä HTML-tiedosto ja tallenna se sopivaan paikkaan.  
5.  Napsauta tiedostoa hiiren kakkospainikkeella, valitse **Avaa sovelluksessa** ja valitse sitten sopiva ohjelma.  

    > [!NOTE]  
    >  Sähköposti-tyyppisen ilmoitusmallien sisältö on HTML-muodossa. Muistiinpano-tyypin ilmoitusmallien sisältö on TXT-muodossa.  
6.  Muokkaa ilmoitusmallin sisältöä lisäämällä, muuttamalla tai poistamalla parametrimuuttujia. Tallenna tekemäsi muutokset. Lisätietoja on kohdassa "Ilmoitusmallien sisältö".  

    Jatka tuomalla muokattu sisältö takaisin samaan tai uuteen ilmoitusmalliin.  
7.  Jos haluat muokata vietyä ilmoitusmallia, valitse **Ilmoitusmallit**-sivulla sama malli, jonka valitsit vaiheessa 2.  

    Jos haluat tuoda muokatun mallin sisällön uuteen ilmoitusmalliin, seuraa kohdan "Uuden ilmoitusmallin luominen" ohjeita ja valitse uusi ilmoitusmalli.  
8.  Valitse **Tuo mallin sisältö** -toiminto.  
9. Jos muokkaat olemassa olevaa ilmoitusmallia, valitse **Kyllä** sanomassa, joka liittyy olemassa olevan mallin korvaamiseen.  
10. Valitse **Valitse tuotava tiedosto** -sivulla HTML-tiedosto, jota muokkasit vaiheessa 6 , ja valitse sitten **Avaa**-painike.  

Muokattu sisältö on nyt päivitetty **Ilmoitusmallit**-sivun aiemmin luotuun tai uuteen ilmoitusmalliin.  

### <a name="content-of-the-notification-templates"></a>Ilmoitusmallien sisältö  
Kolmen ilmoitusmallityypin (**Uusi tietue**, **Hyväksyntä** ja **Myöhässä**) sisällöt poikkeavat toisistaan.  

Parametriarvot lisätään automaattisesti ilmoituksiin ilmoitusmallin tyypin mukaan.  

#### <a name="new-record"></a>Uusi tietue  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Hyväksyntä  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Erääntynyt  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Katso myös  
 [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
 [Sähköpostin määrittäminen](admin-how-setup-email.md)   
 [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)   
 [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
 [Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md)   
 [Työnkulku](across-workflow.md)   
