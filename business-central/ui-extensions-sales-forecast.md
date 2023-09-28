---
title: Varaston hallinta myynnin ja varaston ennustelaajennuksen avulla | Microsoft Docs
description: Tällä laajennuksella voi ennakoida myyntiä ja saada selkeän käsityksen odotettavissa olevista varaston loppumisesta. Se myös auttaa luomaan täydennyspyyntöjä toimittajille.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Myynti- ja varastoennustelaajennus

Varaston hallintaan kuuluvat sekä asiakaspalvelu että kustannusten hallinta. Pieni varasto vaatii vähemmän liikepääomaa, mutta toisaalta varaston loppumiset voivat aiheuttaa myyntimenetyksiä. Myynti- ja varastoennuste -laajennus ennustaa mahdollisen myynnin aiempien tietojen avulla. Se tarjoaa selvän yleiskuvan odotetuista varaston loppumisista. Ennusteen perusteella laajennus auttaa luomaan täydennyspyyntöjä toimittajille, ja säästää näin aikaasi.  

## <a name="setting-up-forecasting"></a>Ennusteiden määrittäminen

[Azure AI](https://azure.microsoft.com/overview/ai-platform/) -yhteys on muodostettu valmiiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Voit kuitenkin määrittää ennusteen niin, että se käyttää raportoinnissa erityyppistä kautta. Ennuste voidaan laatia esimerkiksi kuukauden sijaan neljännesvuosittain. Voit myös valita ennustelaskelmassa käytettävien kausien määrän sen mukaan, miten hajautetun ennusteen haluat. Ennusteen voi tehdä esimerkiksi kuukautta kohti 12 kuukauden ajalle.

> [!TIP]  
> Mieti, miten pitkiä jaksoja palvelun laskelmissa käytetään. Mitä enemmän tietoja on käytettävissä, sitä tarkempia ennusteet ovat. Varo myös suuria jaksovaihteluita. Ne vaikuttavat myös ennusteisiin. Jos Azure AI ei löydä riittävästi tietoja tai tiedot ovat kovin erilaisia, palvelu ei voi tehdä ennustetta.

## <a name="use-the-forecasts"></a>Ennusteiden käyttäminen

Laajennus ennustaa Azure AI:n avulla tulevan myynnin myyntihistorian perusteella. Näin voidaan välttää puutteet varastossa. Jos esimerkiksi valitset nimikkeen **Nimikkeet**-sivulla, kaavion **Nimikkeen ennuste** -ruudussa näkyy tämän nimikkeen arvioitu myynti tulevan kauden aikana. Näin näet, onko nimike loppumassa varastosta lähiaikoina.  

Voit käyttää laajennusta myös varaston täydennysajankohdan ehdottamisessa. Jos esimerkiksi luot ostotilauksen Fabrikamille, koska haluat ostaa heiltä uuden työtuolin, Myynti- ja varastoennuste -laajennus ehdottaa, että samalla kannattaa ostaa LONDON-toimistotuoleja, joita yleensä ostat kyseiseltä toimittajalta. Laajennus ehdottaa tätä sen vuoksi, koska se ennustaa LONDON-toimistotuolien loppuvan varastosta kahden seuraavan kuukauden aikana. Tuoleja siis kannattaa ostaa lisää jo nyt.  

## <a name="design-details"></a>Rakennetiedot

[!INCLUDE[prod_short](includes/prod_short.md)]:n tilaukset sisältävät käyttöoikeuden useisiin ennakoitaviin verkkopalveluihin kaikilla alueilla, joilla [!INCLUDE[prod_short](includes/prod_short.md)] on saatavissa. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/en-us/business-central/overview/) verkkosivulla. 

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja.

> [!NOTE]  
>   Voit käyttää myös omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Myynnin ja varaston ennusteiden ennakoivan verkkopalvelun luominen ja käyttäminen](#AnchorText). 

### <a name="data-required-for-forecast"></a>Ennusteeseen vaadittavat tiedot

Jos haluat tehdä ennusteita tulevasta myynnistä, verkkopalvelu vaatii määrällisiä tietoja aiemmasta myynnistä. Nämä tiedot saadaan **Kirjauspäivämäärä**-, **Nimikenro**- ja **Määrä**-kentistä **Nimiketapahtumat**-sivulla, jossa:

- Tapahtumatyyppi on Myynti.
- Kirjauspäivämäärä on **Myynnin ja varaston ennusteiden asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen kuin käytät verkkopalvelua, [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **Nimikenro**- ja **Kirjauspäivämäärä**-kenttien mukaan **Kauden tyyppi** -kentän perusteella **Myynnin ja varaston ennusteiden määritykset** -sivulla.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Myynnin ja varaston ennusteiden ennakoivan verkkopalvelun luominen ja käyttäminen

Voit myös luoda oman ennakoivan verkkopalvelun **Microsoft Business Central -sovelluksen ennustemalli** -nimisen julkisen mallin perusteella. Tämä ennakoiva malli on saatavana verkossa Azure AI Galleryssa. Voit käyttää mallia seuraavien vaiheiden avulla:  

1. Avaa selain ja siirry [Azure AI Galleryyn](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Etsi **Ennustusmalli Microsoft Business Centralille** ja avaa malli Azuren koneoppimisstudiossa.  
3. Kirjaudu työtilaan Microsoft-tilin avulla ja kopioi malli.  
4. Aja malli ja julkaise se verkkopalveluna.  
5. Kirjoita API:n URL-osoite ja API-avain muistiin. Näitä tunnistetietoja käytetään kassavirran asetuksissa.  
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynti- ja varastoennusteiden määritys** ja valitse sitten vastaava linkki.  
7. Laajenna **Yleistä**-pikavälilehti ja täytä sitten API-URL- ja API-avain-kentät.  

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Tekoälyn käyttäminen Microsoft Dynamics 365 Business Centralissa](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
