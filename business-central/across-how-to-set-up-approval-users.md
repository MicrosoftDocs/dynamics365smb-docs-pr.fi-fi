---
title: Hyväksynnän käyttäjien määrittäminen
description: 'Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät.'
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hyväksynnän käyttäjien määrittäminen

Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat käyttäjät **Hyväksynnän käyttäjäasetukset** -sivulla. Voit myös määrittää määrärajoja erityyppisille pyynnöille, määrittää korvaavia hyväksyjiä ja määrittää ilmoituksia.  

Kun olet määrittänyt hyväksynnän käyttäjät, voit määrittää työnkulun vastaukset hyväksynnän työnkuluille. Lisätietoja on kohdassa [Hyväksyntätyönkulkujen luominen](across-how-to-create-workflows.md).  

> [!TIP]
> Voit edellyttää, että useat hyväksyjät reagoivat hyväksymispyyntöön luomalla hyväksyjien ryhmän **Työnkulun käyttäjäryhmä** -sivulla. Lisätietoja kohdassa [Työnkulun käyttäjäryhmien määrittäminen](across-how-to-set-up-workflow-users.md).  

## Hyväksynnän käyttäjän määrittäminen

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset**, valitse sitten vastaava linkki.  
2. Luo uusi rivi **Hyväksynnän käyttäjäasetukset** -sivulla ja täytä sitten kentät seuraavassa taulukossa kuvatulla tavalla.  

   |Kenttä|Kuvaus|
   |-----|-----------|
   |**Käyttäjätunnus**|Valitse hyväksyntäprosessiin liittyvän henkilön tunnus.|
   |**Myyjän/ostajan koodi**|Määritä käyttäjää vastaava myyjän tai ostajan koodi.<br /><br /> Yleensä **Myyjän/ostajan koodi** -kenttä täytetään, jos myyjä tai ostaja, joka on vastuussa asiakkaasta tai toimittajasta, on samalla henkilö, joka hyväksyy osto- tai myyntipyynnöt.|
   |**Hyväksyjän tunnus**|Valitse sen hyväksyntäprosessiin liittyvän henkilön tunnus, jonka on hyväksyttävä **Käyttäjätunnus**-kentässä määritetyn henkilön pyynnöt.|
   |**Myyntisumman hyväksymisraja**|Määritä paikallisessa valuutassa (PVA) suurin myyntiarvo, jonka **Käyttäjätunnus**-kentässä valittu henkilö saa hyväksyä.|
   |**Rajaton myynnin hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty henkilö saa hyväksyä kaikki myyntipyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Myyntisumman hyväksymisraja** -kenttää.|
   |**Ostosumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin ostosumma, jonka **Käyttäjätunnus**-kenttään määritetty henkilö saa hyväksyä.|
   |**Rajaton ostojen hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty henkilö saa hyväksyä kaikki ostopyynnöt summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Ostosumman hyväksymisraja** -kenttää.|
   |**Pyyntösumman hyväksymisraja**|Määritä paikallisessa rahayksikössä suurin myyntitarjouksen summa, jonka **Käyttäjätunnus**-kenttään määritetty henkilö saa hyväksyä.<br /><br /> Jos haluat käyttää tätä kenttää, **Työnkulun vastaus** -sivulla olevan **Hyväksyjän rajatyyppi** -kentän valinnaksi on asetettava **Hyväksyjäketju**.|
   |**Rajaton pyyntöjen hyväksyntä**|Määritä, että **Käyttäjätunnus**-kenttään määritetty henkilö saa hyväksyä kaikki ostotarjoukset summasta riippumatta.<br /><br /> Jos valitset tämän valintaruudun, et voi täyttää **Pyyntösumman hyväksymisraja** -kenttää.|
   |**Varahyväksyjä**|Valitse hyväksyntäprosessiin liittyvän henkilön tunnus, jonka on hyväksyttävä **Käyttäjätunnus** -kentässä olevan henkilön pyynnöt jos **Hyväksyjän tunnus** -kentässä oleva käyttäjä ei ole saatavilla. <br /><br />**Huomautus:** korvaava voi olla joko käyttäjä **Korvaava**-kentässä, suora hyväksyjä tai hyväksynnän järjestelmänvalvoja, tässä järjestyksessä. Lisätietoja on kohdassa [Hyväksyntätyönkulkujen käyttäminen](across-how-use-approval-workflows.md).|
   |**Sähköpostiosoite**|Määritä **Käyttäjätunnus**-kenttään syötetyn henkilön sähköpostiosoite.|
   |**Hyväksynnän järjestelmänvalvoja**|Määritä käyttäjä, jolla on oikeus avata hyväksynnän työnkulku, kuten delegoimalla hyväksyntäpyyntöjä uusille korvaaville hyväksyjille tai poistamalla hyväksyntäpyyntöjä, joiden määräaika on ohi.<br /><br />**Huomautus** Vain yksi henkilö voi olla hyväksynnän järjestelmänvalvoja.|

3. Voit testata hyväksyjäkäyttäjän asetukset valitsemalla **Hyväksynnän käyttäjien määrityksen testi** -toiminto.  
4. Toista vaiheet 2 ja 3 jokaiselle henkilölle, jonka haluat määrittää hyväksynnän käyttäjäksi.  

Seuraava askel on määrittää, miten haluat [!INCLUDE [prod_short](includes/prod_short.md)]in ilmoittavan käyttäjille, että pyyntö on odottamassa heidän huomiotaan. Lisätietoja: [Hyväksyntätyönkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).

## Katso myös

[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
