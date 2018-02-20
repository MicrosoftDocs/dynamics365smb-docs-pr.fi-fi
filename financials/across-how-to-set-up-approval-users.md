---
title: "Hyväksyjäasiakkaiden määrittäminen | Microsoft Docs"
description: "Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä työnkulun käyttäjät, jotka ovat osallisina hyväksymisprosesseissa. Voit myös määrittää Hyväksynnän käyttäjäasetukset -ikkunassa rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa."
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
ms.openlocfilehash: 708945a547f22bd132ea3c3b9529a4d05e63737d
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-approval-users"></a>Hyväksynnän käyttäjien määrittäminen
Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät. Voit myös määrittää **Hyväksynnän käyttäjäasetukset** -ikkunassa rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa.  

> [!NOTE]  
>  Hyväksynnän pyytäjät ja hyväksyjät on ensin määritettävä työnkulun käyttäjiksi **Työnkulun käyttäjäasetukset** -ikkunassa. Lisätietoja on kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  

 Kun olet määrittänyt hyväksynnän käyttäjät, voit määrittää työnkulun vastaukset hyväksynnän työnkuluille. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

> [!NOTE]  
>  Jos haluat määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin hyväksyntä-ketjussa usea hyväksyjä on hyväksynyt sen, määritä hyväksyjien hierarkia. Käyttäjätunnukselle **Hyväksyjä** on määritettävä hyväksyjä **Hyväksynnän käyttäjäasetukset** -ikkunassa. Määritä hyväksyjät hyväksyjätyypille **Työnkulun käyttäjäryhmä** **Työnkulun käyttäjäryhmät** -ikkunassa ja määritä hierarkia määrittämällä kullekin hyväksyjälle **Järjestysnro** -kentässä. Lisätietoja on tässä ohjeaiheessa ja kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  
>   
>  Voit määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin usea hyväksyjä on hyväksynyt sen, huolimatta hierarkiasta, määrittämällä tasainen työnkulun käyttäjäryhmän. Määritä hyväksyjät hyväksyjätyypille **Työnkulun käyttäjäryhmä** **Työnkulun käyttäjäryhmät** -ikkunassa ja määritä kullekin hyväksyjälle sama numero **Järjestysnro** -kentässä. Lisätietoja on kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Hyväksynnän käyttäjän määrittäminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Hyväksynnän käyttäjäasetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo uusi rivi **Hyväksynnän käyttäjäasetukset** -ikkunassa ja täytä sitten kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjätunnus**|Valitse hyväksyntäprosessiin liittyvän käyttäjän tunnus.|  
    |**Myyjän/ostajan koodi**|Määritä käyttäjää vastaava myyjän tai ostajan koodi **Myyjän/ostajan koodi** -kenttään.<br /><br /> Yleensä **Myyjän/ostajan koodi** -kenttä täytetään, jos myyjä tai ostaja, joka on vastuussa asiakkaasta tai toimittajasta, on samalla henkilö, joka hyväksyy kyseessä olevat osto- tai myyntipyynnöt.|  
    |**Hyväksyjän tunnus**|Valitse sen hyväksyntäprosessiin liittyvän käyttäjän tunnus, jonka on hyväksyttävä **Käyttäjätunnus**-kentässä olevan käyttäjän pyynnöt.|  
    |**Myyntisumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin myyntiarvo, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.|  
    |**Rajaton myynnin hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä kaikki myyntipyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Myyntisumman hyväksymisraja** -kenttää.|  
    |**Ostosumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin ostoarvo, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.|  
    |**Rajaton ostojen hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä kaikki ostopyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Myyntisumman hyväksymisraja** -kenttää.|  
    |**Pyyntösumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin myyntitarjouksen summa, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.<br /><br /> Jos haluat käyttää tätä kenttää, **Työnkulun vastaus** -ikkunassa olevan **Hyväksyjän rajatyyppi** -kentän valinnaksi on asetettava **Hyväksyjäketju**.|  
    |**Rajaton pyyntöjen hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä kaikki ostotarjoukset summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Pyyntösumman hyväksymisraja** -kenttää.|  
    |**Varahyväksyjä**|Valitse hyväksyntäprosessiin liittyvän käyttäjän tunnus, jonka on hyväksyttävä **Käyttäjätunnus** -kentässä olevan käyttäjän pyynnöt jos **Hyväksyjän tunnus** -kentässä oleva käyttäjä ei ole saatavilla. **Huomautus:** korvaava voi olla joko käyttäjä **Korvaava**-kentässä, suora hyväksyjä tai hyväksynnän järjestelmänvalvoja, tässä järjestyksessä. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).|  
    |**Sähköpostiosoite**|Määritä **Käyttäjätunnus**-kenttään syötetyn käyttäjän sähköpostiosoite.|  
    |**Hyväksynnän järjestelmänvalvoja**|Määritä käyttäjä, jolla on oikeus avata hyväksynnän työnkulkuja, esimerkiksi delegoimalla hyväksyntäpyyntöjä uusille korvaaville hyväksyjille tai poistamalla hyväksyntäpyyntöjä, joiden määräaika on ohi.|  

    > [!NOTE]  
    >  **Hyväksyjän rajatyyppi** -kenttä koskee vain sovellusalueita, joihin voi määrittää rajoituksia, tärkeimpinä myynnin ja ostojen hyväksynnät. Mikä tahansa muuntyyppinen hyväksyntä, jota rajoitukset eivät koske, käyttäytyy aina **Suora hyväksyjä** -vaihtoehdon mukaisesti.  

3. Voit testata hyväksyjäkäyttäjän asetukset valitsemalla **Hyväksynnän käyttäjien määrityksen testi** -toiminto.  
4. Toista vaiheet 2 ja 3 jokaiselle käyttäjälle, jonka haluat määrittää hyväksynnän käyttäjäksi.  

## <a name="see-also"></a>Katso myös  
[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)   
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
[Työnkulkujen luominen](across-how-to-create-workflows.md)   
[Työnkulkujen määrittäminen](across-set-up-workflows.md)   
[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Työnkulku](across-workflow.md)   

