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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fd26f288ee6128539c9a8dd415d98126d693c3fe
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926620"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen
Pankin, myyntisaamisten ja ostovelkojen tilit on täsmäytettävä säännöllisesti kohdistamalla pankkiin tallennetut maksut niiden vastaaviin avoimiin (maksamattomiin) laskuihin ja hyvityslaskuihin tai muihin avoimiin tapahtumiin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla tuomalla esimerkiksi pankin tiliotteen tai syötteen maksujen nopeaa rekisteröintiä varten. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa automaattisia kohdistuksia, ennen kuin kirjaat päiväkirjan. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

Logiikka, joka ohjaa sitä, miten maksuteksti täsmäytetään automaattisesti tapahtumatietojen kanssa, määritetään **Maksusovelluksen säännöt** -sivulla useina priorisoituina sääntöinä, joita voi muokata.

Voit täsmäyttää pankkitilejä myös niin, että maksuja ei kohdisteta samanaikaisesti. Voit tehdä tämän **Pankkitilin täsmäytys** -sivulla. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).   

Voit tuoda pankin tiliotteet pankkisyötteenä määrittämällä ensin Envestnet Yodlee Bank Feeds -palvelun ja linkittämällä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

Vaihtoehtoisesti voit käyttää AMC Banking 365 Fundamentals -laajennusta muuntamaan tiliotteen tiedostomuodosta riippumatta tietovirraksi, jonka voit tämän jälkeen tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuomalla tiliote. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md) |
| Voit kohdistaa maksut manuaalisesti tarkastelemalla jokaisen kohdistetun tiedon tietoja ja ehdotuksia avoimista tapahtumista joihin maksut kohdistetaan. |[Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md) |
| Ratkaise maksut, joita ei voi kohdistaa automaattisesti niihin liittyviin avoimiin tapahtumiin. Syynä voi olla esimerkiksi se, että summat ovat erilaiset tai liittyvää tapahtumaa ei ole. |[Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Linkitä maksujen teksti tiettyyn asiakkaaseen, toimittajaan tai kirjanpitotileihin, jotta toistuvat käteiskuitit tai kulut kirjataan aina näille tileille, kun kohdistettavia asiakirjoja ei ole. |[Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Määritä säännöt, jotka hallinnoivat sitä, kuinka maksuja/pankkitapahtumia sovelletaan automaattisesti niihin liittyviin avoimiin kirjanpitotapahtumiin, kun käytät **Sovella automaattisesti** -toimintoa **Maksujen täsmäytyskirjauskansio** -sivulla.|[Automaattinen maksujen soveltamisen sääntöjen määrittäminen](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Pankkitilien täsmäytys](bank-how-reconcile-bank-accounts-separately.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
