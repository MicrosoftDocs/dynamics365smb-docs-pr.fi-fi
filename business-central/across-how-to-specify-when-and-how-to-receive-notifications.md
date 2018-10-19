---
title: "Ilmoitusten vastaanottoajan ja -tavan määrittäminen | Microsoft Docs"
description: "Kun määrität käyttäjiä hyväksynnän työnkulkuihin, Ilmoituksen asetukset ja Ilmoitusaikataulu-ikkunoissa on määritettävä miten ja milloin käyttäjät saavat ilmoituksia hyväksynnän työnkulun osavaiheista. Yksittäiset käyttäjät voivat muuttaa ilmoitusasetuksiaan valitsemalla Muuta ilmoitusasetuksia -painikkeen, joka näytetään kaikissa ilmoituksissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 714ebd289407293f2a9fb8f05cad68330c79ad9a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen
Kun määrität käyttäjiä hyväksynnän työnkulkuihin, **Ilmoituksen asetukset** ja **Ilmoitusaikataulu**-ikkunoissa on määritettävä miten ja milloin käyttäjät saavat ilmoituksia hyväksynnän työnkulun osavaiheista. Yksittäiset käyttäjät voivat muuttaa ilmoitusasetuksiaan valitsemalla **Muuta ilmoitusasetuksia** -painikkeen, joka näytetään kaikissa ilmoituksissa.  

 Ennen kuin voit määrittää hyväksynnän käyttäjän ilmoitusasetukset, käyttäjä on määritettävä hyväksynnän käyttäjäksi. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  

 Ilmoitusten asettelu ja sisältö määritetään ilmoitusmalleilla. Lisätietoja on kohdassa [Ilmoitusmallien hallinta](across-how-to-manage-notification-templates.md).  

 Useat hyväksyntätyönkulun osavaiheet ilmoittavat käyttäjille toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena lähetetään ilmoitus käyttäjälle 2 (hyväksyjälle). Seuraavan työnkulun osavaiheen tapahtuma voi olla se, että käyttäjä 2 hyväksyy tietueen. Vastauksena lähetetään ilmoitus käyttäjälle 3, jotta hyväksytyn tietueen käsittely voidaan aloittaa. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Määritä, milloin ja miten käyttäjät saavat ilmoituksia  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse sen käyttäjän rivi, jonka ilmoitusasetukset haluat määrittää, ja valitse sitten **Ilmoitusasetukset**-toiminto.  
3.  Täytä **Ilmoituksen asetukset** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ilmoitustyyppi**|Määritä, minkälaiseen tapahtumaan ilmoitus liittyy.<br /><br /> Valitse jompikumpi seuraavista vaihtoehdoista:<br /><br /> -   **Uusi tietue** tarkoittaa, että ilmoitus koskee uutta tietuetta, kuten asiakirjaa, joka vaatii käyttäjän huomiota.<br />-   **Hyväksyntä** tarkoittaa, että ilmoitus koskee yhtä tai useampaa hyväksyntäpyyntöä.<br />-   **Myöhässä** tarkoittaa, että ilmoitus muistuttaa käyttäjiä, että tiettyä tapahtumaa ei ole huomioitu ajoissa.|  
    |**Ilmoitusmallin koodit**|Määritä ilmoitusmallin koodi, jota käytetään käyttäjän ilmoitusten luonnissa.|  
    |**Yhdistämättömät ilmoitukset**|Määritä, lähetetäänkö käyttäjälle yksi ilmoitus jokaista tapahtumaa kohti vai koostettuja ilmoituksia.<br /><br /> Jos **Yhdistämättömät ilmoitukset** -valintaruutua ei ole valittu, käyttäjä saa ilmoituksia, joihin on koottu tietoja tapahtumista, jotka tapahtuvat samalla toistumiskaavalla ilmoitusjakson aikana.|  

     Olet nyt määrittänyt, miten käyttäjä saa ilmoituksia. Määritä seuraavaksi, milloin käyttäjä saa ilmoituksia.  

4.  Valitse **Ilmoitusaikataulu**-toiminto.  
5.  Täytä **Ilmoitusaikataulu**-ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

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
2.  Muuta ilmoitusasetuksiasi **Ilmoituksen asetukset** -ikkunassa edellä kuvattujen ohjeiden mukaisesti.  

## <a name="see-also"></a>Katso myös  
 [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
 [Ilmoitusmallien hallinta](across-how-to-manage-notification-templates.md)   
 [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Työnkulkujen käyttäminen](across-use-workflows.md)

