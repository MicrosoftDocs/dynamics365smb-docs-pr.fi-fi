---
title: Hyväksyntätyönkulkuilmoitusten määrittäminen
description: 'Tässä artikkelissa kerrotaan, miten voit määrittää työnkulun ilmoitukset, jotka ilmoittavat käyttäjälle, että tapahtumaan on reagoitava ja työnkulun vastaus tarvitaan.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hyväksyntätyönkulkuilmoitukset

Määritä työnkulut ilmoittamaan käyttäjille automaattisesti, kun työnkulun vaihe vaatii heidän huomionsa. Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista.

Voit esimerkiksi määrittää, että hyväksyjäkäyttäjä Käyttäjä 2 saa ilmoituksen aina, kun Käyttäjä 1 pyytää hyväksyntää uudelle tietueelle. Seuraavassa työnkulun vaiheessa, kun käyttäjä 2 on hyväksynyt tietueen, käyttäjälle 3 ilmoitetaan ja hän voi aloittaa tietueen käsittelyn. Työnkulun hyväksyntäosavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään. Lisätietoja kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman oletusarvoinen versio tukee ilmoituksia sähköpostina tai sisäisinä muistiinpanoina.  

> [!IMPORTANT]  
> Kaikki työnkulun ilmoitukset lähetetään työjonon kautta. Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja että olet valinnut **Käynnistä automaattisesti palvelimelta** -valintaruudun. Lue lisätietoja kohdasta [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## Ilmoitusten määrittäminen

Työnkulun ilmoitusten osatekijöitä voi määrittää seuraavissa paikoissa:  

* Hyväksyjän ilmoitus

  Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -sivulla kullekin työnkulkuun osallistuvalle käyttäjälle.  

  Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 2. Lisätietoja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md). 
  
* Ilmoitusaikataulut

  Täyttämällä **Ilmoitusaikataulu**-sivu kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia. Lue lisätietoja kohdasta [Työnkulkuilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Sähköposti-ilmoitusten mukauttaminen

  Voit halutessasi mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla Raportti 1320:n sähköposti-ilmoitusta. Lue lisätietoja kohdasta [Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Jos haluat käyttää sähköpostia ilmoitusmenetelmänä, sinun on määritettävä sähköposti sekä lähettäjälle että vastaanottajalle [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa. Lisätietoja kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).
  
* Vastausvaihtoehdot

  Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua. Valitse muokkausasetukset **Työnkulun vastaukset** -sivulla sille työnkulun vastaukselle, joka edustaa ilmoitusta. Lue lisätietoja vaiheesta 9 [Työnkulkujen luominen](across-how-to-create-workflows.md#to-create-a-workflow) -osassa. 
  
* Ilmoita lähettäjälle

  Hyväksymistyönkuluille voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty. Lue lisätietoja vaiheesta 9 [Työnkulkujen luominen](across-how-to-create-workflows.md#to-create-a-workflow) -osassa.   

## Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulun käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md)  
[Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Sähköpostin määrittäminen](admin-how-setup-email.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
