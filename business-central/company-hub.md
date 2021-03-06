---
title: Työnhallinta useiden yritysten välillä yritystoiminnossa
description: Tutustu yritystoimintoon Dynamics 365 Business Centralissa, jossa työskentelet useiden yritysten kesken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: acc1bf44ddf3886d57729fb28ba81c6e7580ce40
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775177"
---
# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Työnhallinta useiden yritysten välillä yritystoiminnossa

Osa ihmisistä työskentelee useissa yrityksissä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, ja osa toimii myös useammassa kuin yhdessä organisaatiossa, kuten ulkoiset kirjanpitäjät tai sellaisten yritysten työntekijät ja johtajat, joilla on useita tytäryhtiöitä. Näille käyttäjille ja monille muille yrityksen toiminto toimii aloitussivuna, jossa työnhallinta toimii eri ympäristöissä, joissa työskentelet, yrityksissä, ympäristöissä ja alueilla.  

Voit käyttää yrityskeskitintä siirtymällä **Yritystoiminto**-rooliin Omat asetukset -kohdassa tai avaamalla **Yritystoiminto**-sivun suoraan. Voit tehdä saman työn kummassakin paikassa, mutta valikoissa on hieman erilaisia toimintoja.  

> [!NOTE]
> Voit yhdistää yrityskeskuksen niin moneen yritykseen kuin tarvitset. Yrityskeskuksen voi kuitenkin liittää vain yrityksiin, joita isännöidään [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa.

## <a name="company-hub-home-page"></a>Yritystoiminnon kotisivu

Jos käytät **Yritystoiminto**-roolia, kotisivusi näyttää luettelon yrityksistä, joihin sinulla on käyttöoikeus, sekä tietoja keskeisten kiinnostavuuspisteiden (KPI) tiedoista sekä linkkejä kunkin yrityksen avaamiseen. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Valitse **Yritystoiminto**-toiminto, kun haluat avata yritystoiminnon, jossa voit työskennellä tiiviimmin kunkin yrityksen kanssa.  

> [!TIP]
> Jos haluat käyttää tiettyä yritystä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman yrityksessä, valitse yrityksen nimi tai valitse **Siirry yritykseen** -valikkovaihtoehto. Olet kirjautunut sisään automaattisesti uudessa selainvälilehdessä.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Yritystoiminnon luettelossa olevan yrityksen toiminnot":::

Voit lisätä uusia yrityksiä, esimerkiksi silloin, kun saat uuden asiakkaan, tai kun yritys lisää uuden tytäryrityksen. Lisätietoja on kohdassa [Yritysten lisääminen yritystoimintoon](company-hub-add-company.md).  

> [!TIP]
> Jotta voisit päivittää yritystoiminnon tiedot, sinun on voitava käyttää niiden yritysten tietoja, joista tiedot ovat peräisin.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Määritetyt tehtävät

Voit määrittää tehtäviä [!INCLUDE [prod_short](includes/prod_short.md)]:ssä itselle ja muille; lisäksi muut voivat määrittää tehtäviä sinulle. Yritystoiminto antaa yleiskuvan kullekin yritykselle määritetyistä tehtävistä. Saat käyttöösi myös luettelon kaikista määritetyistä tehtävistä valitsemalla **Aloitus**-sivulla **Omat käyttäjätehtävät**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Omat käyttäjätehtävät

**Omat käyttäjätehtävät** -luettelo auttaa päivän tehtävien priorisoinnissa, sillä siinä on lisätietoja kaikista yritysten sinulle määrittämistä tehtävistä.  

Voit tehdä lajittelun esimerkiksi määräpäivän mukaan tai minkä tahansa sellaisen tietotyypin mukaan, joka auttaa päivän priorisoinnissa. Luettelossa näkyy oletusarvoisesti kaikki sinulle määritetyt tehtävät, mutta määrittää suodattimet näyttämään esimerkiksi vain korkean prioriteetin tehtävät.  

Voit poimia tehtävän yksinkertaisesti valitsemalla sen odottavien käyttäjätehtävien luettelosta. Valintanauhan **Siirry tehtäväkohteeseen** -linkki avaa sivun, jossa voit suorittaa työn.  

Kun tehtävä on suoritetty, voit merkitä sen valmiiksi.  

Lisätietoja yrityksistä ja ympäristöistä on kohdassa [Ympäristölinkit](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Yritystoiminnon käyttö

Jotta voisit käyttää yritystoimintoa, sinulla on oltava käyttöoikeus joko *D365 Yritystoiminto*-käyttäjäryhmään tai *D365 Yritystoiminto*-käyttöoikeus joukkoon. Sinun täytyy myös pystyä käyttämään yrityksiä, jotka on luetteloitu yritystoiminnossasi, mikä tarkoittaa sitä, että sinun täytyy olla käyttäjä näissä yrityksissä. Katso lisätietoja kohdasta [Luo käyttäjiä lisenssien mukaan](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Yritystoiminto on yrityksenlaajuinen luettelo, joten kuka tahansa yritystoiminnon käyttöoikeuden myöntänyt käyttäjä voi nähdä kaikki oman [!INCLUDE [prod_short](includes/prod_short.md)] -vuokralaisyrityksensä yritykset ja kaikki niiden yritysten KPI:t, joihin hänellä on käyttöoikeus.

Jos et löydä yritystoimintoa ja tiedät, että sinulla on siihen käyttöoikeus, tarkista asia järjestelmänvalvojalta, jos yritystoiminto on luetteloitu **Laajennusten hallinta** -sivulla. Lisätietoja on kohdassa [Business Centralin mukauttaminen laajennusten avulla](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Määritä yritystoiminto

Jotta voisit aloittaa yritystoiminnon käyttämisen, sinun on lisättävä vähintään yksi yritys koontinäyttöön. Lisätietoja on kohdassa [Yritysten lisääminen yritystoimintoon](company-hub-add-company.md).  

Yrityksen lisääminen edellyttää kuitenkin, että sinulla on käyttöoikeus yhteen tai useampaan [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman esiintymään sen yrityksen lisäksi, jota yritystoiminnossa käytät.  

Esimerkiksi, jos olet kirjanpitäjä, asiakkaasi voivat kutsua sinut heidän [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaansa. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant).  

Järjestelmänvalvojat voivat käyttää samaa avustettua Ohjatun määrityksen opasta käyttäjien lisäämiseen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, tai he voivat lisätä sinut asianmukaiseen Azure AD -tiliin Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Käyttäjien ja ryhmien hallinta](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Katso myös

[Yritysten lisääminen yrityksen keskittimeen](company-hub-add-company.md)  
[Kirjanpitäjän käyttökokemukset Business Centralissa](finance-accounting.md)  
[Business Central -laajennuksen yritystoiminto](ui-extensions-company-hub.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]