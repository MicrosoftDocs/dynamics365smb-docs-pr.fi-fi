---
title: "Myyntimahdollisuuksien käsitteleminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan myyntimahdollisuuksien käsitteleminen Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 889ef028b34ddad52c978373a5dab4329d96c91f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="processing-sales-opportunities"></a>Myyntimahdollisuuksien käsitteleminen
Mahdollisuuden luomisen jälkeen sen hallinnassa ja valmistumisprosessissa voidaan käyttää useita toimintoja.

## <a name="view-opportunities"></a>Mahdollisuuksien tarkasteleminen
Olemassa olevat myyntimahdollisuudet ovat käytettävissä **Mahdollisuusluettelo**-ikkunassa. Tätä ikkunaa voidaan käyttää seuraavilla tavoilla myyntimahdollisuuksien käsittelemisessä:

| Mahdollisuuksien tarkasteminen | Sitten |
| --- | --- |
| Kaikki myyjät ja kontaktit |Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Mahdollisuusluettelo** ja valitse sitten liittyvä linkki. |
| Määritetty myyjä |Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Myyjät** ja valitse sitten liittyvä linkki. Valitse myyjä, valitse sitten **Mahdollisuudet**-toiminto. Valitse tämän jälkeen **Luettelo**-toiminto. |
| Määritetty kontakti |Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kontaktit** ja valitse sitten liittyvä linkki. Valitse kontakti luettelosta ja valitse sitten **Mahdollisuudet**-toiminto. |

Jokainen näistä tehtävistä avautuu **Mahdollisuusluettelo**-ikkunaan.

## <a name="close-opportunities"></a>Mahdollisuuksien sulkeminen
Voit sulkea mahdollisuuden, kun neuvottelut ovat ohi. Mahdollisuuden sulkemisen yhteydessä voit määrittää, onko se voitettu vai menetetty ja sulkemisen syyt. Syyn määrittäminen edellyttää suljettujen mahdollisuuksien koodien määrittämistä.

1. Valitse **Mahdollisuusluettelo**-ikkunassa mahdollisuus ja valitse sitten **Sulje**-toiminto. **Sulje mahdollisuus** -ikkuna avautuu.
2. Täytä tarvittavat kentät ja valitse **OK**-painike.

   **Sulje mahdollisuuden koodi** - ja **Pvm suljettu** -kentät ovat pakollisia. Ne on täytettävä, ennen kun voi valita **OK**-painikkeen.

   Valitse **Sulje mahdollisuuden koodi** -kentässä jokin olemassa olevista suljettujen mahdollisuuksien koodeista tai lisää uusi koodi. Voit lisätä uuden koodin valitsemalla avattavasta luettelosta **Valitse koko luettelosta** ja valitsemalla sitten **Uusi**. Täytä tyhjän rivin **Koodi**-, **Tyyppi**- ja **Kuvaus**-kenttä ja valitse sitten **OK**-painike.

## <a name="create-quotes-for-opportunities"></a>Mahdollisuuksien tarjousten luominen
Voit luoda myyntitarjouksia kontakteille, joita ei ole tallennettu asiakkaiksi.

1. Valitse **Mahdollisuusluettelo**-ikkunassa mahdollisuus ja valitse sitten **Määritä myyntitarjous** -toiminto. **Myyntitarjous**-ikkuna aukeaa.
2. Täytä asianmukaiset kentät.

## <a name="create-sales-orders-for-opportunities"></a>Mahdollisuuksien myyntitilausten luominen
Voit tehdä myyntitilauksia niistä myyntitarjouksista, jotka olet luonut mahdollisuuksillesi. Ennen kun voit luoda myyntitilauksia kontakteillesi, sinun täytyy luoda kontaktista asiakas. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Etsi **Mahdollisuusluettelo**-ikkunasta mahdollisuus, jolle olet luonut myyntitarjouksen.
2. Valitse **Määritä myyntitarjous** -toiminto. Näyttöön tulee **Myyntitarjous**-ikkuna, jossa näkyy tähän mahdollisuuteen liittämäsi myyntitarjous.
3. Täytä lisäkentät ja valitse sitten **Tee tilaus** -toiminto.

Käsitellessäsi myyntien mahdollisuuksia sinulle ehkä tarvitsee luoda tarjous sille kontaktille, johon mahdollisuus on linkitetty.

## <a name="delete-opportunities"></a>Mahdollisuuksien poistaminen
Voit poistaa mahdollisuuksia esimerkiksi silloin, kun olet tehnyt sopimuksen. Voit kuitenkin poistaa vain suljettuja mahdollisuuksia. Suljetut mahdollisuudet voi poistaa kahdella eri tavalla. Voit poistaa yksittäisiä suljettuja mahdollisuuksia **Mahdollisuusluettelo**-ikkunassa tai voit suorittaa **Poista suljetut mahdollisuudet** -erätyön ja poistaa useita mahdollisuuksia määritettyjen ehtojen perusteella.

Voit poistaa suljetut mahdollisuudet **Mahdollisuusluettelo**-ikkunassa valitsemalla mahdollisuuden ja valitsemalla sitten **Poista**-toiminnon.

Voit poistaa suljetut mahdollisuudet **Poista suljetut mahdollisuudet** -eräajon avulla seuraavien vaiheiden avulla:

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Poista mahdollisuudet** ja valitse sitten liittyvä linkki.
2. Määritä **Mahdollisuus**-osassa suodattimet, jotka määrittävät poistettavat suljetut mahdollisuudet.
3. Valitse **OK**-painike.

Kun olet poistanut mahdollisuuden, ohjelma poistaa sen **Mahdollisuusluettelo**-ikkunasta.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Mahdollisuuden siirtäminen myyntisyklin vaiheiden läpi
Jos mahdollisuus seuraa myyntisykliä, voit siirtää sitä vaiheittain eteen- tai takaisinpäin eli seuraavaan tai edelliseen vaiheeseen. Voit jopa ohittaa vaiheita.

1. Valitse **Mahdollisuusluettelo**-ikkunassa **Päivitä**-toiminto. **Päivitä mahdollisuus** -ikkuna avautuu.
2. Siirrä mahdollisuus myyntisyklin vaiheiden läpi **Toiminnon tyyppi** -kentän avulla seuraavasti:
   * **Seuraava** siirtää mahdollisuutta yhdellä vaiheella eteenpäin.
   * **Ohita** siirtää mahdollisuutta eteenpäin yhdellä tai usealla vaiheella myyntisyklissä. Vaiheiden määrä määritetään **Esittely**-kentässä. Voit ohittaa vain vaiheita, jotka on määritetty niin, että ohittaminen on sallittua.
   * **Edellinen** siirtää mahdollisuutta yhdellä vaiheella taaksepäin.
   * **Hyppää** siirtää mahdollisuutta taaksepäin yhdellä tai usealla vaiheella myyntisyklissä. Vaiheiden määrä määritetään **Esittely**-kentässä.
   * **Päivitä**-kohdan avulla voi muuttaa tietoja (kuten muokata onnistumismahdollisuuksien arviota ja arvioituja arvoja) ilman toiseen vaiheeseen siirtymistä.
3. Täytä muut tarvittavat kentät ja valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Kontaktien luonti ja hallinta](marketing-contacts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

