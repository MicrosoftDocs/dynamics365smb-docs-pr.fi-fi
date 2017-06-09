---
title: Myyntisaamisten hallinta| Microsoft Docs
description: Myyntisaamisten hallinta
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62d59546331a5faa5ecb7aea0f9bb8dedea719f9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

