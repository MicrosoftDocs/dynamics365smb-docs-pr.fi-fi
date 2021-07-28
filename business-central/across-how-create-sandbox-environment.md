---
title: Eristysympäristön (sandbox) luominen
description: Luo Business Centralissa sandbox-ympäristö (testiympäristö) turvallista tutustumista, oppimista, esittelyä, kehittämistä, vianmääritystä ja testausta varten.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437675"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Sandbox-ympäristön luominen [!INCLUDE[prod_short](includes/prod_short.md)]issa

[!INCLUDE[prod_short](includes/prod_short.md)]n avulla voit helposti luoda turvallisen ympäristön, jossa voit testata, kouluttaa tai tehdä vianmäärityksiä häiritsemättä yrityksen työprosesseja tai liiketoimintatietoja. Tällaista ei-tuotantoympäristöä kutsutaan *eristysympäristöksi (sandbox)*. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.  

Järjestelmänvalvoja hallinnoi eristysympäristöjä [hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mutta jos haluat testata jotain nopeasti, voit luoda [!INCLUDE[prod_short](includes/prod_short.md)]ssa eristetyn ympäristön. Kun olet valmis, voit poistaa eristysympäristön hallintakeskuksen avulla.  

> [!NOTE]
> Teknisesti eristysympäristöt ovat hyvin erilaisia tuotantoympäristöihin verrattuna, vaikka järjestelmänvalvoja luo eristysympäristön, joka sisältää tuotantotiedot. Sandbox-ominaisuutta ei voi käyttää vertailuun, eikä esimerkiksi tietokannan vientiä voi pyytää. Jos haluat luoda eristysympäristön vertailua varten, järjestelmänvalvoja voi luoda erillisen ympäristön hallintakeskuksessa. Lisätietoja on kohdassa [Tuotanto- ja eristysympäristöt](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Sandbox-ympäristön luominen [!INCLUDE[prod_short](includes/prod_short.md)]ssa

1. Kirjaudu [!INCLUDE[prod_short](includes/prod_short.md)]-palvelun tuotantoilmentymään.

2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sandbox-ympäristö** ja valitse sitten vastaava linkki.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Valitse **Luo**-painike.  

    Näyttöön avautuu toinen [!INCLUDE[prod_short](includes/prod_short.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.

    > [!NOTE]  
    >  Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan *.businesscentral.dynamics.com-osoitteen URL-osoitteet.

Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

Voit valita **Lue lisää** -painikkeen, kun haluat lisätietoja kehittäjäskenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.

Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.
>
> Vaihtoehtoisesti voit luoda tuotantotietoihin perustuvan eristysympäristön. Tämä on tehtävä hallintakeskuksen kautta. Lisätietoja on kehittäjä- ja hallintasisällön kohdassa [Ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments).  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Järjestelmänvalvoja voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä. Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Sandbox-ympäristön lisätoiminnot

Eristysympäristö on hyödyllinen muun muassa seuraavien kätevien ominaisuuksien ansiosta:

* [Käyttäjäkokemuksen parannus](#advanced-user-experience)  
* [Täydelliset esimerkkitiedot](#complete-sample-data)  
* [Suunnitteluohjelma](#designer)  

### <a name="advanced-user-experience"></a>Käyttäjäkokemuksen parannus

[!INCLUDE[prod_short](includes/prod_short.md)]in perusversion voi ottaa käyttöön ja sen kaikkia toimintoja voi käyttää eristysvuokraajassa määrittämällä **Kokemus**-kentän asetukseksi *Premium* **Yrityksen tiedot** -sivulla. Etsi **Yrityksen tiedot** -sivu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Asetukset-kuvake."::: -valikosta.  

Kun olet ottanut käyttöön *Premium*-käyttökokemuksen, saat käyttöösi kaikki vakioprofiilit (roolit) ja roolikeskukset vakioversiossa. Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden. Vaihtoehtoisesti voit ottaa yhteyttä jälleenmyyntiyhteistyökumppaniin, jotta saat esittelyn ominaisuuksista. Lisätietoja on kohdassa [Miten löydän jälleenmyyjäkumppanin?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Täydelliset esimerkkitiedot

Jos tarvitset lisää esimerkkitietoja, käänny jälleenmyyjäkumppanin puoleen.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Täydelliset näytetiedot sisältävän yrityksen luonti eristysympäristössä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yritykset** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Uusi**-toiminto ja valitse sitten **Luo uusi yritys**.  
3. Valitse **Yrityksen luontiasetusten ohjattu määritys** -sivulla **Seuraava**.  
4. Määritä uuden yrityksen nimi ja valitse sitten **Aloita valitsemalla tiedot ja asetukset** -kentässä **Laajennettu arviointi - Kaikki mallitiedot**.  
5. Suorita asetusten ohjatun määritysoppaan loput vaiheet.  

Kun asetuksen ohjattu määritysopas on suoritettu, voi aloittaa uuteen yritykseen tutustumisen täydellisten mallitietojen avulla. Lisätietoa on kohdassa [Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](about-new-company.md).  

### <a name="designer"></a>Rakennenäkymä

Sandbox-ympäristössä on **Rakennenäkymä** käytössä. Voit aktivoida Suunnitteluohjelman valitsemalla suunnittelukuvakkeen ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) sivulla tai valitsemalla **Rakenne**-valikkokohteen ![Asetukset](media/ui-experience/settings_icon_small.png) Asetukset-valikossa.  

Lisätietoja on kehittäjä- ja järjestelmänvalvojasisällön kohdassa [Suunnitteluohjelman käyttäminen ](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) (vain englanniksi).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]Kokeilut ja tilaukset](across-preview.md)  
[Ympäristöjen hallinta Business Centralin hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
