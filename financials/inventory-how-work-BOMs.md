---
title: "Toimintaohje: Tuoterakenteiden käyttäminen| Microsoft Docs"
description: "Kokoonpanon tuoterakenteet määrittävät, mitä komponentteja tai resursseja tarvitaan kokoonpanon tuoterakenteen edustavan nimikkeen valmistamiseen. Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää yhden tai useamman resurssin, jotka suorittavat kokoonpanotyön."
services: project-madeira
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
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: fi-fi
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Toimintaohje: Tuoterakenteen käyttäminen
**Huomautus**: [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyinen versio sisältää vain kokoonpanon hallintaominaisuuden ensimmäisen osan. Voit luoda nyt vain kokoonpanon tuoterakenteita ja käsitellä sitten liittyviä päänimikkeitä tavallisina varastonimikkeinä. Tulevan päivityksen jälkeen voit hallita nimikkeiden kokoamista osista joko kokoonpano varastoon tai kokoonpano tilauksiin työkuluissa. Voit myös myydä osia paketteina.

Voit käyttää tuoterakenteita jäsentämään päänimikkeitä, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuoterakennetta kutsutaan kokoonpanon tuoterakenteeksi. Kokoonpanon tuoterakenteet määrittävät, mitkä osat sisältyvät päänimikkeisiin. Tässä dokumentaatiossa päänimikettä kutsutaan kokoonpanonimikkeeksi.

Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää myös resursseja, joita tarvitaan niiden kokoamiseen.

Kokoonpanon tuoterakenteessa voi olla useita tasoja. Toisin sanoen kokoonpanon tuoterakenteen komponentti voi olla itsessään kokoonpanonimike. Siinä tapauksessa kokoonpanon tuoterakennerivillä olevassa **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.

Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta. Lisätietoja on [Toimintaohjeen: Saatavuuden yleiskuva](inventory-how-availability-overview.md) kohdassa Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa.

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [Financials-kokemuksen mukauttaminen](ui-experiences.md).

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

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-ikkunan **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -ikkunassa **Näytä tuoterakenne** -toiminto.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Kokoonpanonimikkeiden ostaminen, myynti tai siirtäminen
Koska [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa kokoonpanon tuoterakenne voidaan määrittää ja liittää vain nimikkeille, voit käsitellä asiakirjarivien kokoonpanonimikkeitä vain tavallisina nimikkeinä.

**Varoitus**: Tuoterakenneosien varastomäärää ei muuteta, jos teet niin.

## <a name="see-also"></a>Katso myös
[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Toimintaohje: Saatavuuden yleiskuva](inventory-how-availability-overview.md)     
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)

