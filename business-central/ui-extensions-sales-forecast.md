---
title: Varaston hallinta myynnin ja varaston ennustelaajennuksen avulla
description: Tällä laajennuksella voi ennakoida myyntiä ja saada selkeän käsityksen odotettavissa olevista varaston loppumisesta. Se myös auttaa luomaan täydennyspyyntöjä toimittajille.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Myynti- ja varastoennustelaajennus

Varaston hallintaan kuuluvat sekä asiakaspalvelu että kustannusten hallinta. Pieni varasto vaatii vähemmän liikepääomaa, mutta toisaalta varaston loppumiset voivat aiheuttaa myyntimenetyksiä. Myynti- ja varastoennuste -laajennus ennustaa mahdollisen myynnin aiempien tietojen avulla. Se tarjoaa selvän yleiskuvan odotetuista varaston loppumisista. Ennusteen perusteella laajennus auttaa luomaan täydennyspyyntöjä toimittajille, ja säästää näin aikaasi.  

## Ennusteiden määrittäminen

[Azure AI](https://azure.microsoft.com/overview/ai-platform/) -yhteys on muodostettu valmiiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Voit kuitenkin määrittää ennusteen niin, että se käyttää raportoinnissa erityyppistä kautta. Ennuste voidaan laatia esimerkiksi kuukauden sijaan neljännesvuosittain. Voit myös valita ennustelaskelmassa käytettävien kausien määrän sen mukaan, miten hajautetun ennusteen haluat. Ennusteen voi tehdä esimerkiksi kuukautta kohti 12 kuukauden ajalle.

> [!TIP]  
> Mieti, miten pitkiä jaksoja palvelun laskelmissa käytetään. Mitä enemmän tietoja on käytettävissä, sitä tarkempia ennusteet ovat. Varo myös suuria jaksovaihteluita. Ne vaikuttavat myös ennusteisiin. Jos Azure AI ei löydä riittävästi tietoja tai tiedot ovat kovin erilaisia, palvelu ei voi tehdä ennustetta.

## Ennusteiden käyttäminen

Laajennus ennustaa Azure AI:n avulla tulevan myynnin myyntihistorian perusteella. Näin voidaan välttää puutteet varastossa. Jos esimerkiksi valitset nimikkeen **Nimikkeet**-sivulla, kaavion **Nimikkeen ennuste** -ruudussa näkyy tämän nimikkeen arvioitu myynti tulevan kauden aikana. Näin näet, onko nimike loppumassa varastosta lähiaikoina.  

Voit käyttää laajennusta myös varaston täydennysajankohdan ehdottamisessa. Voit esimerkiksi luoda ostotilauksen Fabrikamille sen uuden toimistotuolin ostamista varten. Myynti- ja varastoennustelaajennus saattaa ehdottaa, että täydennät myös yleensä tältä toimittajalta hankkimasi LONDON-kääntötuolin varastoa. Laajennus voi ennustaa LONDON-toimistotuolien loppuvan varastosta pian. Tuoleja siis kannattaa ostaa lisää jo nyt.  

## Rakennetiedot

[!INCLUDE[prod_short](includes/prod_short.md)]:n tilaukset sisältävät käyttöoikeuden useisiin ennakoitaviin verkkopalveluihin kaikilla alueilla, joilla [!INCLUDE[prod_short](includes/prod_short.md)] on saatavissa. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/en-us/business-central/overview/) verkkosivulla. 

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja.

> [!NOTE]  
>   Voit käyttää myös omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Myynnin ja varaston ennusteiden ennakoivan verkkopalvelun luominen ja käyttäminen](#AnchorText). 

### Ennusteeseen vaadittavat tiedot

Jos haluat tehdä ennusteita tulevasta myynnistä, verkkopalvelu vaatii määrällisiä tietoja aiemmasta myynnistä. Nämä tiedot saadaan **Kirjauspäivämäärä**-, **Nimikenro**- ja **Määrä**-kentistä **Nimiketapahtumat**-sivulla, jossa:

- Tapahtumatyyppi on Myynti.
- Kirjauspäivämäärä on **Myynnin ja varaston ennusteiden asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen kuin käytät verkkopalvelua, [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **Nimikenro**- ja **Kirjauspäivämäärä**-kenttien mukaan **Kauden tyyppi** -kentän perusteella **Myynnin ja varaston ennusteiden määritykset** -sivulla.

## <a name="AnchorText"> </a>Myynnin ja varaston ennusteiden ennakoivan verkkopalvelun luominen ja käyttäminen

Jotta [!INCLUDE[prod_short](includes/prod_short.md)] toimii verkossa Microsoft julkaisee mallin ja yhdistää sen Microsoft-tilaukseen. Toisia käyttöönottovaihtoehtoja varten on luotava koneoppimisen resursseja omassa Azure-tilauksessaan. Esimerkkivaiheita: [esimerkkiraportti](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tämän tehtävän tarkoituksena on noutaa ohjelmointirajapinnan URI ja ohjelmointirajapinnan avain.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynti- ja varastoennusteiden määritys** ja valitse sitten vastaava linkki.  
2. Laajenna **Yleistä**-pikavälilehti ja täytä sitten API-URL- ja API-avain-kentät.  

## Katso myös

[Myynti](sales-manage-sales.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Tekoälyn käyttäminen Microsoft Dynamics 365 Business Centralissa](/training/paths/use-artificial-intelligence/)  
[Ennusteiden ohjelmointirajapinnan yleiskatsaus](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
