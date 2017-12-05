---
title: "Myyntisaamisten hallintatehtävien yleiskatsaus | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan tehtävistä, joilla hallitaan myyntisaamisia ja kohdistetaan maksuja asiakas- ja toimittajatapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: e8e6098cf6efe91153fe4e112cf3f6f6635032ed
ms.contentlocale: fi-fi
ms.lasthandoff: 10/17/2017

---
# <a name="managing-receivables"></a>Myyntisaamisten hallinta
Säännöllinen vaihe missä tahansa rahoituskierrossa on pankkitilien täsmäyttäminen, mikä edellyttää maksujen kohdistamista asiakas- tai toimittajatapahtumiin, jotta myyntilaskut tai ostohyvityslaskut voidaan sulkea.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa voi rekisteröidä maksut nopeasti **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen tai syötteen. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa täsmäytyksiä ennen päiväkirjan kirjaamista sekä sulkea tapahtumien pankkitilitapahtumia päiväkirjaan kirjauksen aikana. Pankkitili täsmäytetään, kun kaikki maksut on kohdistettu.

Maksuja voi kuitenkin kohdistaa ja pankkitilejä täsmäyttää myös muualla.  

* **Pankkitilin täsmäytystilaan** -ikkuna, josta voit myös tarkistaa tapahtumia. Lisätietoja on kohdassa [Toimintaohje: Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md).  
* Voit kohdistaa ja tarkistaa manuaalisesti **Maksurekisteröinti**-ikkunassa käteisenä, sekkinä tai pankkitapahtumana vastaanotetut maksut maksamattomia myyntiasiakirjoja vastaan. Huomaa, että tämä toiminto on käytettävissä vain myyntiasiakirjoja varten.  
* **Kassapäiväkirja**-ikkunassa, jossa vastaanotot kirjataan antamalla manuaalisesti maksurivi soveltuvaan pääkirjaan tai soveltuvalle asiakkaalle tai toiselle tilille. Voit kohdistaa vastaanoton tai hyvityksen yhteen avoimeen tapahtumaan tai useisiin avoimiin tapahtumiin, ennen kuin kirjaat kassapäiväkirjan. Voit tehdä kohdistuksen myös asiakastapahtumista.  

Toinen osa myyntisaamisten hallintaa on kerätä avoimet saldot, kuten viivästyskulut, ja lähettää muistutuksia. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa nämä toimet voi tehdä erilaisilla tavoilla. Lisätietoja on kohdassa [Toimintaohje: Avointen saldojen perintä](receivables-collect-outstanding-balances.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuodun pankin tiliotetiedoston tai syötteen perusteella. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Kohdista maksut avoimiin asiakasmaksuihin maksamattomien myyntiasiakirjojen luettelon manuaalisen tapahtuman perusteella. |[Toimintaohje: Asiakkaan maksujen täsmäyttäminen manuaalisesti maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Kirjaa asiakkaiden kassaanmaksut tai hyvitykset kassapäiväkirjaan ja kohdista asiakastapahtumat päiväkirjasta tai kirjatuista tapahtumakirjauksista. |[Toimintaohje: Asiakkaan maksujen täsmäyttäminen manuaalisesti](receivables-how-apply-sales-transactions-manually.md) |
| Asiakkaiden muistuttaminen erääntyneistä summista, koron laskeminen ja viivästyskululaskut sekä myyntireskontran hallinta. |[Toimintaohje: Avointen saldojen perintä](receivables-collect-outstanding-balances.md) |
|Varmista. että tiedät toimitettujen nimikkeiden kulut määrittämällä lisätyt nimikekulut, kuten nimikkeiden myynnin jälkeen syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.|[Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Toimintaohje: Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

