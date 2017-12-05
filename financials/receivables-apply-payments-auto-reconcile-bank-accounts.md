---
title: "Pankkitilien täsmäytystehtävät ja maksujen kohdistaminen liittyviin tapahtumiin | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan tehtävistä, joilla täsmäytetään pankki-, myyntisaamis- ja ostovelkatilit, kirjataan kassaanmaksut ja kassakulut sekä kohdistetaan maksut automaattisesti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: b12a298fd9dc8d03d04790debb7a66715cc96458
ms.contentlocale: fi-fi
ms.lasthandoff: 10/17/2017

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen
Pankin, myyntisaamisten ja ostovelkojen tilit on täsmäytettävä säännöllisesti kohdistamalla pankkiin tallennetut maksut niiden vastaaviin maksamattomiin laskuihin ja hyvityslaskuihin tai muihin avoimiin tapahtumiin [!INCLUDE[d365fin](includes/d365fin_long_md.md)]issa.  

Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen tai syötteen ja rekisteröimällä maksut nopeasti. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa automaattisia kohdistuksia, ennen kuin kirjaat päiväkirjan. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.  

Voit tuoda pankin tiliotteet pankkisyötteenä määrittämällä ensin Envestnet Yodlee -pankkisyötepalvelun ja linkittämällä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

Vaihtoehtoisesti voit käyttää pankkitietojen muuntopalvelua muuntaessasi minkä tahansa muotoisen pankin tiliotteen tietovirraksi, jonka voit tämän jälkeen tuoda [!INCLUDE[d365fin](includes/d365fin_long_md.md)]iin. Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuomalla tiliote. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Toimintaohjeet: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md) |
| Voit kohdistaa maksut manuaalisesti tarkastelemalla jokaisen kohdistetun tiedon tietoja ja ehdotuksia avoimista tapahtumista joihin maksut kohdistetaan. |[Toimintaohjeet: Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md) |
| Ratkaise maksut, joita ei voi kohdistaa automaattisesti niihin liittyviin avoimiin tapahtumiin. Syynä voi olla esimerkiksi se, että summat ovat erilaiset tai liittyvää tapahtumaa ei ole. |[Toimintaohje: Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Linkitä maksujen teksti tiettyyn asiakkaaseen, toimittajaan tai kirjanpitotileihin, jotta toistuvat käteiskuitit tai kulut kirjataan aina näille tileille, kun kohdistettavia asiakirjoja ei ole. |[Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

