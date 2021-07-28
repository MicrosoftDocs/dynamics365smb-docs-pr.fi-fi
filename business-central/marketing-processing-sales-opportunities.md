---
title: Myyntisyklien myyntimahdollisuuksien käsitteleminen
description: Tässä aiheessa kuvataan erilaisia tapoja käsitellä myyntimahdollisuuksia myyntisykleissä ja siirtää mahdollisuutta myyntisyklin vaiheissa.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/22/2021
ms.author: jswymer
ms.openlocfilehash: d67e1d1eda6cf3ae80ebad185a0db3fadd3eec1b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437600"
---
# <a name="process-sales-opportunities"></a>Myyntimahdollisuuksien käsitteleminen
Mahdollisuuden luomisen jälkeen sen hallinnassa ja valmistumisprosessissa voidaan käyttää useita toimintoja.

## <a name="to-view-opportunities"></a>Mahdollisuuksien tarkasteleminen
Olemassa olevat myyntimahdollisuudet ovat käytettävissä **Mahdollisuusluettelo**-sivulla. Tätä sivua voidaan käyttää seuraavilla tavoilla myyntimahdollisuuksien käsittelemisessä:

| Mahdollisuuksien tarkasteminen | Sitten |
| --- | --- |
| Kaikki myyjät ja kontaktit |Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mahdollisuusluettelo** ja valitse sitten vastaava linkki. |
| Määritetty myyjä |Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyjät** ja valitse sitten vastaava linkki. Valitse myyjä, valitse sitten **Mahdollisuudet**-toiminto. Valitse tämän jälkeen **Luettelo**-toiminto. |
| Määritetty kontakti |Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten vastaava linkki. Valitse kontakti luettelosta ja valitse sitten **Mahdollisuudet**-toiminto. |

Jokainen näistä tehtävistä avaa **Mahdollisuusluettelo**-sivun.

## <a name="to-close-opportunities"></a>Mahdollisuuksien sulkeminen
Voit sulkea mahdollisuuden, kun neuvottelut ovat ohi. Mahdollisuuden sulkemisen yhteydessä voit määrittää, onko se voitettu vai menetetty ja sulkemisen syyt. Syyn määrittäminen edellyttää suljettujen mahdollisuuksien koodien määrittämistä.

1. Valitse **Mahdollisuusluettelo**-sivulla mahdollisuus ja valitse sitten **Sulje**-toiminto. **Sulje mahdollisuus** -sivu avautuu.
2. Täytä tarvittavat kentät ja valitse **OK**-painike.

   **Sulje mahdollisuuden koodi** - ja **Pvm suljettu** -kentät ovat pakollisia. Ne on täytettävä, ennen kun voi valita **OK**-painikkeen.

   Valitse **Sulje mahdollisuuden koodi** -kentässä jokin olemassa olevista suljettujen mahdollisuuksien koodeista tai lisää uusi koodi. Voit lisätä uuden koodin valitsemalla avattavasta luettelosta **Valitse koko luettelosta** ja valitsemalla sitten **Uusi**. Täytä tyhjän rivin **Koodi**-, **Tyyppi**- ja **Kuvaus**-kenttä ja valitse sitten **OK**-painike.

## <a name="to-create-quotes-for-opportunities"></a>Tarjousten luominen mahdollisuuksille
> [!NOTE]
> Voit luoda myyntitarjouksia vain mahdollisuuksista, joiden yhteyshenkilön tyyppi on Yritys.

1. Valitse **Mahdollisuusluettelo**-sivulla mahdollisuus ja valitse sitten **Määritä myyntitarjous** -toiminto. **Myyntitarjous**-sivu aukeaa.
2. Täytä asianmukaiset kentät.

## <a name="to-create-sales-orders-for-opportunities"></a>Mahdollisuuksien myyntitilausten luominen
Voit tehdä myyntitilauksia niistä myyntitarjouksista, jotka olet luonut mahdollisuuksillesi. Ennen kun voit luoda myyntitilauksia kontakteillesi, sinun täytyy luoda kontaktista asiakas. Lisätietoja on kohdassa [Kontaktien luominen](marketing-create-contact-companies.md).

1. Etsi **Mahdollisuusluettelo**-sivulla mahdollisuus, jolle olet luonut myyntitarjouksen.
2. Valitse **Määritä myyntitarjous** -toiminto. Näyttöön tulee **Myyntitarjous**-sivu, jossa näkyy tähän mahdollisuuteen liittämäsi myyntitarjous.
3. Täytä lisäkentät ja valitse sitten **Tee tilaus** -toiminto.

Käsitellessäsi myyntien mahdollisuuksia sinulle ehkä tarvitsee luoda tarjous sille kontaktille, johon mahdollisuus on linkitetty.

## <a name="to-delete-opportunities"></a>Mahdollisuuksien poistaminen
Voit poistaa mahdollisuuksia esimerkiksi silloin, kun olet tehnyt sopimuksen. Voit kuitenkin poistaa vain suljettuja mahdollisuuksia. Suljetut mahdollisuudet voi poistaa kahdella eri tavalla. Voit poistaa yksittäisiä suljettuja mahdollisuuksia **Mahdollisuusluettelo**-sivulla tai voit suorittaa **Poista suljetut mahdollisuudet** -erätyön ja poistaa useita mahdollisuuksia määritettyjen ehtojen perusteella.

Voit poistaa suljetut mahdollisuudet **Mahdollisuusluettelo**-sivulla valitsemalla mahdollisuuden ja valitsemalla sitten **Poista**-toiminnon.

Voit poistaa suljetut mahdollisuudet **Poista suljetut mahdollisuudet** -eräajon avulla seuraavien vaiheiden avulla:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Poista mahdollisuudet** ja valitse sitten vastaava linkki.
2. Määritä **Mahdollisuus**-osassa suodattimet, jotka määrittävät poistettavat suljetut mahdollisuudet.
3. Valitse **OK**-painike.

Kun olet poistanut mahdollisuuden, ohjelma poistaa sen **Mahdollisuusluettelo**-sivulta.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Mahdollisuuden siirtäminen myyntisyklin vaiheiden läpi
Jos mahdollisuus seuraa myyntisykliä, voit siirtää sitä vaiheittain eteen- tai takaisinpäin eli seuraavaan tai edelliseen vaiheeseen. Voit jopa ohittaa vaiheita.

1. Valitse **Mahdollisuusluettelo**-sivulla **Päivitä**-toiminto. **Päivitä mahdollisuus** -ikkuna avautuu.
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
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]