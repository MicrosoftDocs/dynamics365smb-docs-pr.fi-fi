---
title: Pankkitilien täsmäyttäminen erikseen| Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten varastoarvo täsmäytetään pääkirjanpidon kanssa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69afda011e17a13eff747f8916e33c74c336bb82
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304202"
---
# <a name="reconcile-bank-accounts-separately"></a>Pankkitilien täsmäyttäminen erikseen
[!INCLUDE[d365fin](includes/d365fin_md.md)] -pankkitilien täsmäyttäminen pankista saatujen tiliotteiden kanssa: Aloita täyttämällä vasemmanpuoleisessa ruudussa **Pankkitilin täsmäytys** -sivu pankin tiliotteen tiedoilla, jotka sitten täsmäytät oikean puoleisen ruudun pankkitilitapahtumien kanssa. Älykäs tapa täyttää tiliotteen rivit on pankin tiliotteen tuonti tiedostona tai syötteenä.

> [!NOTE]  
> Pohjois-Amerikan versioissa, voit suorittaa tämän työn myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.

> [!TIP]  
> Voit täsmäyttää pankkitilit myös **Maksujen täsmäytyskirjauskansio** -sivulla. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee Bank Feeds -palvelu ja linkitä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

**Pankkitilin täsmäytys** -sivun rivit jaetaan kahteen ruutuun. **Pankin tiliotteen rivit** -ruudussa näkyvät joko tuodut pankkitapahtumat tai tapahtumat, joilla on avoimia maksuja. **Pankkitilitapahtumat**-ruudussa näkyvät pankkitilin tapahtumat.

Täsmäytettävien tapahtumien etsimistä ja kohdistamista kutsutaan *kohdistukseksi*. Voit suorittaa kohdistuksen automaattisesti **Kohdista automaattisesti** -toiminnon avulla. Vaihtoehtoisesti voit valita rivit manuaalisesti molemmissa ruuduissa linkittääksesi jokaisen tilioterivin yhteen tai useampaan pankkitilin kirjanpitotapahtumaan ja käyttää sitten **Kohdista manuaalisesti** -toimintoa. Jos rivi sisältää kohdistettavia tapahtumia, rivin **Kohdistettu**-valintaruutu valitaan.

Voit täyttää **Pankin tiliotteen rivit** -ruudun **Pankkitilin täsmäytys** -sivulla seuraavalla tavalla:

* Automaattisesti täyttämällä rivit **Tuo pankin tiliote** -toiminnolla pankin toimittamien toteutuneiden tiliotteiden perusteella.
* Manuaalisesti **Ehdota rivejä** -toiminnolla, kun haluat täyttää riveille niiden laskujen tapahtumien tiedot, joilla on avoimia maksuja.

Kun **Kokonaissaldo**-kentän arvo**Pankin tiliotteen rivit** -ruudussa on sama kuin **Täsmäytettävä saldo** -kentän arvo **Pankkitilitapahtumat**-ruudussa, voit täsmäyttää kohdistetun pankkitilin tapahtumat valitsemalla **Kirjaa**-toiminnon. Kaikki ei käytössä olevat pankkitilin kirjanpitomerkinnät säilyvät sivulla, tämä ilmaisee, että pankkitilille käsitellyt maksut eivät näy viimeisimmässä tiliotteessa, tai että eräät maksuista vastaanotettiin sekkeinä.

> [!NOTE]  
>   Jos pankin tiliotteen rivit liittyvät sekkitapahtumiin, et voi käyttää kohdistustoimintoja. Sen sijaan sinun on valittava **Kohdista tapahtumat** -toiminto ja valittava sitten asianmukainen sekkitapahtuma, jota kohdistetaan pankin tiliotteen riviin.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pankin täsmäytysrivien täyttäminen tiliotteen tuomisen avulla
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytys** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Pankkitilin nro** -kentässä asianmukainen pankkitilin koodi. Pankkitilillä olevat tapahtumat näkyvät **Pankkitilitapahtumat**-ruudussa.
4. Syötä **Tiliotteen pvm** -kenttään pankin tiliotteen päivämäärä.
5. Syötä **Tiliotteen loppusaldo** -kenttään pankin tiliotteen saldo.
6. Jos sinulla on tiliotetiedosto, valitse **Tuo pankin tiliote** -toiminto.
7. Etsi tiedosto ja valitse sitten **Avaa**-painike tuodaksesi pankkitapahtumat **Pankkitilin täsmäytys** -sivun riveihin.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pankin täsmäytyksen rivien täyttäminen Ehdota rivejä -toiminnon avulla
1. Valitse **Pankkitilin täsmäytys** -sivulla **Ehdota rivejä** -toiminto.
2. Syötä **Aloituspvm**-kenttään ensimmäinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
3. Syötä **Lopetuspvm**-kenttään viimeinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
4. Valitse **Sisällytä sekit** -valintaruutu, kun haluat ehdottaa sekkitapahtumia vastaavien pankkitilitapahtumien sijaan.
5. Valitse **OK**-painike.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen automaattisesti
Sivu tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (vasemmassa ruudussa) olevan tekstin vastaavuuden perusteella verrattuna yhden tai useamman pankkitilitapahtuman (oikealla puolella) tekstiin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisätietoja on seuraavassa toimenpiteessä.

1. Valitse **Pankkitilin täsmäytys** -sivulla **Kohdista automaattisesti**. **Kohdista pankkitapahtumat** -sivu avautuu.
2. Määritä **Tapahtuman päivämäärätoleranssi (päivinä)** -kenttään ajanjakso ennen ja jälkeen pankkitilitapahtuman kirjauspäivämäärän, jonka aikana toiminto hakee vastaavia tapahtumapäivämääriä tiliotteesta.

    Jos kirjoitat arvon 0 tai jätät kentän tyhjäksi, **Kohdista automaattisesti** -toiminto etsii vain vastaavat tapahtumapäivämäärät pankkitilin kirjanpitotapahtuman kirjauspäivänä.
3. Valitse **OK**-painike.

    Kaikkien pankin tiliotteen rivien ja täsmäytettävissä olevien pankkitilitapahtumien kirjasin muuttuu vihreäksi, ja **Kohdistettu**-valintaruutu on valittuna.
4. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen manuaalisesti
1. Valitse **Pankkitilin täsmäytys** -sivun **Pankin tiliotteen rivit** -ruudussa kohdistamaton rivi.
2. Valitse **Pankkitilitapahtumat** -ruudussa yksi tai useampia pankkitilitapahtumia, joihin voidaan kohdistaa valitun pankin tiliotteen rivi. Voit valita useita rivejä pitämällä Ctrl-näppäimen painettuna.
3. Valitse **Kohdista manuaalisesti** -toiminto.

    Valitun pankin tiliotteen rivin ja valittujen pankkitilitapahtumien fontti muuttuu vihreäksi, ja oikeanpuoleisen ruudun **Kohdistettu**-valintaruutu on valittuna.
4. Toista vaiheet 1–3 kaikille pankin tiliotteen riveille, joita ei ole kohdistettu.
5. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Puuttuvien tapahtumien luominen ja kohdistaminen pankkitapahtumiin
Joskus pankin tiliotteessa on koron tai veloitetun maksun summia. Tällaisia pankkitapahtumia ei voi kohdistaa, koska niillä ei ole vastaavia tapahtumia [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tällöin jokaiselle tapahtumalle on kirjattava päiväkirjarivi. Näin luodaan liittyvä tapahtuma, johon kohdistus voidaan tehdä.

1. Valitse **Pankkitilin täsmäytys** -sivulla **Siirrä yleiseen päiväkirjaan** -toiminto.  
2. Määritä käytettävä yleinen päiväkirja **Siirrä p-til. täsm. yl. pvk:aan** -sivulla ja valitse sitten **OK**.

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää kaikkien puuttuvia tapahtumia sisältävien tiliotteiden päiväkirjarivit.
3. Syötä päiväkirjariville tarvittavat tiedot, kuten vastatili. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  
4. Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla **Testiraportti** -toiminto. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Pankkitilin täsmäytys** -sivun otsikot.
4. Valitse **Kirjaa**-toiminto.

    Kun tapahtuma on kirjattu, voit jatkaa pankkitapahtuman kohdistukseen.
5. Päivitä tai avaa **Pankkitilin täsmäytys** -sivu. Uusi tapahtuma näkyy **Pankkitilitapahtumat**-ruudussa.
6. Kohdista tiliotteen rivi pankkitilitapahtumaan manuaalisesti tai automaattisesti.

## <a name="see-also"></a>Katso myös
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
