---
title: Työnkulkuilmoitusten vastaanoton ajankohdan ja tavan määrittäminen
description: Kun määrität käyttäjiä hyväksymistyönkuluissa, voit määrittää, miten ja milloin kukin hyväksynnän käyttäjä saa ilmoituksia.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 261e2908f7f7ed3a47a337b2c3f49d7c633f1cce
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522350"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Työnkulkuilmoitusten vastaanoton ajankohdan ja tavan määrittäminen
Kun määrität hyväksynnän käyttäjiä työnkuluissa, joissa jonkun on tarkoitus hyväksyä muutokset, kuten uusia tietueita luotaessa tai jonkun pyytäessä hyväksyntää, sinun on määritettävä miten hyväksynnän käyttäjälle ilmoitetaan ja miten. Voit esimerkiksi määrittää, että hyväksynnän käyttäjä saa välittömästi sähköpostiviestin, kun joku luo uuden asiakkaan. Vaihtoehtoisesti voit aikatauluttaa toimitettavat ilmoitukset esimerkiksi viikko- tai kuukausiperusteisesti.

Ihmiset voivat muuttaa ilmoitusasetuksiaan valitsemalla **Muuta ilmoitusasetuksia** -painikkeen, joka näytetään kaikissa ilmoituksissa.  

> [!NOTE]
> Ilmoitukset toimitetaan vastaanottajan, ei lähettäjän, ilmoitusasetusten mukaisesti. Tämä on tärkeä ero, koska se tarkoittaa sitä, että kun joku pyytää hyväksyntää osana työnkulkua, pyyntöä ei välttämättä lähetetä heti. Sen sijaan se toimitetaan hyväksyjän ilmoitusasetuksissa määritetyn ilmoitusaikataulun mukaisesti. 

Ennen kuin voit määrittää hyväksynnän käyttäjän ilmoitusasetukset, käyttäjä on määritettävä hyväksynnän käyttäjäksi. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  

Voit määrittää sähköposti-ilmoitusten asettelua muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Jos haluat käyttää sähköpostia ilmoitusmenetelmänä, sinun on määritettävä sähköposti sekä lähettäjälle että vastaanottajalle [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Työkulun vaiheet 
Useat hyväksyntätyönkulun osavaiheet ilmoittavat käyttäjille toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena lähetetään ilmoitus käyttäjälle 2 (hyväksyjälle). Seuraavan työnkulun osavaiheen tapahtuma voi olla se, että käyttäjä 2 hyväksyy tietueen. Vastauksena lähetetään ilmoitus käyttäjälle 3, jotta hyväksytyn tietueen käsittely voidaan aloittaa. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Määritä, milloin ja miten käyttäjät saavat ilmoituksia  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten vastaava linkki.  
2.  Valitse sen käyttäjän rivi, jonka ilmoitusasetukset haluat määrittää, ja valitse sitten **Ilmoitusasetukset**-toiminto.  
3.  Täytä **Ilmoituksen asetukset** -sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    > [!NOTE]
    > Jos avaat **Hyväksynnän käyttäjäasetukset** -sivun **Ilmoitusasetukset**-sivun, ilmoituksen asetukset yhdistetään hyväksynnän käyttäjälle. Hyväksynnän käyttäjä saa työnkulkuilmoituksia aina kyseisten ilmoitusasetusten mukaisesti. Jos avaat **Ilmoitusasetukset**-sivun Kerro, mitä haluat tehdä -toiminnolla, ilmoitusasetukset otetaan käyttöön kaikilla käyttäjillä.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Ilmoitustyyppi**|Määritä, minkälaiseen tapahtumaan ilmoitus liittyy.<br /><br /> Valitse jompikumpi seuraavista vaihtoehdoista:<br /><br /> -   **Uusi tietue** tarkoittaa, että ilmoitus koskee uutta tietuetta, kuten asiakirjaa, joka vaatii käyttäjän huomiota.<br />-   **Hyväksyntä** tarkoittaa, että ilmoitus koskee yhtä tai useampaa hyväksyntäpyyntöä.<br />-   **Myöhässä** tarkoittaa, että ilmoitus muistuttaa käyttäjiä, että tiettyä tapahtumaa ei ole huomioitu ajoissa.|  
    |**Ilmoitusmenetelmä**|Määritä, lähetetäänkö ilmoitus sähköpostitse vai sisäisenä huomautuksena.|

    Voit määrittää sähköposti-ilmoitusten asettelua muokkaamalla raportin 1320 sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

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
 [Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)   
 [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Käytä työnkulkuja](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]