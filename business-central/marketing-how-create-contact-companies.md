---
title: Kontaktiyritysten luominen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten luodaan kontakti kullekin sellaiselle uudelle yritykselle tai mahdolliselle yritykselle, joiden kanssa olet vuorovaikutuksessa tai joihin sinulla on liikesuhde.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "920980"
---
# <a name="create-contacts"></a>Kontaktien luominen
Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.

Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.

## <a name="create-a-company-contact-from-scratch"></a>Yrityksen kontaktin luominen alusta alkaen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Syötä **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.  
4. Määritä **yrityksen** **tyyppi**.
5. Täytä tarvittaessa muut kentät.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä
Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.

> [!NOTE]  
>   Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivulla. Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä jokin seuraavista sen perusteella, missä haluat luoda kontakteja, ja valitse liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvalla erätyön sivulla **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

    Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -sivulla määritettyjen toimittajien suhde.

> [!TIP]  
>   Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Katso myös
[Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Liikesuhteiden liittäminen kontaktiin](marketing-business-relations.md#AssignBusRelContact)  
[Toimialaryhmien liittäminen kontaktiin](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Postitusryhmien liittäminen kontaktiin](marketing-mailing-groups.md#AssignMailGroupContact)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Business Central -sovelluksen käyttäminen](ui-work-product.md)
