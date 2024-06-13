---
title: Työnkulun käyttäjien määrittäminen
description: Työnkulussa jäseninä olevat käyttäjät on määritettävä Hyväksynnän käyttäjäasetukset -sivulla ennen kuin voit luoda työnkulun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Työnkulun käyttäjien järjestyksen määrittäminen

Ennen kuin voit luoda hyväksyntätyönkulun, on määritettävä käyttäjät jotka lähettävät pyyntöjä sekä pyyntöjen hyväksyjät. Voit esimerkiksi määrittää ne henkilöt, jotka saavat ilmoituksen toimia työnkulun osavaiheissa. Hyväksyntätyönkulun osallistujat määritetään **Hyväksynnän käyttäjäasetukset** -sivulla. Lisätietoja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).

**Työnkulun käyttäjäryhmät** -sivulla voit määrittää, missä osallistuja osallistuu hyväksyntätyönkulkuun syöttämällä numeron **Järjestysnumero**-kenttään. -kentässä. Voit esimerkiksi määrittää, että käyttäjät osallistuvat peräkkäisessä järjestyksessä, kuten hyväksyjien ketjussa. Voit myös määrittää samanarvoisten hyväksyjien luettelon syöttämällä saman numeron. Jälkimmäisessä tapauksessa vain yhden hyväksyjän täytyy hyväksyä pyyntö.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Työnkulun käyttäjäryhmän määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulun käyttäjäryhmät**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulun käyttäjäryhmä** -sivu avautuu.  
3. Anna **Koodi**-kentässä enintään 20 merkkiä pitkä työnkulun tunniste.  
4. Syötä **Kuvaus**-kenttään työnkulun kuvaus.  
5. Lisää soveltuvat arvot **Työnkulun käyttäjäryhmän jäsenet**-pikalomakkeen ensimmäisen rivin kenttiin seuraavassa taulukossa kuvatulla tavalla.  

   |Kenttä|Kuvaus|
   |-----|-----------|
   |**Käyttäjätunnus**|Määritä työnkulkuun osallistuva käyttäjä.<br /><br /> Käyttäjän on oltava olemassa **Käyttäjien määritys** -sivulla. Lisätietoja kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).|
   |**Järjestysnro**|Määritä järjestys, jossa työnkulun käyttäjä osallistuu työnkulkuun suhteessa muihin käyttäjiin. Tämä kenttä voi esimerkiksi määrittää, milloin käyttäjä hyväksyy suhteessa muihin hyväksyjiin määrittämällä **työnkulun käyttäjäryhmä** -vaihtoehdon **Hyväksyjän tyyppi** -kenttää liittyvässä työnkulkuvastauksessa.|

   > [!NOTE]
   > Tavallisesti järjestysnumerot ovat peräkkäisiä työnkulun käyttäjäryhmässä oleville käyttäjille. Usealla käyttäjällä voi kuitenkin olla sama järjestysnumero. Tällöin vain toisen käyttäjän on hyväksyttävä pyyntö, ennen kuin työnkulku siirtyy seuraavaan vaiheeseen. Jos esimerkiksi käyttäjät A ja B ovat molemmat järjestyksessä numero kaksi, työnkulku siirtyy vaiheeseen 3, kun käyttäjä A tai B hyväksyy pyynnön.
6. Toista vaihe 5, jos haluat lisätä useampia työnkulun käyttäjiä työnkulun käyttäjäryhmään.  

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
