---
title: Power Automate -työnkulkujen käyttö Business Centralissa
description: Määritä ja käytä Power Automate -työnkulkuja luodaksesi tai muuttaaksesi Business Centralin tietoja.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 08/31/2023
ms.custom: bap-template
---

<!-- Line 41 says there are three cloud flow types, but the table lists four. Should line 41 change? -->


# <a name="use-power-automate-flows-in-"></a>Power Automate -työnkulkujen käyttäminen [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksissa

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukana olet antanut Microsoft Power Automate -lisenssin. Tämän lisenssin avulla voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja työnkulun osana Microsoft Power Automatessa. Luo työnkulkuja ja yhdistä tiedot sisäisistä ja ulkoisista lähteistä [!INCLUDE [prod_short](includes/prod_short.md)] -yhdistimellä.

Power Automate -työnkulut käynnistyvät tapahtumien avulla, kuten tietueiden luonti, muokkaaminen tai poistaminen. Työnkulut voidaan myös suorittaa käyttäjän määrittämässä aikataulussa tai pyydettäessä.

> [!NOTE]
> Järjestelmänvalvojat voivat rajoittaa Power Automate -käyttöoikeuksia. Jos huomaat, että sinulla ei ole oikeuksia joihinkin tai kaikkiin tässä artikkelissa kuvattuihin ominaisuuksiin, ota yhteyttä järjestelmänvalvojaasi. Lisätietoja siitä, miten voit hallita Power Automaten käyttöä ylläpitäjänä, on kohdassa [Power Automate -integroinnin määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Power Automaten lisäksi voi käyttää hyväksyntätyönkulkumalleja [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu hyväksyntätyönkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Lisätietoja kohdassa [Työnkulut](across-workflow.md).

## <a name="about-power-automate-flows"></a>Tietoja Power Automaten työnkuluista

Power Automateon palvelu, jonka avulla voit luoda automaattisia työnkulkuja (tai työnkulkuja) sovellusten ja palveluiden välillä, kuten [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automaten työnkulut vaativat vain vähän tai ei lainkaan tietoa koodauksesta. Ne voivat liittyä moniin erilaisiin tapahtumiin ja vastauksiin, esimerkiksi:

- Tallenna muutokset
- Ulkoisten tiedostojen päivitykset
- Kirjatut asiakirjat
- Microsoftin ja kolmannen osapuolen palvelut, kuten Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps, jne.

Voit käsitellä kolmea eri pilvityönkulun tyyppiä:

|Työnkulun tyyppi|Kuvaus|
|---------|-----------|
|Automaattinen työnkulku|Tapahtuma käyttää tätä työnkulun tyyppiä automaattisesti. [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa tapahtuma voi olla se, kun tietue tai asiakirja luodaan, sitä muokataan tai se poistetaan. Esimerkiksi uusi myyntilasku voi käynnistää hyväksymispyynnön työnkulun, jolla voi olla erilaisia tapahtumia määritettynä hyväksyjän vastauksen mukaan. Negatiivinen vastaus lähettää ilmoituksen ja sähköpostin hyväksynnän pyytäjälle. Positiivinen vastaus päivittää samanaikaisesti SharePoint-kansiossa sijaitsevan Excel-taulukon ja lähettää päivityksen Teams-keskusteluun. Automaattisia työnkulkuja voi käynnistää sekä sisäisten että ulkoisten tapahtumien avulla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.|
|Hyväksynnän työnkulku|Hyväksynnän työnkulut ovat myös automaattisia työnkulkuja Power Automatessa, mutta ne on suunniteltu erityisesti hyväksynnän pyytämistä varten, kun tietueisiin ja tietoihin tehdään muutoksia. Voit käyttää hyväksynnän työnkulkuja Power Automatessa vaihtoehtona [hyväksynnän työnkulkutoiminnolle](across-use-workflows.md), joka kuuluu kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]. |
|Ajoitettu työnkulku|Tämä työnkulun tyyppi suoritetaan myös automaattisesti, mutta se suoritetaan ajoittain aikataulutetun päivämäärän ja ajan mukaan. |
|Pikatyönkulku|Tämä työnkulun tyyppi suoritetaan pyydettäessä, ja se vaatii käyttäjää suorittamaan sen manuaalisesti toisesta sovelluksesta tai laitteesta, tässä tapauksessa [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmasta. Pikatyönkulut toimivat samalla tavalla kuin eräajot, suorittavat useita pitkiä vaiheita muutamalla näppäimen painalluksella ja ne käynnistetään tietyiltä sivuilta tai taulukoista. Työnkulun avulla voit esimerkiksi lisätä painikkeen toimintovalikkoon **Toimittajat**-sivulla, jos haluat estää toimittajalle suoritettavat maksut ja samaan aikaan lähettää mukautettavia sähköposteja myyjän kontaktille ja yrityksesi ostajille sekä päivittää kontaktin Outlookissa. |

## <a name="power-automate-features"></a>Power Automate -toiminnot

Voit tutustua kaikkiin tällä hetkellä käytettävissä oleviin Power Automate -työnkulkuihin kirjautumalla sisään [Power Automateen](https://powerautomate.com) ja valitsemalla vasemmalla olevasta siirtymispalkista **Omat työnkulut**. Täältä löydät kaikki työnkulut, jotka olet jo luonut itse, ja työnkulut, jotka ylläpitäjä tai työtoverisi on jakanut kanssasi.

- Pikatyönkulkuja voi myös käyttää suoraan useimmista luettelo-, kortti- ja asiakirjasivuista [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisussa. Voit etsiä pikatyönkulkuja sivujen toimintopalkin **Automatisoi**-toimintoryhmästä. Voit suorittaa työnkulun valitsemalla sen ja noudattamalla sinulle esitettyjä ohjeita. Katso lisätietoja seuraavista osioista.

- [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen avulla sinun ei tarvitse tehdä mitään, jos et halua muuttaa niitä tai poistaa niitä käytöstä. Muussa tapauksessa ne vain toimivat käynnistettäessä. 
<!--

## <a name="automated-flows"></a>Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a>Suorita pikatyönkulkuja

Pikatyönkulut avautuvat [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa niin, että ne säilyvät sen liiketoimintaprosessin kontekstissa, jota suoritat. Voit käyttää pikatyönkulkua useimmista luetteloista, korteista tai asiakirjoista.

1. Valitse toimintoriviltä **Automaattinen** ja valitse sitten työnkulku **Power Automate** -toiminnon alla olevasta käytettävissä olevien työnkulkujen luettelosta.

    :::image type="content" source="media/power-automate-instant-menu.svg" alt-text="Näyttää automaattisen toiminnon ja välittömät työnkulun toiminnot.":::

    Joillakin sivuilla **Automaattinen** on **Lisää vaihtoehtoja (...)** -valinnan alla. 
2. Täytä **Suorita työnkulku** -ruudussa kaikki pakolliset kentät ja suorita sitten työnkulku valitsemalla **Jatka**.

> [!NOTE]
> Kun käytät **automaattinen**-nimikettä ensimmäisen kerran, saatat nähdä vain **Power Automaten käytön aloittaminen** -toiminnon. Näet tämän toiminnon, koska et ole hyväksynyt Microsoft Power Automaten tietosuojailmoitusta. Jatka valitsemalla **Power Automaten käytön aloittaminen** ja noudata ohjeita hyväksyäksesi tai hylätäksesi.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Näyttää toimintopalkin Automaattinen-nimikkeen.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a>Luo, muokkaa ja hallitse työnkulkuja

Uusien työnkulkujen luominen tai vanhojen muokkaaminen ja hallinta (esimerkiksi niiden kytkeminen päälle tai pois) voidaan tehdä suoraan Power Automatessa. Voit kuitenkin aloittaa joitakin näistä tehtävistä Automaattinen toiminto -valikosta kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]:

:::image type="content" source="media/power-automate-menu.svg" alt-text="Näyttää toimintopalkissa Automaattinen-toiminnon laajennetut toiminnot.":::

- Luo automaattinen työnkulku luettelosta, kortista tai asiakirjan sivusta valitsemalla **Automaattinen** > **Luo automaattinen työnkulku**.
- Luo hyväksymistyönkulku kortista tai asiakirjan sivusta valitsemalla **Automaattinen** > **Luo hyväksymistyönkulku**.

  > [!TIP]
  > Tämä toiminto on käytettävissä vain kortilla ja asiakirjatyyppien sivuilla, ei luetteloissa.
- Luo pikatyönkulku luettelosta, kortista tai asiakirjan sivusta valitsemalla **Automaattinen** > **Luo työnkulkuun perustuva toiminto**.
- Avaa Power Automate luettelo-, kortti- tai asiakirjasivulta valitsemalla **Automaattinen** > **Hallitse työnkulkuja**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Nämä tehtävät tekee yleensä vain järjestelmänvalvoja tai superkäyttäjä. Tehtävät edellyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman liiketoimintaprosessien laajempaa tuntemusta. Lisätietoja on Business Centralin kehittäjien ja IT-ammattilaisten ohjeen seuraavissa artikkeleissa:

- [Power Automate -integraatio](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview)
- [Luo automaattisia työnkulkuja](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) (tämä kattaa myös hyväksymistyönkulut)
- [Luo pikatyönkulkuja](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)
- [Power Automate -työnkulkujen hallinta](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)
<!-- 

## <a name="add-more-automated-flows-and-instant-flows"></a>Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows"></a>Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  
[Liiketoimintaan valmistautuminen](ui-get-ready-business.md)  
[Työnkulut](across-workflow.md)  
[Liiketoimintatietojen tuominen muista taloushallintojärjestelmistä](across-import-data-configuration-packages.md)  
[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Määritä [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Taloushallinto](finance.md)  
[Power Automate -työnkulkujen hallinta](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Ota pikatyönkulut käyttöön](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
