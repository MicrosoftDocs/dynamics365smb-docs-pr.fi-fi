---
title: Business Centralin kirjanpitäjän käyttökokemukset | Microsoft Docs
description: Lisätietoja Business Central -sovelluksen kirjanpitäjäportaalista ja kirjanpitäjän roolikeskusta, joka tukee asiakasyrityksen omia ja ulkopuolisia kirjanpitäjää.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 06/01/2020
ms.author: edupont
ms.openlocfilehash: 7f78fbcb4c0f37e9c6230004c70cd9d1625b8768
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528108"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]issa
Kaikkien yritysten on pidettävä kirjanpitoa ja hyväksyttävä se. Jotkin yritykset käyttävät ulkoista kirjanpitäjää, ja joillain yrityksillä on oma kirjanpitäjä. Olit kummanlainen kirjanpitäjä tahansa, voit käyttää **kirjanpitäjän** roolikeskusta [!INCLUDE[d365fin](includes/d365fin_md.md)]in kotisivunasi. Siitä saat avattua kaikki sivut, joita tarvitset työssäsi.  

## <a name="accountant-role-center"></a>Kirjanpitäjän roolikeskus
Roolikeskus on koontinäyttö, joka sisältää reaaliaikaisia avainlukuja näyttäviä toimintoruutuja, joista saat nopean pääsyn tietoihin. Sivun yläreunassa on valintanauha, josta pääset käyttämään lisätoimintoja, kuten eniten käytettyjen raporttien ja laskelmien avaaminen Excelissä. Yläosassa olevan siirtymispalkin avulla voit vaihtaa eniten käyttämiesi luetteloiden välillä. Täällä näkyy muita alueita, kuten **Kirjatut asiakirjat** sekä eri tyyppisiä yrityksen kirjaamia asiakirjoja.  

Jos olet uusi [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjä, voit avata opetusvideoiden luettelon suoraan roolikeskuksesta. Voit avata myös **Aloitusoppaan**, joka osoittaa sovelluksen tärkeimmät osat.  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytät ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, järjestelmänvalvojasi voi kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iisi, jolloin he saavat käyttöönsä kirjanpitotietosi. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää kolme lisenssiä, joiden tyyppi on ulkopuolinen kirjanpitäjä. Lisätietoja käyttöoikeuksista on kohdassa [Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://go.microsoft.com/fwlink/?LinkId=871590).

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämille sivuille.  

Ulkopuolisen kirjanpitäjän kutsumista on helpotettu. Avaa vain **Käyttäjät**-sivuta ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  

> [!Note]  
> Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Kirjanpitäjän sähköpostiosoitteen on oltava Azure Active Directoryyn perustuva työsähköpostiosoite. Jos kirjanpitäjä käyttää jotakin muuta sähköpostityyppiä, kutsua ei voi lähettää. 
> 
> Tämä tehtävä edellyttää käyttäjien ja käyttöoikeuksien hallintaa Azure Active Directoryssä, tämän kutsun lähettäneen käyttäjällä on oltava **Yleinen järjestelmänvalvoja** -rooli tai **Käyttäjien järjestelmänvalvoja** -rooli Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Tietoja järjestelmänvalvojarooleista](/microsoft-365/admin/add-users/about-admin-roles) Microsoft 365 -järjestelmänvalvojasisällössä.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Kirjanpitäjän lisääminen Office 365:iin Azure-portaalin kautta

Jos järjestelmänvalvoja tai jälleenmyyntikumppani ei halua käyttää **Ulkoisen kirjanpitäjän kutsuminen** -opasta, hän voi lisätä ulkoisen käyttäjän Azure-portaaliin ja määrittää tälle käyttäjälle ulkoisen kirjanpitäjän käyttöoikeuden. Lisätietoja on kohdassa [Nopeasti alkuun: Lisää vieraskäyttäjiä hakemistoon Azure-portaalissa](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Kirjanpitäjän lisääminen vieraskäyttäjäksi

1. Avaa [Azure -portaali](https://portal.azure.com/).
2. Valitse **Azure Active Directory** vasemmanpuoleisessa ruudussa.
3. Valitse **Hallitse**-kohdassa **Käyttäjät**.
4. Valitse **Uusi vieraskäyttäjä**.
5. Valitse **Uusi käyttäjä** -sivulla **Kutsu käyttäjä**, ja lisää sitten tietoja ulkoisesta kirjanpitäjästäsi.  

   Voit halutessasi lisätä kirjanpitäjälle henkilökohtaisen tervetuloviestin, jotta he tietävät, että lisäät heidät kohteeseen [!INCLUDE[prodshort](includes/prodshort.md)].

6. Valitse **Kutsu** lähettääksesi automaattisen kutsun. Ilmoitus tulee näkyviin oikeaan yläkulmaan viestinä **Käyttäjän kutsuminen onnistui**. 
7. Kun olet lähettänyt kutsun, käyttäjätili lisätään automaattisesti hakemistoon vieraana.

Seuraavaksi sinun on määritettävä uudelle vieraskäyttäjälle käyttöoikeus [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Voit antaa kirjanpitäjälle pääsyn kohteeseen [!INCLUDE[prodshort](includes/prodshort.md)]

1. Valitse Azure-portaalissa juuri lisätyn käyttäjän **Profiili** ja valitse sitten **Muokkaa**
2. Päivitä **Käyttösijainti** -kenttä asianomaisen maan kohdalle ja valitse sitten **Tallenna**.
3. Valitse **Käyttöoikeudet** ja avaa sitten **Varaukset**.
4. Valitse **Dynamics 365 Business Central Ulkoinen kirjanpitäjä** -käyttöoikeus.  

    Jos tämä käyttöoikeus ei ole käytettävissä, sinun on käytettävä käytettävissä olevaa **Dynamics 365 Business Central IWS** -käyttöoikeutta.
5. Tallenna tehtävä.

Jos tämä onnistuu, käyttöoikeus määritetään vieraskäyttäjälle ja vierastili luodaan.

### <a name="importing-the-new-user-into-prodshort"></a>Uuden käyttäjän tuominen kohteeseen [!INCLUDE[prodshort](includes/prodshort.md)]

Kirjanpitäjä saa sähköpostiviestin, joka ilmoittaa hänelle, että hänelle on annettu pääsy Active Directoryyn. Seuraavaksi sinun on annettava heille oikeus käyttää oikeaa yritystä kohteessa [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Kirjanpitäjän lisääminen oikeaan yritykseen

1. Avaa [!INCLUDE[prodshort](includes/prodshort.md)]-yritys, johon haluat antaa kirjanpitäjälle käyttöoikeuden, kohteessa [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.  
3. Valitse **Hae uudet käyttäjät Office 365:stä** -toiminto.

Tämä tuo käyttäjätilin, jonka loit Azure-portaalissa yritykselle. Lisätietoja on kohdassa [Käyttäjän lisääminen Business Centralissa](ui-how-users-permissions.md#adduser).  

Jos haluat antaa käyttöoikeudet useille yrityksille, sinun on kirjauduttava jokaiseen yritykseen ja toistettava tämä prosessi. Vaihtoehtoisesti voit päivittää kirjanpitäjän käyttäjäprofiilin käyttöoikeusryhmät kohteessa [!INCLUDE[prodshort](includes/prodshort.md)], esimerkiksi määrittämällä heille *D365 Bus Premium* -käyttäjäryhmän. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

<!--## Accountant Hub

If you are an accountant with several clients, you can use [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] for a better overview of your clients. From there, you can access each client's tenant in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the Accountant Role Center as described above. For more information see [Welcome to [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE[d365acc_long_md](includes/d365acc_long_md.md)] is currently in public preview in a limited number of markets.-->

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Rahoituslaskelmien analysointi Excelissä](finance-analyze-excel.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md)  
