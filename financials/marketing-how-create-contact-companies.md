---
title: Kontaktiyritysten luominen | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten kontaktiyrityksiä luodaan Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-companies"></a>Kontaktiyritysten luominen:
Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.

Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.

Ennen uuden kontaktin luomista kannattaa ehkä tarkistaa asetukset **Kontaktienhallinnan asetukset** -ikkunasta. Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Yrityksen kontaktin luominen alusta alkaen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Syötä **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-ikkunassa, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.  
4. Määritä **yrityksen** **tyyppi**.
5. Täytä tarvittaessa muut kentät.

## <a name="create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä
Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.

**Huomautus**: Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa. Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita jokin seuraavista sen mukaan, missä haluat luoda kontaktit, ja valitse sitten liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvassa erätyön ikkunassa **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

    Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -ikkunassa määritettyjen toimittajien suhde.

**Vihje**: Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Katso myös
[Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Liikesuhteiden liittäminen kontaktiin](marketing-business-relations.md#AssignBusRelContact)  
[Toimialaryhmien liittäminen kontaktiin](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Postitusryhmien liittäminen kontaktiin](marketing-mailing-groups.md#AssignMailGroupContact)  
[Toimintaohjeet: Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Financialsin käyttäminen](ui-work-product.md)

