---
title: Työnkulkuilmoitusten määrittäminen
description: Tässä artikkelissa kerrotaan, miten voit määrittää työnkulun ilmoitukset, jotka ilmoittavat käyttäjälle, että tapahtumaan on reagoitava ja työnkulun vastaus tarvitaan.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 99c08769429eef51a1d52e142d455ccd227781c7
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130008"
---
# <a name="workflow-notifications"></a>Työnkulun ilmoitukset

Määritä työnkulut ilmoittamaan käyttäjille automaattisesti, kun työnkulun vaihe vaatii heidän huomionsa. Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista.

Voit esimerkiksi määrittää, että hyväksyjäkäyttäjä Käyttäjä 2 saa ilmoituksen aina, kun Käyttäjä1 pyytää hyväksyntää uudelle tietueelle. Seuraavassa työnkulun osavaiheessa Käyttäjä 3:lle ilmoitetaan, kun Käyttäjä 2 on hyväksynyt tietueen tietueen asianmukaisen käsittelyn aloittamista varten. Työnkulun hyväksyntäosavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman oletusarvoinen versio tukee ilmoituksia sähköpostina ja sisäisinä muistiinpanoina.  

> [!IMPORTANT]  
> Kaikki työnkulun ilmoitukset lähetetään työjonon kautta. Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja että **Käynnistä automaattisesti palvelimelta** -valintaruutu on valittu. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Ilmoitusten määrittäminen

Työnkulun ilmoitusten osatekijöitä voi määrittää seuraavissa paikoissa:  

* Hyväksyjän ilmoitus

    Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -sivulla kullekin työnkulkuun osallistuvalle käyttäjälle.  

    Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 2. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
* Ilmoitusaikataulut

    Täyttämällä **Ilmoitusaikataulu**-sivu kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Sähköposti-ilmoitusten mukauttaminen

    Voit halutessasi mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla Raportti 1320:n sähköposti-ilmoitusta. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Jos haluat käyttää sähköpostia ilmoitusmenetelmänä, sinun on määritettävä sähköposti sekä lähettäjälle että vastaanottajalle [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

* Vastausvaihtoehdot

    Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua. Valitse muokkausasetukset **Työnkulun vastaukset** -sivulla sille työnkulun vastaukselle, joka edustaa ilmoitusta. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md#to-create-a-workflow) vaiheessa 9.  

* Ilmoita lähettäjälle

    Hyväksymistyönkuluille voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty. Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md#to-create-a-workflow) vaiheessa 9.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-workflows/)

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)  
[Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Työnkulkujen luominen](across-how-to-create-workflows.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Sähköpostin määrittäminen](admin-how-setup-email.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]