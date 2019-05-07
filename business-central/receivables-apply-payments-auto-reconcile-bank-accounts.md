---
title: Pankkitilien täsmäyttäminen ja maksujen kohdistaminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan tehtävistä, joilla täsmäytetään pankki-, myyntisaamis- ja ostovelkatilit, kirjataan kassaanmaksut ja kassakulut sekä kohdistetaan maksut automaattisesti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 124b3e82a38af375128353d977cc250aa9f94cf8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "921653"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen
Pankin, myyntisaamisten ja ostovelkojen tilit on täsmäytettävä säännöllisesti kohdistamalla pankkiin tallennetut maksut niiden vastaaviin maksamattomiin laskuihin ja hyvityslaskuihin tai muihin avoimiin tapahtumiin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla tuomalla pankin tiliotteen tai syötteen ja rekisteröimällä maksut nopeasti. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa automaattisia kohdistuksia, ennen kuin kirjaat päiväkirjan. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

Voit täsmäyttää pankkitilejä myös niin, että maksuja ei kohdisteta samanaikaisesti. Voit tehdä tämän **Pankkitilin täsmäytys** -sivulla. Lisätietoja on kohdassa [Pankkitilin täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md).   

Voit tuoda pankin tiliotteet pankkisyötteenä määrittämällä ensin Envestnet Yodlee -pankkisyötepalvelun ja linkittämällä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

Vaihtoehtoisesti voit käyttää pankkitietojen muuntopalvelua muuntaessasi minkä tahansa muotoisen pankin tiliotteen tietovirraksi, jonka voit tämän jälkeen tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja on kohdassa [Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuomalla tiliote. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md) |
| Voit kohdistaa maksut manuaalisesti tarkastelemalla jokaisen kohdistetun tiedon tietoja ja ehdotuksia avoimista tapahtumista joihin maksut kohdistetaan. |[Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md) |
| Ratkaise maksut, joita ei voi kohdistaa automaattisesti niihin liittyviin avoimiin tapahtumiin. Syynä voi olla esimerkiksi se, että summat ovat erilaiset tai liittyvää tapahtumaa ei ole. |[Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Linkitä maksujen teksti tiettyyn asiakkaaseen, toimittajaan tai kirjanpitotileihin, jotta toistuvat käteiskuitit tai kulut kirjataan aina näille tileille, kun kohdistettavia asiakirjoja ei ole. |[Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
