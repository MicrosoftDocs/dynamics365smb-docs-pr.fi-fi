---
title: "Yrityksen ja ohjatun RapidStart-toiminnon määrittäminen | Microsoft Docs"
description: "Voit nopeasti määrittää uuden yrityksen, jonka olet luonut käyttämällä RapidStart Services -palvelun ohjattua määritystoimintoa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e0973c719381cb286a57335888e521d359fe232a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Yrityksen ja ohjatun RapidStart-toiminnon määrittäminen
Voit nopeasti määrittää uuden yrityksen, jonka olet luonut käyttämällä RapidStart Services -palvelun ohjattua määritystoimintoa.

Seuraavassa toimenpiteessä olet antanut asiakkaalle määrityspaketin, joka sitten asennetaan tietokoneeseen. Asiakas avaa uuden yrityksen, jolla ei ole asiakastietoja. Sinun tai asiakkaan tulee seurata vaiheita RapidStart Services -palvelun ohjatussa toiminnossa, jotka on kuvattu tähän menettelyyn, ja antaa perustiedot yrityksestä. Ohjattu toiminto tuo kokoonpanopaketin ja käyttää sitten pakettia yrityksessä.  

## <a name="to-configure-a-new-company"></a>Määritä uusi yritys  
1. Valitse RapidStart Services -käyttöönottajan roolikeskuksessa **Ohjattu RapidStart-toiminto** -toiminto.  
2. Laajenna **Vaihe 1** -pikavälilehti, joka sisältää uuden yrityksen yleiset tiedot. Kirjoita kenttiin uuden yrityksen tarvittavat tiedot. Ohjelmassa on yksi kenttä, joka on täytettävä, eli **Nimi**. Muut kentät ovat valinnaisia.  
3. Laajenna **Vaihe 2** -pikavälilehti, joka sisältää uuden yrityksen viestintä- ja yhteystiedot. Kirjoita kenttiin uuden yrityksen tarvittavat tiedot.
4. Laajenna **Vaihe 3** -pikavälilehti, joka sisältää uuden yrityksen pankkitilin ja maksujen tiedot. Kirjoita kenttiin uuden yrityksen tarvittavat tiedot.  
5. Laajenna **Vaihe 4**-pikavälilehti. Valitse **AssistEdit**-painike ja valitse haluamasi kokoonpanopaketti. Kokoonpanopaketin nimi tulee näkyviin. Sitten voit tehdä seuraavat toimet luetellussa järjestyksessä:  

    1. Käytä määritystä valitsemalla **Käytä pakettia** -toiminto. Tämä tuo kokoonpanopaketin ja käyttää paketin tietokantatietoja samanaikaisesti.  

    2. Tarkista määritykset sen jälkeen, kun ne on otettu käyttöön. Tämän vaihtoehdon avulla voit tarkistella määritystietoja ja yhteistyökumppanin toimittamia kyselylomakkeita sekä tuoda joitakin perustietoja, joita yrityksesi tarvitsee. Valitse **Määritystyökirja**-toiminto. Lisätietoja on Määrityskyselylomakkeen viimeisteleminen -osan kohdassa [Asiakkaan asetusarvojen kerääminen](admin-gather-customer-setup-values.md).  

6. Laajenna **Vaihe 5**-pikavälilehti. Määritä, minkä roolikeskuksen haluat uuden yrityksen oletusvalinnaksi.  

    > [!IMPORTANT]  
    >  Muuta vain roolikeskustasi, kun yrityksen määritykset ovat valmiit. Jos harkittavia ja muokattavia asetustietoja on lisää, jatka työskentelyä ensimmäiseksi määritystyökirjan parissa. Palaa sitten ohjattuun toimintoon ja päivitä roolikeskuksen profiili tai valitse **Täydelliset asetukset** -toiminto.

7. Valitse **OK**-painike.  
8. Voit varmistaa, että määritystiedot on otettu käyttöön uudessa yrityksessä, kun valitset ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, syötät **yrityksen tiedot** ja valitset aiheeseen liittyvän linkin.

**Yrityksen tiedot** -ikkunassa on tietoja, jotka olet määrittänyt.   

Olet nyt määrittänyt yrityksen ja ottanut tiedot käyttöön sitä varten.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)

