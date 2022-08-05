---
title: Työnkulun käyttäjien määrittäminen
description: Työnkulussa jäseninä olevat käyttäjät on määritettävä Työnkulun käyttäjäryhmä -sivulla ennen kuin voit luoda työnkulun.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 187ff9bad2fb8bf320872759115e98b326b689c8
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130197"
---
# <a name="set-up-workflow-users"></a>Työnkulun käyttäjien määrittäminen

Työnkuluissa jäseninä olevat käyttäjät on määritettävä ennen kuin voit luoda työnkulun. On esimerkiksi pakollista määritellä ne henkilöt, jotka saavat ilmoituksen toimia työnkulun osavaiheilla.  

Käyttäjät määritellään työnkulun käyttäjäryhmiin **Työnkulun käyttäjäryhmä** -sivulla, jonka jälkeen käyttäjän numerot määritetään osaksi prosessin järjestystä, kuten hyväksyjäketjua.  

Työnkulun käyttäjät, jotka toimivat hyväksynnän pyytäjinä ja hyväksyjinä on myös määritettävä työnkulun käyttäjiksi **Hyväksynnän käyttäjäasetukset** -sivulla. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Jos haluat määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin useat hyväksyntäketjun hyväksyjät ovat hyväksyneet sen, määritä hyväksyjien hierarkia. Käyttäjätunnukselle **Hyväksyjä** on määritettävä hyväksyjä **Hyväksynnän käyttäjäasetukset** -sivulla. Määritä hyväksyjät **Työnkulun käyttäjäryhmä** -hyväksyjätyypille **Työnkulun käyttäjäryhmät** -sivulla ja määritä hierarkia määrittämällä kullekin hyväksyjälle **Järjestysnro** -kentässä. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md) ja seuraavassa osassa.  
>
> Voit määrittää, että hyväksymispyyntöä ei ole hyväksytty, ennen kuin usea hyväksyjä on hyväksynyt sen, huolimatta hierarkiasta, määrittämällä tasainen työnkulun käyttäjäryhmän. Määritä hyväksyjät hyväksyjätyypille **Työnkulun käyttäjäryhmä** **Työnkulun käyttäjäryhmät** -sivulla ja määritä kullekin hyväksyjälle sama numero **Järjestysnro** -kentässä. Lisätietoja on seuraavassa osassa.  

## <a name="to-set-up-a-workflow-user"></a>Työnkulun käyttäjän määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulun käyttäjäryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulun käyttäjäryhmä** -sivu avautuu.  
3. Anna **Koodi**-kentässä enintään 20 merkkiä pitkä työnkulun tunniste.  
4. Syötä **Kuvaus**-kenttään työnkulun kuvaus.  
5. Lisää soveltuvat arvot **Työnkulun käyttäjäryhmän jäsenet**-pikalomakkeen ensimmäisen rivin kenttiin seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjänimi**|Määritä työnkulkuun osaa ottava käyttäjä.<br /><br /> Käyttäjän on oltava olemassa **Käyttäjien määritys** -sivulla. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).|  
    |**Järjestysnro**|Määritä järjestys, jossa työnkulun käyttäjä osallistuu työnkulkuun suhteessa muihin käyttäjiin. Tätä kenttää voidaan käyttää, esimerkiksi määrittämään, milloin käyttäjä hyväksyy suhteessa muihin hyväksyjiin, kun käytät **työnkulun käyttäjäryhmä** -vaihtoehdon **Hyväksyjän tyyppi** -kenttää liittyvässä työnkulkuvastauksessa.<br /><br /> **VINKKI:** Jos haluat määrittää, että hyväksymispyyntö edellyttää usean samanarvoisen käyttäjän hyväksyntää (hierarkiasta riippumatta), määritä tasainen työnkulkuryhmä määrittämällä sama järjestysnumero kyseisille hyväksyjille.|  
6. Toista vaihe 5, jos haluat lisätä useampia työnkulun käyttäjiä ryhmään.  
7. Toista vaiheet 2-6, jos haluat luoda uusia työnkulun käyttäjäryhmiä.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-workflows/)

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulkujen määrittäminen](across-set-up-workflows.md)  
[Käytä työnkulkuja](across-use-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]