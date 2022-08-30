---
title: Asiakkaiden synkronointi
description: Asiakkaiden tuominen tai vieminen Shopifyista tai Shopifyihin
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 0c1402c4f41f108b504ad31829ede5a1095b6ce4
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317324"
---
# <a name="synchronize-customers"></a>Asiakkaiden synkronointi

Kun tilaus tuodaan Shopifysta, asiakkaan tiedot ovat olennaisia asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. On olemassa kaksi päävaihtoehtoa ja niiden yhdistelmät:

* Käytä erikoisasiakasta kaikissa tilauksissa.
* Tuo todelliset asiakastiedot Shopify-tiedoista. Tämä valinta on käytettävissä myös silloin, kun viet asiakkaan Shopifyhin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Miten yhdistin valitsee käytettävän asiakkaan

*Tuo tilaus Shopifysta* -toiminto yrittää valita asiakkaan seuraavassa järjestyksessä:

1. Jos **Oletusasiakasnro** -kenttä määritetään vastaavan maan **Shopify-asiakasmallissa**, vastaavalle maalle, silloin **oletusasiakasnroa** käytetään, riippumatta **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentistä. Lisätietoja on osassa [Asiakasmalli maata kohti](synchronize-customers.md#customer-template-per-country).
2. Jos **Asiakkaan tuonti Shopifysta** on määritetty arvoon *Ei mitään* ja **Oletusasiakasnro** on määritetty **Shopify-ostoskortissa**, arvoa **Oletusasiakasnro** käytetään.

Seuraavat vaiheet määräytyvät **asiakkaan yhdistämismäärityksen tyypin** mukaan.

* **Ota aina oletusasiakas**, jolloin yhdistin käyttää asiakasta, joka on määritetty **oletusasiakasnro** -kentässä **Shopify-ostoskortti**-sivulla.
* **Sähköpostilla/puhelimella**-yhdistin yrittää löytää nykyisen asiakkaan ensin tunnuksella, sitten sähköpostitse, ja sitten puhelimitse. Jos asiakasta ei löydy - yhdistin luo uuden asiakkaan.
* **Laskutustiedoilla**, yhdistin yrittää löytää olemassa olevan asiakkaan ensin tunnuksella ja sitten laskutusosoitteen tiedoilla. Jos ei löydy - yhdistin luo uuden asiakkaan.

> [!NOTE]  
> Yhdistin käyttää laskutusosoitteen tietoja ja luo laskutusasiakkaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tilausasiakas on sama kuin laskutusasiakas.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Tärkeät asetukset tuotaessa asiakkaita Shopifysta

Joko tuot asiakkaita Shopifysta joukkona tai yhdessä tilausten tuonnin kanssa, seuraavat asetukset mahdollistavat prosessin hallinnan:

|Kenttä|Kuvaus|
|------|-----------|
|**Asiakkaan tuonti Shopifysta**|Valitse **Kaikki asiakkaat**, jos aiot tuoda asiakkaita Shopifysta joukkona, joko manuaalisesti käyttämällä **Synkronoi asiakkaat** -toimintoa tai työjonon kautta toistuvia päivityksiä varten. Valinnasta huolimatta asiakastiedot tuodaan aina yhdessä tilauksen kanssa. Näiden tietojen käyttäminen riippuu kuitenkin **Shopifyn asiakasmalleista** ja asetuksista **asiakkaan yhdistämismäärityksen tyyppi** -kentässä.|
|**Asiakkaan yhdistämismäärityksen tyyppi**|Määritä, kuinka haluat yhdistimen suorittavan yhdistämisen.<br>- **Sähkö postilla/puhelimitse** jos haluat, että yhdistin yhdistää tuodun Shopify-asiakkaan olemassa olevaan asiakkaaseen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa sähköpostin ja puhelimen avulla.</br>- **Laskutustietojen mukaan** jos haluat, että yhdistin yhdistää tuodun Shopify-asiakkaan olemassa olevaan asiakkaaseen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa käyttämällä laskun vastaanottavan osapuolen osoitetietoja.</br>Valitse **Ota aina oletusasiakas**, jos haluat, että järjestelmä käyttää asiakasta **oletusasiakasnro** -kentässä. |
|**Shopify voi päivittää asiakkaat**| Valitse tämä vaihtoehto, jos haluat, että yhdistin päivittää löydetyt asiakkaat, kun **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**.|
|**Luo tuntemattomat asiakkaat automaattisesti**| Valitse tämä vaihtoehto, jos haluat, että yhdistin luo puutuvat asiakkaat, kun **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**. Uusi asiakas luodaan käyttämällä tuotuja tietoja ja **asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortilla** tai **Shopify-asiakasmalli**-sivuilla. Huomaa, että Shopify-asiakkaalla täytyy olla vähintään 1 osoite. Jos tämä asetus ei ole käytössä, sinun on luotava asiakas manuaalisesti ja linkitettävä se Shopify-asiakkaaseen. Voit aina aloittaa asiakkaan luomisen manuaalisesti **Shopify-tilaus**-sivulta.|
|**Asiakasmallin koodi**|Käytetään yhdessä **Tuntemattomien asiakkaiden luominen automaattisesti** -toiminnon kanssa.<br> Valitse oletusmalli, jota käytetään automaattisesti luoduille asiakkaille. Varmista, että valitussa mallissa on pakolliset kentät, kuten **Yleinen liiketoiminnan kirjausryhmä**, **Asiakkaan kirjausryhmä**, ALV:hen tai veroihin liittyvät kentät.<br> Voit määrittää malleja kullekin maalle/alueelle **Shopify-asiakasmallit** -sivulla, josta on hyötyä asianmukaisen veron laskentaan. <br>Lisätietoja on kohdassa [Verotuksen määritykset](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Asiakasmalli maata kohti

Jotkin asetukset voidaan määrittää maan tai alueen tasolla tai osavaltion/provinssin tasolla. Asetukset voidaan määrittää kohdassa [Toimitus-ja toimitus](https://www.shopify.com/admin/settings/shipping) Shopifyssa.

**Shopify-asiakasmallin** avulla voit tehdä seuraavat toimet kunkin maan osalta:

1. Määritä **oletusasiakasnro**, joka on etusijalla **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentissä olevan valinnan. Sitä käytetään tuodussa myyntitilauksessa.
2. **Määritä asiakasmallin koodi**, jota käytetään puuttuvien asiakkaiden luomisessa, jos **Luo automaattisesti tuntemattomat asiakkaat** on otettu käyttöön. Jos **asiakasmallin koodi** on tyhjä, funktio käyttää **Asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortissa**.
3. Määritä, sisällytetäänkö tuotujen tilausten hintoihin verot/ALV.
4. Joissakin tapauksissa **asiakasmallin koodi** maata kohti määritettynä ei riitä varmistamaan verojen oikeaa laskentaa. Esimerkiksi maissa, joissa on käytössä arvonlisävero. Tässä tapauksessa **Veroalueet** voi olla hyödyllinen lisäys.

> [!NOTE]  
> Maakoodit ovat ISO 3166-1 alpha-2-maakoodeja. Lisätietoja on [Maakoodi](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode)-sivustossa.

## <a name="export-customers-to-shopify"></a>Vie asiakastiedot Shopifyhin

Olemassa olevat asiakkaat voidaan viedä Shopifyhin joukkona. Tämän seurauksena luodaan asiakas ja yksi oletusosoite. Voit hallita prosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Vie asiakastiedot Shopifyhin**|Valitse, jos aiot viedä kaikki asiakkaat, joilla on voimassa oleva sähköpostiosoite [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyhin kerralla. Joko manuaalisesti **Synkronoi asiakkaat** -toiminnolla tai työjonon kautta toistuvia päivityksiä varten.<br> Kun viet asiakkaita, joissa on maakunta/valtio, varmista, että maiden/alueiden **ISO-koodi** on täytetty.|
|**Voi päivittää Shopify-asiakkaat**|Käytetään yhdessä **Vie asiakas Shopifyhin** -asetuksen kanssa. Ota se käyttöön, jos haluat luoda päivityksiä myöhemmin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa Shopifyssa oleville asiakkaille.|

> [!NOTE]  
> Kun olet luonut asiakkaat Shopifyhin, haluat ehkä lähettää suoria kutsuja asiakkaille. Se kannustaa heitä aktivoimaan tilinsä.

### <a name="populate-customer-information-in-shopify"></a>Asiakastietojen täyttäminen Shopifyssa

Shopifyssa asiakkaalla on etunimi, sukunimi, sähköpostiosoite ja/tai puhelinnumero. Etunimen ja sukunimen voi täyttää [!INCLUDE[prod_short](../includes/prod_short.md)]issa asiakaskortin perusteella.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Yhteyshenkilön nimi**|Korkein prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Yhteystiedot**-kenttä sisältää *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|2|**Nimi 2**|Jos **Nimi 2** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimi 2 -tiedot**-kenttä sisältää *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|3|**Nimi**|Alin prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimitiedot**-kenttä sisältää *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|

Shopifyssa asiakkaalla on myös oletusosoite, jonka lisäksi etunimi, sukunimi, sähköpostiosoite ja/tai puhelin voivat sisältää yrityksen ja osoitteen. Voit täyttää **Yritys**-kentän [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman asiakaskortin tietojen perusteella.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Nimi**|Korkein prioriteetti, jos **Nimilähde**-kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|
|2|**Nimi 2**|Alin prioriteetti, jos **Nimi 2 lähde** -kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|

Valitse osoitteissa, joissa käytetään maata tai provinssia, valitsemalla *Koodi* tai *Nimi* **Shopify-ostoskortin** **Maalähde**-kentässä määrittääksesi, minkä tyyppisiä tietoja tallennetaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa **Maa**-kentässä.

## <a name="sync-customers"></a>Synkronoi asiakkaat

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida asiakkaat avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi asiakkaat** -toiminto.

Vaihtoehtoisesti voit käyttää **Käynnistä asiakkaan synkronointi** - toimintoa **Shopify-asiakkaat**-ikkunassa tai hae **Synkronoi asiakkaat** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoitus](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
