---
title: "Lisävaluuttojen määrittäminen| Microsoft Docs"
description: "Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA) ja toinen valuutta määritetään lisävaluutaksi, jolle määritetään ajantasainen vaihtokurssi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/07/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a98027c3ef3171491f84197897f93cbed4e288c2
ms.openlocfilehash: 294ed8019b12287e4b4ad59d46e842e4022a637f
ms.contentlocale: fi-fi
ms.lasthandoff: 01/07/2019

---
# <a name="set-up-an-additional-reporting-currency"></a>Lisäraportointivaluutan määrittäminen
Yritysten toimiessa yhä useammassa maassa tai alueella niiden on entistä tärkeämpää pystyä tarkistamaan ja raportoimaan taloustiedot useana valuuttana.

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin.

> [!Warning]
> Lisäraportointivaluutta-toimintoa ei saa käyttää rahoituslaskelmien käännösten perustana. Tällä työkalulla ei pysty kääntämään ulkomaisten tytäryritysten tilinpäätöksiä osana yrityksen konsolidointia. Lisäraportointivaluuttaa voidaan käyttää vain toista valuttaa käyttävien raporttien valmisteluun siten, että kyseinen valuutta on kuin yrityksen paikallinen valuutta.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Raporttien ja summien näyttäminen lisäraportointivaluuttana
Lisäraportointivaluutan käyttäminen voi helpottaa yrityksen raportointiprosessia seuraavissa tapauksissa:

- Yritys toimii EU:n ulkopuolella ja suuri osa sen liiketoimista tapahtuu EU:ssa toimivien yritysten kanssa. Tässä tapauksessa EU:n ulkopuolisen yrityksen kannattaa ehkä raportoida euroina, jotta sen finanssiraportit olisivat helpommin EU-liikekumppanien käytettävissä.
- Yritys haluaa esittää raporttinsa oman paikallisen valuuttansa lisäksi myös laajemmin kansainvälisesti käytetyssä valuutassa.

Useat talousraportit perustuvat kirjanpitotapahtumiin. Voit näyttää raportin tiedot lisäraportointivaluuttana yksinkertaisesti lisäämällä valintamerkin kyseisen KP-raportin **Vaihtoehdot**-pikavälilehden **Näytä summat lisäraportointivaluuttana** -kenttään.

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen
Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä ohjelmaan, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty. **Muuta vaihtokursseja** -eräajon avulla voi muuttaa kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia. Lisätietoja on kohdassa [Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Lisäraportointivaluutan määrittäminen
Määritä lisäraportointivaluutta seuraavien ohjeiden mukaisesti:

-   Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  
-   Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  
-   Määritä vaihtokurssien muutosmenetelmän ALV-tapahtumille  
-   Lisäraportointivaluutan aktivoiminen  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten liittyvä linkki.  
2. Täytä **Valuutat**-sivulla seuraavat kentät lisäraportointivaluuttaa varten.  

|Kenttä|Description|  
|---------------------------------|---------------------------------------|  
|**Realisoitun. KP-voittojen tili**|KP-tili, jolle ohjelma kirjaa PVA:n ja lisäraportointivaluutan välisten valuuttamuutosten vaihtokurssivoitot|  
|**Realisoitun. KP-tapp. tili**|KP-tili, jolle ohjelma kirjaa PVA:n ja lisäraportointivaluutan välisten valuuttamuutosten kurssitappiot|  
|**Jäännösvoittojen tili**|KP-tili, jolle ohjelma kirjaa jäännössummat, jotka ovat voittoja, silloin kun tapahtumat kirjataan pääkirjanpidon sovellusalueelle sekä PVA:na että lisäraportointivaluuttana|  
|**Jäännöstappioiden tili**|KP-tili, jolle ohjelma kirjaa jäännössummat, jotka ovat tappioita, silloin kun tapahtumat kirjataan pääkirjanpidon sovellusalueelle sekä PVA:na että lisäraportointivaluuttana|

> [!NOTE]  
>  Jäännössummia voi syntyä [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman pyöristäessä PVA:sta lisäraportointivaluutaksi muunnettuja debet- ja kreditsummia.  

Kutakin KP-tiliä varten on määritettävä, kuinka tilin KP-summat muutetaan PVA:n ja lisäraportointivaluutan välisen vaihtokurssin muuttuessa.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Valitse ensin **Tilikartta**-sivulla sopiva tili ja sitten **Muokkaa**-toiminto.  
3. Valitse **KP-tilin kortti** -sivun **Vaihtokurssin muutos** -kentässä sopiva menetelmä.  

    Jos tapahtumat kirjataan lisäraportointivaluuttana, **Vaihtokurssin muutos** -kentässä määritetään, kuinka tätä KP-tiliä muutetaan PVA:n ja lisäraportointivaluutan välisen vaihtokurssin muuttuessa. Seuraavassa taulukossa näytetään valittavat asetukset.  

    |Kenttä|Kuvaus|  
    |----------------------------------|---------------------------------------|  
    |**Ei muutosta**|KP-tilille ei tehdä vaihtokurssin muutosta. Tämä on oletusarvo.<br /><br /> **HUOMAUTUS:** Ei muutosta -vaihtoehto tulisi valita, jos PVA:n ja lisäraportointivaluutan vaihtokurssi on aina kiinteä.|  
    |**Muuta summaa**|PVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  
    |**Muuta lisävaluuttasummaa**|Lisäraportointivaluutta muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  

    Vaihtokurssivoitot ja -tappiot kirjataan **Muuta vaihtokursseja** -eräajon suorituksen yhteydessä. Kyseisessä eräajossa ohjelma etsii muuttuneen vaihtokurssin **Valuutan vaihtokurssit** -sivulta ja selvittää sitten, onko kyseessä vaihtokurssivoitto vai -tappio, vertaamalla KP-tapahtuman **Summa**- ja **Lisävaluutan summa** -kenttien summia. Eräajo määrittää **Vaihtokurssin muutos** -kentässä valitun vaihtoehdon perusteella, Miten KP-tilien vaihtokurssivoitot tai -tappiot lasketaan ja kirjataan.  

4.  Sulje **KP-tilin kortti** -sivu.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Vaihtokurssien muutosmenetelmän määrittäminen ALV-tapahtumille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Pääkirjanpidon asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Pääkirjanpidon asetukset** -sivun **ALV:n vaihtokurssin muutos** -kentässä sopiva menetelmä.  
3. Jos tapahtumat kirjataan lisäraportointivaluuttana, **ALV:n vaihtokurssin muutos** -kentässä voi määrittää, kuinka **ALV-kirjausten asetukset** -sivulla ALV-kirjauksille määritettyjä tilejä muutetaan PVA:n ja lisäraportointivaluutan välisen vaihtokurssin muuttuessa.  

    **Muuta vaihtokursseja** -eräajon suorittamisen yhteydessä muuttunut vaihtokurssi määritetään **Valuutan vaihtokurssi** -sivulla ja selvitetään sitten, onko kyseessä vaihtokurssivoitto vai -tappio, vertaamalla ALV-tapahtuman **Summa**- ja **Lisävaluutan summa** -kenttiä. Eräajo määrittää tässä kentässä valitun vaihtoehdon perusteella, kuinka ALV-tilien vaihtokurssivoitot tai -tappiot kirjataan.  

    Valittavana on samat kolme vaihtoehtoa kuin KP-tapahtumissa, mutta tässä tapauksessa muutettavat tapahtumat ovat ALV-tapahtumia: Seuraavassa taulukossa näytetään valittavat asetukset.

    |Kenttä|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ei muutosta**|KP-tilille ei tehdä vaihtokurssin muutosta. Tämä on oletusarvo.|  
    |**Muuta summaa**|PVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  
    |**Muuta lisävaluuttasummaa**|Lisäraportointivaluutta muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Lisäraportointivaluutan aktivoiminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Pääkirjanpidon asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Pääkirjanpidon asetukset** -sivulla **Lisäraportointivaluutta**-kenttä ja valitse haluamasi raportoinnin lisävaluutta.  
3. Kun poistut kentästä, [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää vahvistussanoman, jossa kuvataan lisäraportointivaluutan valitsemisen (ja aktivoinnin) vaikutus.  
4. Vahvista valuutan aktivointi valitsemalla **Kyllä**.  
5. **Muuta/Lisää. Raportointivaluutta** -eräajo avautuu.

    Tämä eräajo muuttaa olemassa olevien tapahtumien PVA-summat lisäraportointivaluutaksi. Eräajo käyttää oletusvaihtokurssina työpäivänä voimassa olevaa **Valuutan vaihtokurssit** -sivulta kopioitua vaihtokurssia. Jäännössummat, jotka syntyvät, kun PVA muunnetaan lisäraportointivaluutaksi, kirjataan **Valuutat**-sivulla määritetyille jäännösvoittojen ja -tappioiden tileille. Näiden tapahtumien kirjauspäivämäärä ja asiakirjanumero ovat samat kuin alkuperäisessä KP-tapahtumassa. Kun kaikki nämä jäännöstapahtumat on kirjattu, eräajo kirjaa jakamattoman voiton tilille pyöristystapahtuman kunkin suljetun tilikauden sulkemispäivänä. Näin varmistetaan, että kunkin suljetun vuoden tuloslaskelmatilin loppusaldo on 0 sekä PVA:na että lisäraportointivaluuttana.
6. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Suorita eräajo valisemalla **OK**.  

Tämän eräajon suorittamisen jälkeen seuraavien aiemmin luotujen tapahtumien summat ovat sekä PVA:na että lisäraportointivaluuttana.  

- Pääkirjanpidon tapahtumat  
- Nimikkeen kohdistustapahtumat  
- ALV-tapahtumat  
- Projektitapahtumat  
- Arvotapahtumat  
- tuotantotilausrivit  
- tuotantotilaustapahtumat.  

Lisäksi kaikissa samantyyppisissä tulevissa tapahtumissa summat kirjataan sekä PVA:na että lisäraportointivaluuttana.  

> [!NOTE]  
>  **Lisäraportointivaluutta**-kenttä aktivoituu vasta, kun olet napsauttanut **Muuta lisäraportointivaluuttaa**-eräajon **OK**-painiketta.  

## <a name="see-also"></a>Katso myös
[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

