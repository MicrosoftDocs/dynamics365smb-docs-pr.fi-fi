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
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910634"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a>Sandbox-ympäristön luominen [!INCLUDE [prodshort](includes/prodshort.md)]issa

[!INCLUDE [prodshort](includes/prodshort.md)]n avulla voit helposti luoda turvallisen ympäristön, jossa voit testata, kouluttaa tai tehdä vianmäärityksiä häiritsemättä yrityksen työprosesseja tai liiketoimintatietoja. Tällaista ei-tuotantoympäristöä kutsutaan *eristysympäristöksi (sandbox)*. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.  

Järjestelmänvalvoja voi luoda eristysympäristöjä [hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mutta jos haluat testata jotain nopeasti, voit luoda [!INCLUDE [prodshort](includes/prodshort.md)]ssa eristetyn ympäristön.  

> [!NOTE]
> Teknisesti eristysympäristöt ovat hyvin erilaisia tuotantoympäristöihin verrattuna, vaikka järjestelmänvalvoja luo eristysympäristön, joka sisältää tuotantotiedot. Sandbox-ominaisuutta ei voi käyttää vertailuun, eikä esimerkiksi tietokannan vientiä voi pyytää. Jos haluat luoda eristysympäristön vertailuun, järjestelmänvalvoja voi luoda erillisen tuotantoympäristön hallintakeskuksessa. Lisätietoja on kohdassa [Ympäristötyypit](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a>Sandbox-ympäristön luominen [!INCLUDE [prodshort](includes/prodshort.md)]ssa

1. Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.

2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Eristysympäristö** ja valitse sitten liittyvä linkki.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Valitse **Luo**-painike.  

    Näyttöön avautuu toinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.

    > [!NOTE]  
    >  Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan *.businesscentral.dynamics.com-osoitteen URL-osoitteet.

Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Voit valita **Lue lisää** -painikkeen, kun haluat lisätietoja kehittäjäskenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.

Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.<br /><br />
> Voit luoda myös sandbox-ympäristön, joka sisältää tuotantotiedot. Tämä on tehtävä hallintakeskuksen kautta. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments).

Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.

> [!NOTE]  
> Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Järjestelmänvalvoja voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä. Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Sandbox-ympäristön lisätoiminnot

Eristysympäristö ei ole vähiten hyödyllinen, koska se sisältää muutamia käteviä ominaisuuksia.

### <a name="designer"></a>Rakennenäkymä

Sandbox-ympäristössä on **Rakennenäkymä** käytössä. Voit aktivoida Rakennenäkymän valitsemalla Rakennenäkymä-kuvakkeen ![Rakennenäkymä](./media/across-sandbox/sandbox-inclient-design-icon.png) sivulta tai valitsemalla **Rakennenäkymä**-valikkovaihtoehdon ![Asetukset](media/ui-experience/settings_icon_small.png) Asetukset-valikosta.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön
On mahdollista ottaa käyttöön ja kokeilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusversion täyttä toiminnallisuutta Sandbox-vuokraajassa asettamalla **Kokemus**-kenttä **Yrityksen tiedot** -sivulla.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Kun olet ottanut käyttöön *Premium*-käyttökokemuksen, saat käyttöösi kaikki vakioprofiilit (roolit) ja roolikeskukset vakioversiossa. Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden. Vaihtoehtoisesti voit ottaa yhteyttä jälleenmyyntiyhteistyökumppaniin, jotta saat esittelyn ominaisuuksista. Lisätietoja on kohdassa [Miten löydän jälleenmyyjäpartnerin?](across-faq.md#findpartner).  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Katso myös

[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]Kokeilut ja tilaukset](across-preview.md)  
[Ympäristöjen hallinta Business Centralin hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
