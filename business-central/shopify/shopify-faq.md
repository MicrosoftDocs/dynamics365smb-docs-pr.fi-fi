---
title: Teknisten tietojen UKK
description: Shopify-yhdistimeen liittyvät toteutustiedot.
ms.date: 01/24/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="faq-for-technical-details"></a>Teknisten tietojen UKK

Tämä artikkeli vastaa Shopify-yhdistintä koskeviin yleisimpiin kysymyksiin.

## <a name="what-is-shopify"></a>Shopifyn kuvaus

Shopify on tilauspohjainen sovellus, jonka avulla kuka tahansa voi perustaa verkkokaupan ja myydä tuotteitaan. Shopify-ympäristö tarjoaa verkkovähittäismyyjille palvelupaketin, johon kuuluu maksu-, markkinointi-, toimitus- ja asiakasvuorovaikutustyökaluja.

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Mikä on Microsoft Dynamics 365 Business Central Shopify -yhdistin?

Shopify-yhdistimen avulla yritykset voivat linkittää Shopify-kauppansa [!INCLUDE[prod_short](../includes/prod_short.md)]iin maksimoidakseen liiketoiminnan tuottavuuden. Käyttämällä Shopify-yhdistintä ne voivat käyttää ja hallita yrityksensä ja Shopify-verkkokauppansa merkityksellisiä tietoja yhtenä yksikkönä.

### <a name="capabilities"></a>Ominaisuudet

- Tuki useammalle kuin yhdelle Shopify-kaupalle
  - Jokaisella myymälällä on omat määrityksensä, kuten tuotekokoelma, varaston laskemiseen käytetyt sijainnit ja hinnastot.  
- Nimikkeiden tai tuotteiden kaksisuuntainen synkronointi
  - Yhdistin synkronoi kuvat, nimikevariantit, viivakoodit, toimittajien nimikenumerot, laajennetut tekstit ja tunnisteet.  
  - Nimikemääritteiden vienti Shopifyhin.  
  - Käytä valittuja asiakashintaryhmiä ja alennuksia määrittääksesi Shopifyhin vietyjä hintoja.  
  - Päätä, voidaanko nimikkeitä luoda automaattisesti vai sallitaanko vain päivitykset aiemmin luotuihin tuotteisiin.  
- Varastotasojen synkronointi
  - Valitse joitakin [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmassa käytettävissä olevista sijainneista tai ne kaikki.  
  - Päivitä usean sijainnin varastotasot Shopifyssa.  
- Asiakkaiden kaksisuuntainen synkronointi
  - Kohdista asiakkaat älykkäästi puhelinnumeron ja sähköpostiosoitteen perusteella.  
  - Käytä maa- ja aluekohtaisia malleja asiakkaiden luomisessa. Näin varmistetaan, että veroasetukset ovat oikein.  
- Tilausten tuonti Shopifysta
  - Sisällytä tilaukset, jotka on luotu eri myyntikanavissa, kuten verkkokaupassa tai **Shopify POS** -sovelluksessa.
  - Toimituskulut, lahjakortit, vinkit, toimitus- ja maksutavat, tapahtumat ja petosriski.  
  - Tuonnin aikana voit luoda automaattisesti asiakkaita [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmassa tai päättää hallita asiakkaita Shopifyssa.  
  - Vastaanota maksusuoritustietoja Shopify Paymentsista.
- Täyttämistietojen seuranta
  - Voit halutessa valita nimikeseurantatietojen siirron [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyhin.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Miksi Microsoft ja Shopify ryhtyivät tähän kumppanuuteen?

[!INCLUDE[prod_short](../includes/prod_long.md)] tekee yhteistyötä Shopifyn kanssa auttaakseen asiakkaitaan luomaan paremman ostoskokemuksen. Shopify tarjoaa kauppiaille helppokäyttöisen verkkokaupparatkaisun, kun taas [!INCLUDE[prod_short](../includes/prod_short.md)] tarjoaa kattavan liiketoiminnan hallintaratkaisun, joka tarjoaa kattavaa liiketoiminnan hallintaa talous-, myynti-, palvelu- ja toimintotiimien laajuisesti. Saumaton yhteys sovellusten välillä synkronoi tilaukset, varastot ja asiakastiedot, jotta kauppiaat voivat täyttää tilauksensa nopeammin ja palvella asiakkaitaan paremmin.

## <a name="which-microsoft-products-is-the-shopify-connector-available-for"></a>Mille Microsoft-tuotteille Shopify-yhdistin on saatavilla?

Tämä ominaisuus on käytössä vain [!INCLUDE[prod_short](../includes/prod_short.md)] onlinessa alkaen varsiosta 20.1. Sitä ei ole saatavilla paikallisiin ympäristöihin. Yhdistin on esiasennettu uusiin ympäristöihin. Organisaatiot, joilla on jo ympäristöjä, voivat ladata ja asentaa yhdistimen AppSourcesta. Organisaatiolla on oltava sekä [!INCLUDE [prod_short](../includes/prod_short.md)] -käyttöoikeus että Shopify-käyttöoikeus käyttääkseen yhdistintä. Lisätietoja tuetuista maista, alueista, kielistä ja [!INCLUDE[prod_short](../includes/prod_short.md)] -versioista on kohdassa [Shopify-yhdistin AppSourcessa](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-yhdistin ei toimi [upotetussa sovelluksessa](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), jossa asiakkaan URL-osoitteen muoto on `https://[application name].bc.dynamics.com`.

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Millaista tukea Shopify-yhdistimelle on tarjolla?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Nykyinen tukimalli kattaa Shopify-yhdistimen. Lisätietoja on kohdassa [Tekninen tuki](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (vain englanniksi).

Pyydä apua konsultilta, joka tuntee [!INCLUDE[prod_short](../includes/prod_short.md)] -ratkaisun Shopify-yhdistimen, vastataksesi yksilöllisiin liiketoimintavaatimuksiisi. Hae [konsulttipalveluista](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Jos haluat ohjeita Shopifyn käyttöön, aloita [Yleisestä Shopify ohjekeskuksesta](https://help.shopify.com/) tai [24/7-tuesta kaupallesi, kun olet Shopify-kauppias](https://help.shopify.com/questions#/).

Voit myös tutustua [Experts Marketplaceen](https://experts.shopify.com/) löytääksesi oikeat asiantuntijat, jotka tarjoavat palveluita Shopify-kauppiaille.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them"></a>Seuraavia ominaisuuksia ei tueta tällä hetkellä, mutta pidämme niitä silmällä ja saatamme harkita niiden lisäämistä

- B2B-ominaisuudet, mukaan lukien yritykset, yritysten hinnastot ja maksuehdot
  - B2B:n lisätuki on saatavilla vuoden 2024 1. julkaisuaallossa. Lisätietoja on kohdassa [Business Centralin yhdistäminen Shopifyn B2B:hen](/dynamics365/release-plan/2023wave2/smb/dynamics365-business-central/connect-business-central-shopify-b2b)
- Markkinat
  - Päätietojen useat käännökset. Voit valita yhden kielen, jota käytetään tuotetietojen viennissä.
  - Maa-/aluekohtaiset hinnat. Valitulle valuutalle on saatavilla yksi hinnasto. Shopify käsittelee muuntamisen muihin valuuttoihin.
- Tilausluonnokset

## <a name="is-the-shopify-connector-extensible"></a>Voidaanko Shopify-yhdistintä laajentaa?

Kyllä, Shopify-yhdistintä voidaan laajentaa. Tarkista GitHub ja tutustu [laajennettavuuspisteiden luetteloon](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) ja tutki joitakin [esimerkkejä](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## <a name="is-the-shopify-connector-open-for-contribution"></a>Voivatko muut osallistua Shopify-yhdistimen työstämiseen?

Kyllä, yhteisö voi osallistua tämän laajennuksen työstämiseen. Löydät [lähdekoodin](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) Microsoft AL -sovelluksen lisäosasäilöstä.

## <a name="building-your-version-of-shopify-connector"></a>Shopify-yhdistimen rakentaminen

Shopifyn mukaan, jos haluat luoda ja julkaista Shopify-markkinapaikalla yhdistinsovelluksen, jonka pääasiallisena tarkoituksena on siirtää tai jakaa kauppiastietoja kolmannelle osapuolelle ([!INCLUDE [prod_short](../includes/prod_short.md)]), sinulla on oltava Shopifyn kirjallinen suostumus. Osana tätä prosessia sinun tulee saada Microsoftin suostumus Loppuvastaanottajan tietojen kuittauslomake -lomakkeeseen. Meidän on pyydettävä sinua käsittelemään asiaa Shopifyn kanssa, koska Microsoft ei voi allekirjoittaa kolmansien osapuolten sopimuksia.

### <a name="what-to-do"></a>Mitä tehdä

Tarkista Shopifyn vaatimukset, koska sinulla voi vielä olla luetteloimaton sovellus.

Vaihtoehtoisesti Shopify Connector for [!INCLUDE [prod_short](../includes/prod_short.md)] saa jatkuvasti uusia ominaisuuksia ja uusia asiakkaita. Jos huomaat jonkin tietyn välin, harkitse tuote-ehdotuksen (https://aka.ms/bcideas) tai koodiehdotuksen sen lähettämistä [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmaan. Sellaisten tarpeiden osalta, jotka eivät välttämättä ole olennaisia suurimmalle osalle asiakkaita ja joita nykyinen laajennettavuusmalli ei pysty käsittelemään helposti, ota yhteyttä [!INCLUDE [prod_short](../includes/prod_short.md)] -kehitystiimiin voidaksesi keskustella käyttötapauksesta. Meidän pitäisi pystyä löytämään toteuttamiskelpoinen ratkaisu.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
