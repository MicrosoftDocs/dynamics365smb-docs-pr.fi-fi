---
title: Työnkulun käyttäjien määrittäminen
description: Työnkulussa jäseninä olevat käyttäjät on määritettävä Työnkulun käyttäjäryhmä -sivulla ennen kuin voit luoda työnkulun.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Työnkulun käyttäjien määrittäminen

Työnkuluissa jäseninä olevat käyttäjät on määritettävä ennen kuin voit luoda hyväksyntätyönkulun. On esimerkiksi pakollista määritellä ne henkilöt, jotka saavat ilmoituksen toimia työnkulun osavaiheilla.  

Käyttäjät määritellään työnkulun käyttäjäryhmiin **Työnkulun käyttäjäryhmät** -sivulla, jonka jälkeen käyttäjän numerot voidaan määrittää osaksi prosessin järjestystä, kuten hyväksyjäketjua. 

Työnkulun käyttäjät, jotka toimivat hyväksynnän pyytäjinä ja hyväksyjinä on myös määritettävä työnkulun käyttäjiksi **Hyväksynnän käyttäjäasetukset** -sivulla. Lisätietoja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Jos haluat määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin käyttäjät ovat hyväksyneet sen, määritä hyväksyjien hierarkia. Käyttäjätunnukselle **Hyväksyjä** on määritettävä hyväksyjä **Hyväksynnän käyttäjäasetukset** -sivulla. Määritä hyväksyjät **Työnkulun käyttäjäryhmä** -hyväksyjätyypille **Työnkulun käyttäjäryhmät** -sivulla ja määritä hierarkia määrittämällä kullekin hyväksyjälle **Järjestysnro** -kentässä. Lisätietoja alla ja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md). 

## Työnkulun käyttäjän määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulun käyttäjäryhmät**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulun käyttäjäryhmä** -sivu avautuu.  
3. Anna **Koodi**-kentässä enintään 20 merkkiä pitkä työnkulun tunniste.  
4. Syötä **Kuvaus**-kenttään työnkulun kuvaus.  
5. Lisää soveltuvat arvot **Työnkulun käyttäjäryhmän jäsenet**-pikalomakkeen ensimmäisen rivin kenttiin seuraavassa taulukossa kuvatulla tavalla.  

   |Kenttä|Kuvaus|
   |-----|-----------|
   |**Käyttäjänimi**|Määritä työnkulkuun osaa ottava käyttäjä.<br /><br /> Käyttäjän on oltava olemassa **Käyttäjien määritys** -sivulla. Lisätietoja kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).|
   |**Järjestysnro**|Määritä järjestys, jossa työnkulun käyttäjä osallistuu työnkulkuun suhteessa muihin käyttäjiin. Tämä kenttä voi esimerkiksi määrittää, milloin käyttäjä hyväksyy suhteessa muihin hyväksyjiin määrittämällä **työnkulun käyttäjäryhmä** -vaihtoehdon **Hyväksyjän tyyppi** -kenttää liittyvässä työnkulkuvastauksessa.| 

   > [!TIP]
   > Jos haluat määrittää, että hyväksymispyyntö edellyttää usean samanarvoisen käyttäjän hyväksyntää (hierarkiasta riippumatta), määritä tasainen työnkulkuryhmä määrittämällä sama järjestysnumero kaikille kyseisille hyväksyjille.

6. Toista vaihe 5, jos haluat lisätä useampia työnkulun käyttäjiä työnkulun käyttäjäryhmään.  
7. Toista vaiheet 2-6, jos haluat luoda uusia työnkulun käyttäjäryhmiä.  

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-workflows/)

## Katso myös

[Hyväksyjäkäyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
