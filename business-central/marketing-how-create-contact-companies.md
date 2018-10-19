---
title: Kontaktiyritysten luominen| Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten luodaan kontakti kullekin sellaiselle uudelle yritykselle tai mahdolliselle yritykselle, joiden kanssa olet vuorovaikutuksessa tai joihin sinulla on liikesuhde."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 64bef8820ec10bb293ccda88e7384d5d9e868e1f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="create-contact-companies"></a>Kontaktiyritysten luominen:
Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.

Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.

Ennen uuden kontaktin luomista kannattaa ehkä tarkistaa asetukset **Kontaktienhallinnan asetukset** -ikkunasta. Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Yrityksen kontaktin luominen alusta alkaen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Syötä **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-ikkunassa, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.  
4. Määritä **yrityksen** **tyyppi**.
5. Täytä tarvittaessa muut kentät.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä
Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.

> [!NOTE]  
>   Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa. Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -ikkunassa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä jokin seuraavista sen perusteella, missä haluat luoda kontakteja, ja valitse liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvassa erätyön ikkunassa **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

    Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -ikkunassa määritettyjen toimittajien suhde.

> [!TIP]  
>   Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Katso myös
[Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Liikesuhteiden liittäminen kontaktiin](marketing-business-relations.md#AssignBusRelContact)  
[Toimialaryhmien liittäminen kontaktiin](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Postitusryhmien liittäminen kontaktiin](marketing-mailing-groups.md#AssignMailGroupContact)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Business Central -sovelluksen käyttäminen](ui-work-product.md)

