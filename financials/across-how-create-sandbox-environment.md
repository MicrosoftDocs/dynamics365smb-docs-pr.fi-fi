---
title: "Sandbox-ympäristön luominen | Microsoft Docs"
description: "Luo tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten sopiva ympäristö."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d7bcb866d5f69e77e5a175d0b73e8ac03cf09d98
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="how-to-create-a-sandbox-environment"></a>Toimintaohje: Sandbox-ympäristön luominen
Sandbox-ympäristö (esiversio) on [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuotantoympäristöön kuulumaton ilmentymä. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.

## <a name="to-create-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Tarvitse sandbox-ympäristön luontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen. Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.

1. Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.
2. Valitse ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, kirjoita **Sandbox-ympäristö** ja valitse liittyvä linkki.
![Sandbox-ympäristön määrittäminen](./media/across-sandbox/sandbox-environment-setup.png)
3. Valitse **Luo**.  
  Selaimeen avautuu uusi välilehti, jossa voi viimeistellä sandbox-ympäristön määrittämisen.
> [!NOTE]  
>  Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan financials.dynamics.com-osoitteen URL-osoitteet.   

4. Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.
![Sandbox-ympäristön ohjattu aloitustoiminto](./media/across-sandbox/sandbox-wizard.png)

5. Valitse **Lisätietoja**, jos haluat lukea skenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse sen sijaan **Sulje**, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in sanbox-ilmentymän roolikeskukseen.
6. Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.
![Sandbox-ympäristön roolikeskuksen ilmoitus](./media/across-sandbox/sandbox-rolecenter-notification.png)  
Sandbox-ympäristöön on luotu täysin uusi vuokraaja. Vuokraajaan on ladattu CRONUS-yrityksen oletusesittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä sandbox-ympäristön luonnin aikana.
7.  Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.
> [!NOTE]  
>  Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.  

8.  Voit siirtyä tuotanto- ja sandbox-ympäristöjen välillä Dynamics 365:n sovellusten käynnistysohjelman avulla.
![Sandbox-ympäristön Dynamics 365 -valikko](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Järjestelmänvalvoja tai toinen käyttäjä voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä. Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksilla, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.

![Sandbox-ympäristön käyttöoikeuksien joukot](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Sandbox-ympäristön lisätoiminnot
### <a name="the-in-client-designer"></a>Asiakasohjelman suunnittelutoiminto
Sandbox-ympäristössä on otettu käyttöön asiakasohjelman suunnittelutoiminto, ja voit aktivoida sen valitsemalla suunnittelukuvakkeen ![Rakennenäkymä](./media/across-sandbox/sandbox-inclient-design-icon.png) -sivulla.

![Asiakasohjelman suunnittelutoiminto](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön
[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisätoiminnot (kaikki toiminnot) voi ottaa käyttöön kokeiltavaksi sandbox-ympäristön vuokraajassa määrittämällä **Kokemus**-kentän **Yrityksen tiedot** -sivulla.

![Sandbox-ympäristön lisäasetukset](./media/across-sandbox/sandbox-advanced.png)

![Sandbox-tuotantoympäristö](./media/across-sandbox/sandbox-production.png)

Kun olet ottanut lisäasetukset käyttöön sandbox-ympäristön vuokraajassa, voit käyttää kaikkia vakioprofiileja ja -roolikeskuksia. Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.

![Sandbox-ympäristön uusi yritys](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

