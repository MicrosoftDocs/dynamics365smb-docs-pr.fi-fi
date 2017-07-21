---
title: Komponenttien hallinta tuoterakenteiden avulla| Microsoft Docs
description: "Kokoonpanon tuoterakenne luodaan määrittämään komponentit tai resurssit, joista koostetaan nimike, johon kokoonpanon tuoterakenne viittaa. Voit myös tarkastella kokoonpanonimikkeen komponentteja."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Toimintaohje: Tuoterakenteen käyttäminen
> [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyinen versio sisältää vain kokoonpanon hallintaominaisuuden ensimmäisen osan. Voit luoda nyt vain kokoonpanon tuoterakenteita ja käsitellä sitten liittyviä päänimikkeitä tavallisina varastonimikkeinä. Tulevan päivityksen jälkeen voit hallita nimikkeiden kokoamista osista joko kokoonpano varastoon tai kokoonpano tilauksiin työkuluissa. Voit myös myydä osia paketteina.

Voit käyttää tuoterakenteita jäsentämään päänimikkeitä, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuoterakennetta kutsutaan kokoonpanon tuoterakenteeksi. Kokoonpanon tuoterakenteet määrittävät, mitkä osat sisältyvät päänimikkeisiin. Tässä dokumentaatiossa päänimikettä kutsutaan kokoonpanonimikkeeksi.

Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää myös resursseja, joita tarvitaan niiden kokoamiseen.

Kokoonpanon tuoterakenteessa voi olla useita tasoja. Toisin sanoen kokoonpanon tuoterakenteen komponentti voi olla itsessään kokoonpanonimike. Siinä tapauksessa kokoonpanon tuoterakennerivillä olevassa **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.

Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta. Lisätietoja on ohjeaiheen [Toimintaohje: Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md) kohdassa Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa.

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [Financials-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Luo kokoonpanon tuoterakenne
Kokoonpanon tuoterakenne on luotava, jos haluat määrittää päänimikkeen, joka koostuu muista nimikkeistä ja mahdollisesti resursseista, joita tarvitaan päänimikkeen kokoamiseen.  

Kokoonpanon tuoterakenteen luomisessa on kaksi osaa:
- uuden nimikkeen määrittäminen
- kokoonpanonimikkeen tuoterakenteen määrittäminen.

1. Määritä uusi nimike. Lisätietoja on kohdassa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

    Jatka antamalla kokoonpanon tuoterakenteen osat tai resurssit.  
2. Valitse kokoonpanonimikkeen **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
3. Täytä **Kokoonpanon tuoterakenne** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Kokoonpanonimikkeen osien näyttäminen tuoterakenteen perusteella sisennettyinä
Voit avata **Kokoonpanon tuoterakenne** -ikkunassa erillisen ikkunan, joka näyttää osat ja resursseja sisennettynä kokoonpanonimikkeen alle niiden tuoterakenteen mukaisen sijainnin perusteella.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-ikkunan **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -ikkunassa **Näytä tuoterakenne** -toiminto.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Kokoonpanonimikkeiden ostaminen, myynti tai siirtäminen
Koska [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa kokoonpanon tuoterakenne voidaan määrittää ja liittää vain nimikkeille, voit käsitellä asiakirjarivien kokoonpanonimikkeitä vain tavallisina nimikkeinä.

**Varoitus**: Tuoterakenneosien varastomäärää ei muuteta, jos teet niin.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Toimintaohje: Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)     
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)

