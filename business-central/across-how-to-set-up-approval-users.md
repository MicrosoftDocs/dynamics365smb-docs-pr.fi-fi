---
title: Hyväksyjäasiakkaiden määrittäminen | Microsoft Docs
description: Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät. Voit myös määrittää Hyväksynnän käyttäjäasetukset -sivulla rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4775af4afa3d1e97ad15aa24a710ec4e27ef554e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "912630"
---
# <a name="set-up-approval-users"></a>Hyväksynnän käyttäjien määrittäminen
Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät. Voit myös määrittää **Hyväksynnän käyttäjäasetukset** -sivulla rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa.  

> [!NOTE]  
>  Hyväksynnän pyytäjät ja hyväksyjät on ensin määritettävä työnkulun käyttäjiksi **Työnkulun käyttäjäryhmä** -sivulla. Lisätietoja on kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  

 Kun olet määrittänyt hyväksynnän käyttäjät, voit määrittää työnkulun vastaukset hyväksynnän työnkuluille. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.  

> [!NOTE]  
>  Jos haluat määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin useat hyväksyntäketjun hyväksyjät ovat hyväksyneet sen, määritä hyväksyjien hierarkia. Käyttäjätunnukselle **Hyväksyjä** on määritettävä hyväksyjä **Hyväksynnän käyttäjäasetukset** -sivulla. Määritä hyväksyjät **Työnkulun käyttäjäryhmä** -hyväksyjätyypille **Työnkulun käyttäjäryhmät** -sivulla ja määritä hierarkia määrittämällä kullekin hyväksyjälle **Järjestysnro** -kentässä. Lisätietoja on tässä ohjeaiheessa ja kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  
>   
>  Voit määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin usea hyväksyjä on hyväksynyt sen, huolimatta hierarkiasta, määrittämällä tasainen työnkulun käyttäjäryhmän. Määritä hyväksyjät hyväksyjätyypille **Työnkulun käyttäjäryhmä** **Työnkulun käyttäjäryhmät** -sivulla ja määritä kullekin hyväksyjälle sama numero **Järjestysnro** -kentässä. Lisätietoja on kohdassa [Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Hyväksynnän käyttäjän määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2. Luo uusi rivi **Hyväksynnän käyttäjäasetukset** -sivulla ja täytä sitten kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjätunnus**|Valitse hyväksyntäprosessiin liittyvän käyttäjän tunnus.|  
    |**Myyjän/ostajan koodi**|Määritä käyttäjää vastaava myyjän tai ostajan koodi **Myyjän/ostajan koodi** -kenttään.<br /><br /> Yleensä **Myyjän/ostajan koodi** -kenttä täytetään, jos myyjä tai ostaja, joka on vastuussa asiakkaasta tai toimittajasta, on samalla henkilö, joka hyväksyy kyseessä olevat osto- tai myyntipyynnöt.|  
    |**Hyväksyjän tunnus**|Valitse sen hyväksyntäprosessiin liittyvän käyttäjän tunnus, jonka on hyväksyttävä **Käyttäjätunnus**-kentässä olevan käyttäjän pyynnöt.|  
    |**Myyntisumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin myyntiarvo, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.|  
    |**Rajaton myynnin hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä kaikki myyntipyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Myyntisumman hyväksymisraja** -kenttää.|  
    |**Ostosumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin ostoarvo, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.|  
    |**Rajaton ostojen hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä kaikki ostopyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Myyntisumman hyväksymisraja** -kenttää.|  
    |**Pyyntösumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin myyntitarjouksen summa, jonka **Käyttäjätunnus**-kenttään määritetty käyttäjä saa hyväksyä.<br /><br /> Jos haluat käyttää tätä kenttää, **Työnkulun vastaus** -sivulla olevan **Hyväksyjän rajatyyppi** -kentän valinnaksi on asetettava **Hyväksyjäketju**.|  
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
