---
title: Tarkista kirjanpitotilit
description: 'Voit seurata edistymistä, kun kirjaat pääkirjanpidon tileille.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Summien tarkistaminen kirjanpitotileillä

Sinulla voi olla pääkirjanpidon tilit, joita usein pidät silmällä. Tai haluat ehkä nopeuttaa tarkistusprosessia kuukauden lopussa. Jos tarvitset apua tekemiesi toimien seuraamisessa ja nopeuttaaksesi tarkistusta, käytä kunkin tilin **Tilikartan** tai **Kirjanpitotilikortti**-sivun **Tarkastusmerkinnät**-toimintoa. 

## <a name="set-up-accounts-for-reviews"></a>Määritä tilit tarkistusta varten

Määrittele kunkin tilin **KP-tilin kortti** -sivulla, miten **tarkistuskäytäntö**-kentän arvioita sallitaan.

|Tarkistuskäytäntö  |Kuvaus  |
|---------|---------|
|Ei yhtään     | Et voi merkitä tilin tapahtumia tarkistetuksi. Käytä tätä vaihtoehtoa esimerkiksi ostovelkojen, myyntisaamisten ja pankkitiliasiakkaiden osalta, joilla on muita tapoja tarkistaa niiden summia.        |
|Salli tarkistus     | Tarkistukseen ei tarvitse sisällyttää tapahtumia, ja debet- ja kredit-tapahtumien summan ei tarvitse täsmätä. Voit poistaa tarkistuksen esimerkiksi silloin, kun olet tehnyt virheen.        |
|Salli tarkistus ja täsmäytä saldo     | Tarkistuksen debet- ja kredit-tapahtumien kokonaissummien on vastattava toisiaan. Nämä summat näkyvät **debet**- ja **kredit**-kentissä, ja **Saldo**-kentässä näkyy kokonaissumma. Tämän asetuksen avulla voit myös poistaa arvostelun. Kun poistat arvostelun yhdestä tai useammasta kirjauksesta, debet- ja kredit-tapahtumien täytyy silti täsmätä.        |

## <a name="mark-entries-as-reviewed"></a>Merkitse tapahtumat tarkistetuiksi

Valitse tarkistamasi tapahtumat ja käytä sitten **Aseta valittu tarkistetuksi** -toimintoa. Joka kerran kun merkitsen yhden tai useamman merkinnän tarkistetuksi, tapahtumat saavat saman numeron **tarkistettu tunnus** -sarakkeessa. Tarkistettu tunnus on kätevä tapa seurata tapahtumia, jotka tarkistettiin samaan aikaan. [!INCLUDE [prod_short](includes/prod_short.md)] tallentaa myös tarkistuksen suorittaneen käyttäjän ja sen, milloin tarkistus tehtiin.

Jos merkitset tapahtumat tarkistetuiksi, mutta kadut sitä, käytä **Määritä ei-tarkistetuksi** -toimintoa.

* Jos arvostelun sallittu käytäntö on määritetty tilille, toiminto palauttaa tarkistettujen tunnisteiden arvoksi 0 ja poistaa tarkistuksen henkilön sekä päivämäärän ja ajan. 
* Jos tarkistuksen salliminen ja saldon kohdistaminen myönnetään, kreditin ja debetin on oltava edelleen tasapainossa. Jos esimerkiksi jokin arvostelun tapahtumista on virhe, voit valita toisen tapahtuman, jolla on oikea arvo. Korvaavalla tapahtumalla ei tarvitse olla samaa tarkistettujen tunnusten tunnusta.

> [!TIP]
> Nopea tapa valita useita merkintöjä on pitää Ctrl- tai vaihto-näppäimiä painettuna, kun valitset tapahtumat. Ctrl-näppäimen avulla voit valita tiettyjä tapahtumia, ja vaihto valitsee kaikki tapahtumat ensimmäisen ja viimeisen valitsemasi merkinnän välillä.

## <a name="review-accounts-that-have-old-entries"></a>Tarkista tilit, joilla on vanhoja tapahtumia

Sinulla voi olla aiempien kausien tapahtumia, jotka olet jo tarkistanut tai jotka eivät tarvitse tarkistusta. Haluat vain aloittaa tapahtumien tarkistamisen esimerkiksi vuoden tai kirjanpitojakson alusta. Voit jättää tapahtumat ennalleen. Jos kuitenkin haluat analysoida tietoja Excelissä tai käyttämällä analyysitilaa, merkitse tapahtumat tarkistetuiksi. Lisätietoja tapahtumien analysoinnista on kohdassa [Merkintöjen analysoiminen](#analyze-entries). Voit merkitä tapahtumat tarkistetuiksi lisäämällä suodatinruutuun suodattimen, joka näyttää vain kyseiset tapahtumat, ja valitsemalla sitten **Merkitse valitut tapahtumat tarkistetuksi** -toiminnon.

## <a name="filter-entries"></a>Suodata tapahtumat

Jotta voisit saada selkeämmän kuvan, voit suodattaa tapahtumia **Tarkista KP-tapahtumat** -sivulla usealla eri tavalla.

* **Näytä tarkistetut tapahtumat**- ja **Piilota tarkistetut tapahtumat** -toimintojen avulla voit tuoda näkyviin vain ne tapahtumat, joita olet tarkastellut tai joita et ole tarkistanut. Voit tyhjentää suodattimet käyttämällä **Näytä kaikki tapahtumat** -toimintoa.
* Suodatinruudun käyttäminen. Voit esimerkiksi suodattaa tilinumeron mukaan tai, jos sinulla on vanhoja tapahtumia ja haluat merkitä ne kaikki tarkistetuiksi, kirjauspäivämäärän mukaan.

## <a name="analyze-entries"></a>Analysoi tapahtumia

Tarkistamiasi pääkirjanpidon tapahtumia voi analysoida muutamalla eri tavalla.

* Ota analyysitila käyttöön, jos haluat esimerkiksi ryhmitellä tapahtumat tarkistettujen tunnusten mukaan. Lisätietoja analyysitilasta on kohdassa [Analysoi luettelosivun tiedot analyysitilan avulla](analysis-mode.md).
* Vie tapahtumat Exceliin.

## <a name="see-also"></a>Katso myös

[Pääkirjanpidon ja tilikartan ymmärtäminen](finance-general-ledger.md)  
[Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md)  
