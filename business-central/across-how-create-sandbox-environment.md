---
title: "Sandbox-ympäristön luominen | Microsoft Docs"
description: "Luo tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten sopiva ympäristö."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 81eb819295a8d2b03f9c53ecd98053d0b1041faa
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Sandbox-ympäristö (esiversio) on [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuotantoympäristöön kuulumaton ilmentymä. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.

## <a name="to-create-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Tarvitse sandbox-ympäristön luontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen. Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.

1. Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sandbox-ympäristö** ja valitse sitten liittyvä linkki.
![Sandbox-ympäristön määrittäminen](./media/across-sandbox/sandbox-environment-setup.png)
3. Valitse **Luo**.  
  Selaimeen avautuu uusi välilehti, jossa voi viimeistellä sandbox-ympäristön määrittämisen.
> [!NOTE]  
>  Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan *.businesscentral.dynamics.com-osoitteen URL-osoitteet.   

4. Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.
![Sandbox-ympäristön ohjattu aloitustoiminto](./media/across-sandbox/sandbox-wizard.png)

5. Valitse **Lisätietoja**, jos haluat lukea skenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse sen sijaan **Sulje**, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in sanbox-ilmentymän roolikeskukseen.
6. Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.
![Sandbox-ympäristön roolikeskuksen ilmoitus](./media/across-sandbox/sandbox-rolecenter-notification.png)  
Sandbox-ympäristöön on luotu täysin uusi vuokraaja. Vuokraajaan on ladattu CRONUS-yrityksen oletusesittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä sandbox-ympäristön luonnin aikana.
7.  Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.
> [!NOTE]  
>  Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.  

8.  Voit siirtyä tuotanto- ja sandbox-ympäristöjen välillä Business Central -sovellusten käynnistysohjelman avulla.
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

