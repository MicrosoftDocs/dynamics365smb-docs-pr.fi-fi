---
title: Asiakkaiden synkronointi
description: Asiakkaiden tuominen tai vieminen Shopifyista tai Shopifyihin
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 1a796d1094401cd2ebc0efd54f752211d22bfb12
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728651"
---
# <a name="synchronize-customers"></a>Asiakkaiden synkronointi

Kun tilaus tuodaan Shopifysta, asiakkaan tietojen hankkiminen on olennaista asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Nämä ovat olemassa kaksi päävaihtoehtoa ja niiden yhdistelmät:

* Käytä erikoisasiakasta kaikissa tilauksissa.
* Tuo todelliset asiakastiedot Shopify-tiedoista. Tämä valinta on käytettävissä myös silloin, kun viet asiakkaan Shopifyhin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Tärkeät asetukset tuotaessa asiakkaita Shopifysta

Tuotpa asiakkaita Shopifysta joukkona tai samaan aikaan kun tuot tilauksia, seuraavien asetusten avulla voit hallita prosessia:

|Kenttä|Kuvaus|
|------|-----------|
|**Asiakkaan tuonti Shopifysta**|Valitse **Kaikki asiakkaat**, jos aiot tuoda asiakkaita Shopifysta joukkona, joko manuaalisesti käyttämällä **Synkronoi asiakkaat** -toimintoa tai työjonon kautta toistuvia päivityksiä varten. Valinnasta huolimatta asiakastiedot tuodaan aina yhdessä tilauksen kanssa. Näiden tietojen käyttäminen riippuu kuitenkin **Shopifyn asiakasmalleista** ja asetuksista **asiakkaan yhdistämismäärityksen tyyppi** -kentässä.|
|**Asiakkaan yhdistämismäärityksen tyyppi**|Määritä, kuinka haluat yhdistimen suorittavan yhdistämisen.<br>- **Sähkö postilla/puhelimitse** jos haluat, että yhdistin yhdistää tuodun Shopify-asiakkaan olemassa olevaan asiakkaaseen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa sähköpostin ja puhelimen avulla.</br>- **Laskutustietojen mukaan** jos haluat, että liitin käyttää laskun vastaanottajan osoitetta yhdistääkseen tuodun Shopify-asiakkaan olemassa olevaan asiakkaaseen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa käyttämällä laskun vastaanottavan osapuolen osoitetietoja.</br>- Valitse **Ota aina oletusasiakas**, jos haluat, että järjestelmä käyttää asiakasta **oletusasiakasnro** -kentässä. |
|**Shopify voi päivittää asiakkaat**| Valitse tämä kenttä, jos haluat, että yhdistin päivittää löydetyt asiakkaat, kun joko **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**.|
|**Luo tuntemattomat asiakkaat automaattisesti**| Valitse tämä kenttä, jos haluat, että yhdistin luo puutuvat asiakkaat, kun **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**. Uusi asiakas luodaan käyttämällä tuotuja tietoja ja **asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortilla** tai **Shopify-asiakasmalli**-sivuilla. Huomaa, että Shopify-asiakkaalla täytyy olla vähintään 1 osoite. Jos tämä asetus ei ole käytössä, sinun on luotava asiakas manuaalisesti ja linkitettävä se Shopify-asiakkaaseen. Voit aina aloittaa asiakkaan luomisen manuaalisesti **Shopify-tilaus**-sivulta.|
|**Asiakasmallin koodi**|Tätä kenttää käytetään yhdessä **Tuntemattomien asiakkaiden luominen automaattisesti** -toiminnon kanssa.<br>- Valitse oletusmalli, jota käytetään automaattisesti luoduille asiakkaille. Varmista, että valitussa mallissa on pakolliset kentät, kuten **Yleinen liiketoiminnan kirjausryhmä**, **Asiakkaan kirjausryhmä**, arvonlisävero- (ALV) tai veroihin liittyvät kentät.<br>- Voit määrittää malleja kullekin maalle/alueelle **Shopify-asiakasmallit** -sivulla, josta on hyötyä asianmukaisen veron laskentaan. <br>- Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Asiakasmalli maata kohti

Jotkin asetukset voidaan määrittää maan tai alueen tasolla tai osavaltion/provinssin tasolla. Asetukset voidaan määrittää kohdassa [Toimitus-ja toimitus](https://www.shopify.com/admin/settings/shipping) Shopifyssa.

Voit tehdä seuraavan toimen kullekin asiakkaalle **Shopify-asiakasmallin** avulla:

1. Määritä **oletusasiakasnro**, joka on etusijalla **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentissä olevan valinnan. Sitä käytetään tuodussa myyntitilauksessa.
2. **Määritä asiakasmallin koodi**, jota käytetään puuttuvien asiakkaiden luomisessa, jos **Luo automaattisesti tuntemattomat asiakkaat** on otettu käyttöön. Jos **asiakasmallin koodi** on tyhjä, funktio käyttää **Asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortissa**.
3. Määritä, sisällytetäänkö tuotujen tilausten hintoihin ALV/verot.
4. Joissakin tapauksissa maalle määritetty **asiakasmallin koodi** ei riitä varmistamaan verojen oikeaa laskentaa (esimerkiksi maissa, joissa on myyntivero). Tässä tapauksessa **Veroalueiden** sisällyttäminen voi olla hyödyllinen lisäys.

> [!NOTE]  
> Maakoodit ovat ISO 3166-1 alpha-2-maakoodeja. Lisätietoja kohdassa [maakoodi](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Vie asiakastiedot Shopifyhin

Voit viedä olemassa olevat asiakkaat Shopifyhin joukkona. Kussakin tapauksessa luodaan asiakas ja yksi oletusosoite. Voit hallita prosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Vie asiakastiedot Shopifyhin**|Valitse tämä, jos suunnittelet vieväsi kaikki ne asiakkaat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyhin joukkona. Voit tehdä sen joko manuaalisesti käyttämällä **Synkronoi asiakkaat** -toimintoa tai automaattisesti käyttämällä työjonoa toistuvia päivityksiä varten.<br> Kun viet asiakkaita, joiden osoitteet sisältävät maakunnan/valtion, varmista, että maiden/alueiden **ISO-koodi** on täytetty.|
|**Voi päivittää Shopify-asiakkaat**|Tätä käytetään yhdessä **Vie asiakas Shopifyhin** -asetuksen kanssa. Ota se käyttöön, jos haluat luoda päivityksiä myöhemmin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa Shopifyssa oleville asiakkaille.|

Seuraavat vaatimukset koskevat asiakkaan viemistä:

* Asiakkaalla täytyy olla voimassa oleva sähköpostiosoite.
* Maa tai alue valitaan asiakaskortista, paikallisille asiakkaille, tyhjällä maalla tai alueella **Yrityksen tiedot** -sivulla määritellyllä maalla tai alueella on oltava ISO-koodi määritelty.
* Jos asiakkaalla on puhelinnumero, numeron täytyy olla yksilöivä, koska Shopify ei hyväksy toista asiakasta, jolla on sama puhelinnumero.
* Jos asiakkaalla on puhelinnumero, sen täytyy olla E.164-muodossa. Eri muotoja tuetaan, jos ne edustavat numeroa, joka voidaan soittaa kaikkialta maailmasta. Seuraavat muodot ovat kelvollisia:
  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Kun olet luonut asiakkaat Shopifyssa, voit lähettää heille suoria kutsuja kannustaaksesi heitä aktivoimaan tilinsä.

### <a name="populate-customer-information-in-shopify"></a>Asiakastietojen täyttäminen Shopifyssa

Shopifyssa asiakkaalla on etunimi, sukunimi, sähköpostiosoite ja/tai puhelinnumero. Etunimen ja sukunimen voi syöttää [!INCLUDE[prod_short](../includes/prod_short.md)]issa asiakaskortin perusteella.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Yhteyshenkilön nimi**|Korkein prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Yhteystiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|2|**Nimi 2**|Jos **Nimi 2** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimi 2 -tiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|3|**Nimi**|Alin prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimitiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|

Shopifyssa asiakkaalla on myös oletusosoite, joka voi sisältää yrityksen ja osoitteen etunimen, sukunimen, sähköpostiosoitteen ja/tai puhelimen lisäksi. Voit täyttää **Yritys**-kentän [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman asiakaskortin tietojen perusteella.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Nimi**|Korkein prioriteetti, jos **Nimilähde**-kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|
|2|**Nimi 2**|Alin prioriteetti, jos **Nimi 2 lähde** -kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|

Valitse osoitteissa, joissa käytetään maata tai provinssia, valitsemalla *Koodi* tai *Nimi* -ostoskortin **Maalähde**-kentässä **Shopify-ostoskortissa**. Tämä määrittää **maa**-kentän [!INCLUDE[prod_short](../includes/prod_short.md)] -kohteeseen tallennettavien tietojen tyypin.

## <a name="sync-customers"></a>Synkronoi asiakkaat

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse määrättykauppa, jolle haluat synkronoida asiakkaat.
3. Valitse **Synkronoi asiakkaat** -toiminto.

Vaihtoehtoisesti voit käyttää **Käynnistä asiakkaan synkronointi** - toimintoa **Shopify-asiakkaat**-ikkunassa tai hae **Synkronoi asiakkaat** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
