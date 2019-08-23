---
title: Sandbox-ympäristön luominen | Microsoft Docs
description: Luo tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten sopiva ympäristö.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 10ccbc7546aa5d03c3837997a721c63c3ce465da
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796663"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Sandbox-ympäristö (esiversio) on [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuotantoympäristöön kuulumaton ilmentymä. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.

## <a name="to-create-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Tarvitse sandbox-ympäristön luontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen. Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.

1. Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.

2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sandbox-ympäristö** ja valitse sitten liittyvä linkki.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Valitse **Luo**-painike.  

    Näyttöön avautuu toinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.

    > [!NOTE]  
    >  Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan *.businesscentral.dynamics.com-osoitteen URL-osoitteet.

4. Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Valitse **Lue lisää** -painike, kun haluat lisätietoja skenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.

    Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.<br /><br />
    > Voit luoda myös sandbox-ympäristön, joka sisältää tuotantotiedot. Tämä on tehtävä hallintakeskuksen kautta. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Ympäristöjen hallinta](/business-central/dev-itpro/administration/tenant-admin-center-environments).

6. Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.
    > [!NOTE]  
    >  Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.  

7. Voit siirtyä tuotanto- ja sandbox-ympäristöjen välillä Business Central -sovellusten käynnistysohjelman avulla.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. Järjestelmänvalvoja tai toinen käyttäjä voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä. Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Sandbox-ympäristön lisätoiminnot
### <a name="designer"></a>Rakennenäkymä
Sandbox-ympäristössä on otettu käyttöön **suunnittelutoiminto**, ja voit aktivoida sen valitsemalla sivulla suunnittelukuvakkeen ![Suunnitteluohjelma](./media/across-sandbox/sandbox-inclient-design-icon.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön
[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisätoiminnot (kaikki toiminnot) voi ottaa käyttöön kokeiltavaksi sandbox-ympäristön vuokraajassa määrittämällä **Kokemus**-kentän **Yrityksen tiedot** -sivulla.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Kun olet ottanut lisäasetukset käyttöön sandbox-ympäristön vuokraajassa, voit käyttää kaikkia vakioprofiileja (rooleja) ja roolikeskuksia. Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
