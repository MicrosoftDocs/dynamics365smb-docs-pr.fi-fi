---
title: "Ilmoitusten vastaanottoajan ja -tavan määrittäminen | Microsoft Docs"
description: "Kun määrität käyttäjiä hyväksynnän työnkulkuihin, Ilmoituksen asetukset- ja Ilmoitusaikataulu-sivuilla on määritettävä miten ja milloin käyttäjät saavat ilmoituksia hyväksynnän työnkulun osavaiheista. Yksittäiset käyttäjät voivat muuttaa ilmoitusasetuksiaan valitsemalla Muuta ilmoitusasetuksia -painikkeen, joka näytetään kaikissa ilmoituksissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 8bb1b2815740e3acfeb984c1b7cbad160dcd1016
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen
Kun määrität käyttäjiä hyväksynnän työnkulkuihin, **Ilmoituksen asetukset**- ja **Ilmoitusaikataulu**-sivuilla on määritettävä miten ja milloin käyttäjät saavat ilmoituksia hyväksynnän työnkulun osavaiheista. Yksittäiset käyttäjät voivat muuttaa ilmoitusasetuksiaan valitsemalla **Muuta ilmoitusasetuksia** -painikkeen, joka näytetään kaikissa ilmoituksissa.  

 Ennen kuin voit määrittää hyväksynnän käyttäjän ilmoitusasetukset, käyttäjä on määritettävä hyväksynnän käyttäjäksi. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  

 Voit määrittää sähköposti-ilmoitusten asettelua muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin tai asiakirjan mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  

 Useat hyväksyntätyönkulun osavaiheet ilmoittavat käyttäjille toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena lähetetään ilmoitus käyttäjälle 2 (hyväksyjälle). Seuraavan työnkulun osavaiheen tapahtuma voi olla se, että käyttäjä 2 hyväksyy tietueen. Vastauksena lähetetään ilmoitus käyttäjälle 3, jotta hyväksytyn tietueen käsittely voidaan aloittaa. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Määritä, milloin ja miten käyttäjät saavat ilmoituksia  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse sen käyttäjän rivi, jonka ilmoitusasetukset haluat määrittää, ja valitse sitten **Ilmoitusasetukset**-toiminto.  
3.  Täytä **Ilmoituksen asetukset** -sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ilmoitustyyppi**|Määritä, minkälaiseen tapahtumaan ilmoitus liittyy.<br /><br /> Valitse jompikumpi seuraavista vaihtoehdoista:<br /><br /> -   **Uusi tietue** tarkoittaa, että ilmoitus koskee uutta tietuetta, kuten asiakirjaa, joka vaatii käyttäjän huomiota.<br />-   **Hyväksyntä** tarkoittaa, että ilmoitus koskee yhtä tai useampaa hyväksyntäpyyntöä.<br />-   **Myöhässä** tarkoittaa, että ilmoitus muistuttaa käyttäjiä, että tiettyä tapahtumaa ei ole huomioitu ajoissa.|  
    |**Ilmoitusmenetelmä**|Määritä, lähetetäänkö ilmoitus sähköpostitse vai sisäisenä huomautuksena.|

    Voit määrittää sähköposti-ilmoitusten asettelua muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin tai asiakirjan mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

    Olet nyt määrittänyt, miten käyttäjä saa ilmoituksia. Määritä seuraavaksi, milloin käyttäjä saa ilmoituksia.  

4.  Valitse **Ilmoitusaikataulu**-toiminto.  
5.  Täytä **Ilmoitusaikataulu**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Toistuminen**|Määritä toistumiskaava, jonka mukaan käyttäjä saa ilmoituksia.|  
    |**Aika**|Määritä, mihin kellonaikaan käyttäjä vastaanottaa ilmoitukset, kun **Toistuminen**-kentän arvo on jokin muu kuin **Heti**.|  
    |**Päivittäinen esiintymistiheys**|Määritä, minkälaisina päivinä käyttäjä saa ilmoituksia kun **Toistuminen**-kentän arvo on **Päivittäin**.<br /><br /> Valitse **Arkipäivisin**, jos haluat saada ilmoituksia jokaisena arkipäivänä. Valitse **Päivittäin**, jos haluat saada ilmoituksia jokaisena viikonpäivänä, myös viikonloppuisin.|  
    |**Maanantai** - **Sunnuntai**|Määritä, minä päivinä käyttäjä saa ilmoituksia kun **Toistuminen**-kentän arvo on **Viikoittain**.|  
    |**Kuukaudenpäivä**|Määritä, lähetetäänkö käyttäjälle ilmoituksia kuukauden ensimmäisenä, viimeisenä, tai tiettynä päivänä.|  
    |**Kuukausittaisen ilmoituksen pvm**|Määritä, minä kuun päivänä käyttäjä saa ilmoituksia kun **Kuukaudenpäivä** -kentän arvo on **Mukautettu**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Muuta, milloin ja miten saat ilmoituksia  
1.  Valitse jossain saamassasi sähköposti- tai viesti-ilmoituksessa olevaa **Muuta ilmoitusasetuksia** -painiketta.  
2.  Muuta ilmoitusasetuksiasi **Ilmoituksen asetukset** -sivulla edellä kuvattujen ohjeiden mukaisesti.  

## <a name="see-also"></a>Katso myös  
 [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
 [Raporttien tai asiakirjojen mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)   
 [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Työnkulkujen käyttäminen](across-use-workflows.md)

