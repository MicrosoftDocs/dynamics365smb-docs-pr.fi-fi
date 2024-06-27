---
title: Kirjanpitäjän käyttökokemukset Business Centralissa
description: 'Lisätietoja kirjanpitäjän roolikeskuksesta ja yritystoiminnosta, jotka tukevat asiakasyrityksen omia ja ulkopuolisia kirjanpitäjiä.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 06/12/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="accountant-experiences-in-"></a>Kirjanpitäjän kokemukset [!INCLUDE[prod_long](includes/prod_long.md)] -ohjelmassa

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Kaikkien yritysten on pidettävä kirjanpitoa ja hyväksyttävä se. Jotkin yritykset käyttävät ulkoista kirjanpitäjää, ja joillain yrityksillä on oma kirjanpitäjä. Olit millainen kirjanpitäjä tahansa, voit käyttää **kirjanpitäjän** roolikeskusta [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman kotisivunasi. Siitä saat avattua kaikki sivut, joita tarvitset työssäsi.  

## <a name="accountant-role-center"></a>Kirjanpitäjän roolikeskus

Roolikeskus on koontinäyttö, joka sisältää reaaliaikaisia avainlukuja näyttäviä toimintoruutuja, joista saat nopean pääsyn tietoihin. Sivun yläosan valintanauhasta voit valita lisää toimintoja. Voit esimerkiksi avata talousraportit ja -laskelmat Excelissä. Yläosassa olevan siirtymispalkin avulla voit vaihtaa eniten käyttämiesi luetteloiden välillä. Täällä näkyy muita alueita, kuten **Kirjatut asiakirjat** sekä eri tyyppisiä yrityksen kirjaamia asiakirjoja.  

Jos olet uusi [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjä, voit avata opetusvideoiden luettelon suoraan roolikeskuksesta. Voit avata myös **Aloitusoppaan**, joka osoittaa sovelluksen tärkeimmät osat.  

## <a name="company-hub"></a>Yritystoiminto

Jos työskentelet useissa [!INCLUDE [prod_short](includes/prod_short.md)] -yrityksissä, kannattaa ehkä käyttää **Yritystoiminto**-sivua työn seuraamiseen. Katso lisätietoja kohdasta [Työnhallinta useiden yritysten välillä yritystoiminnossa](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[prod_short](includes/prod_short.md)]iin

Jos käytät ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, järjestelmänvalvojasi voi kutsua kirjanpitäjän [!INCLUDE[prod_short](includes/prod_short.md)]iisi, jolloin he saavat käyttöönsä kirjanpitotietosi. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää kolme lisenssiä, joiden tyyppi on ulkopuolinen kirjanpitäjä. Saat lisätietoja käyttöoikeuksista lataamalla [Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaan](https://go.microsoft.com/fwlink/?LinkId=866544).

Kun kirjanpitäjällä on [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi eniten käyttämille sivuille. He voivat myös käyttää yritystoimintoa työnsä hallitsemiseen omassa [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassaan. Katso lisätietoja kohdasta [Työnhallinta useiden yritysten välillä yritystoiminnossa](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Ulkoisen kirjanpitäjän kutsuminen on helppoa. Avaa **Käyttäjät**-sivuta ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  

> [!Note]  
> Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Kirjanpitäjän sähköpostiosoitteen on oltava Microsoft Entra ID:hen perustuva työsähköpostiosoite. Jos kirjanpitäjä käyttää jotakin muuta sähköpostityyppiä, kutsua ei voi lähettää.
>
> Tämä tehtävä edellyttää pääsyä käyttäjien ja käyttöoikeuksien hallintaan Microsoft Entra ID:ssä. Tämän kutsun lähettäneen käyttäjän on määritettävä **Yleinen järjestelmänvalvoja** -rooli tai **Käyttäjän järjestelmänvalvoja** -rooli Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Tietoja järjestelmänvalvojarooleista](/microsoft-365/admin/add-users/about-admin-roles)(Microsoft 365:n järjestelmänvalvojasisältö).  

### <a name="add-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Kirjanpitäjän lisääminen Microsoft 365:iin Azure-portaalissa

Jos järjestelmänvalvoja tai jälleenmyyntikumppani ei halua käyttää **Ulkoisen kirjanpitäjän kutsuminen** -opasta, hän voi lisätä ulkoisen käyttäjän Azure-portaaliin ja määrittää tälle käyttäjälle *ulkoisen kirjanpitäjän* käyttöoikeuden. Lisätietoja on kohdassa [Nopeasti alkuun: Lisää vieraskäyttäjiä hakemistoon Azure-portaalissa](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Kirjanpitäjän lisääminen vieraskäyttäjäksi

1. Avaa [Azure -portaali](https://portal.azure.com/).
2. Valitse vasemmanpuoleisessa ruudussa **Microsoft Entra ID**.
3. Valitse **Hallitse**-kohdassa **Käyttäjät**.
4. Valitse **Uusi vieraskäyttäjä**.
5. Valitse **Uusi käyttäjä** -sivulla **Kutsu käyttäjä**, ja lisää sitten tietoja ulkoisesta kirjanpitäjästäsi.  

   Voit halutessasi lisätä kirjanpitäjälle henkilökohtaisen tervetuloviestin, jotta he tietävät, että lisäät heidät kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)].

6. Valitse **Kutsu** lähettääksesi automaattisen kutsun. Ilmoitus tulee näkyviin oikeaan yläkulmaan viestinä **Käyttäjän kutsuminen onnistui**. 
7. Kun olet lähettänyt kutsun, käyttäjätili lisätään automaattisesti hakemistoon vieraana.

Seuraavaksi sinun on määritettävä uudelle vieraskäyttäjälle käyttöoikeus [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-"></a>Voit antaa kirjanpitäjälle pääsyn kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

1. Valitse Azure-portaalissa juuri lisätyn käyttäjän **Profiili** ja valitse sitten **Muokkaa**
2. Päivitä **Käyttösijainti**-kenttään asianomainen maa tai alue ja valitse sitten **Tallenna**.
3. Valitse **Käyttöoikeudet** ja avaa sitten **Varaukset**.
4. Valitse **Dynamics 365 Business Central Ulkoinen kirjanpitäjä** -käyttöoikeus.  
    
    Jos tämä käyttöoikeus ei ole saatavilla, ota yhteyttä jälleenmyyjäkumppaniisi ja lisää käyttöoikeus tilaukseesi.

    Erityisesti arviointia varten kokeiluvuokraajassa voit käyttää saatavilla olevaa **Dynamics 365 Business Central for IWs** -lisenssiä sen sijaan. Et kuitenkaan voi käyttää tämäntyyppistä lisenssiä, jos olet jo ostanut [!INCLUDE[prod_short](includes/prod_short.md)]in. 
5. Tallenna tehtävä.

Jos tämä onnistuu, käyttöoikeus määritetään vieraskäyttäjälle ja vierastili luodaan.

### <a name="import-the-new-user-into-"></a>Uuden käyttäjän tuominen kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

Kirjanpitäjä saa sähköpostiviestin, joka ilmoittaa hänelle, että hänelle on annettu pääsy Microsoft Entra ID:hen. Seuraavaksi sinun on annettava heille oikeus käyttää oikeaa yritystä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Kirjanpitäjän lisääminen oikeaan yritykseen

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]-yritys, johon haluat antaa kirjanpitäjälle käyttöoikeuden, kohteessa [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.  
3. Valitse **Hae uudet käyttäjät Microsoft 365:stä** -toiminto.

Tämä toiminto tuo käyttäjätilin, jonka loit Azure-portaalissa yritykselle. Lisätietoja on kohdassa [Käyttäjän lisääminen Business Centralissa](ui-how-users-permissions.md#adduser).  

Jos haluat antaa käyttöoikeudet useille yrityksille, sinun on kirjauduttava jokaiseen yritykseen ja toistettava tämä prosessi. Vaihtoehtoisesti voit päivittää kirjanpitäjän käyttäjäprofiilin käyttöoikeusryhmät kohteessa [!INCLUDE[prod_short](includes/prod_short.md)], esimerkiksi määrittämällä heille *D365 Bus Premium* -käyttäjäryhmän. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Katso myös

[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Rahoituslaskelmien analysointi Excelissä](finance-analyze-excel.md)  
[Työnhallinta useiden yritysten välillä yrityksen keskittimessä](company-hub.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
