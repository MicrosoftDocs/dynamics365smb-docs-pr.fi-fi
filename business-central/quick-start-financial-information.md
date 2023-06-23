---
title: Taloudellisten tietojen pika-aloitus
description: Valmista yrityksesi liiketoimintaa varten määrittämällä taloustiedot Business Centralissa.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start" />Taloudellisten tietojen pika-aloitus

Kun olet syöttänyt perustiedot yrityksestä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan, jokin seuraavista vaiheista täydentää talousosiota. Teet tämän paitsi vastaanottaaksesi tai suorittaaksesi maksuja, myös hallitaksesi ja raportoidaksesi yrityksesi lukuja oikein.

## <a name="the-chart-of-accounts" />Tilikartta

Tilikartta tarjoaa yleiskuvan yrityksen taloudesta ja listaa tilit strukturoituihin ryhmiin, kuten varat, velat, tuotot, myytyjen tavaroiden kustannukset ja kulut. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää vakiotilikartan, jonka voit mukauttaa yrityksesi kirjanpitokäytäntöjen mukaan.

## <a name="set-up-the-chart-of-accounts" />Tilikartan määrittäminen

Seuraavassa videossa kerrotaan, miten voit määrittää tilikartan [!INCLUDE[prod_short](includes/prod_short.md)]issa.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts" />Lisää tili tilikarttaan

Jos haluat lisätä tilin, joka ei sisälly oletusarvoisesti [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen–esimerkiksi puutarhanhoitopalvelut–toimi seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta**, valitse sitten vastaava linkki.
2. Avaa **KP-tilikortti**-sivu valitsemalla **Uusi**-toiminto.
3. Syötä seuraavat tiedot vastaaviin **Yleinen**-pikalomakkeen kenttiin. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Kenttä | Tiedot |
   | --- | --- |
   | **Ei.** | 61250 |
   | **Nimi** | Puutarhanhoitopalvelut |
   | **Tulos/Tase** | Tuloslaskelma |
   | **Tililuokka** | Kulu |
   | **Tilin aliluokka** | Korjauksen ja ylläpidon kulut |
   | **Debet/Kredit** | Molemmat |
   | **Tilityyppi** | Kirjaus |

4. Lisää seuraavat tiedot **Kirjaus**-pikavälilehteen:

   | Kenttä | Tiedot |
   | --- | --- |
   | **Yleinen kirjaustyyppi** | Ostot |
   | **Ylein. liiketoim. kirjausryhmä** | Kotimaan |
   | **Yleinen tuotteen kirjausryhmä** | Palvelut |

5. Täytä puuttuvat kentät **KP-tilikortti**-sivulla tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts" />Yleiskuvan saaminen tilikartasta

Jos tarvitset tiiviimmän näkymän tilikartasta ilman sarakkeita kirjausryhmille, kirjaustyypille tai kustannustyypeille, esimerkiksi **Tilikartan yleiskatsauksessa** luetellaan kunkin tilin tärkeimmät tiedot pienemmässä taulukossa. Lisäksi voit kutistaa tai laajentaa ryhmiä kätkemään niiden sisällä olevat tilit.

Jos haluat näyttää yleiskatsauksen, valitse **Tilikartta**-sivulla **Tilikartan yleiskuvaus** -toiminto tai etsi ominaisuus käyttämällä ![Lamppu, joka avaa kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -toimintoa.

Lisätietoja tilikartasta ja pääkirjanpidosta on kohdassa [Tietoja pääkirjanpidosta ja tilikartoista](finance-general-ledger.md).

## <a name="set-up-bank-accounts" />Pankkitilien määrittäminen

Pankkitilit [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa rekisteröidään pankkitapahtumia varten, ja ne liittyvät tilikartan tapahtumiin. Seuraavassa videossa kerrotaan, miten voit määrittää pankkitilit.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit**, valitse sitten vastaava linkki.
2. Valitse **Pankkitilit**-sivulla **Uusi**-toiminto.
3. Valitse **Nro**-kenttään -kenttään tunniste, kuten *B010*, syötetään automaattisesti, jos pankkitileille on määritetty numeroitu sarjaluettelo. Jos ei, syötä yksilöllinen yhdistelmä.

   Kenttä eroaa **pankkitilin nro** -kentästä, joka on käytettävissä myös **Yleinen**-pikavälilehdessä.
4. Täytä **Pankkitilikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learnlearnpathsset-up-financial-management-dynamics-365-business-central" />Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also" />Katso myös

[Tilikartan määrittäminen](finance-setup-chart-accounts.md)  
[Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md)  
[Suorita ja tulosta raportteja](ui-work-report.md)  
[Business Centralin pika-aloitus](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
