---
title: "Toimintaohje: Pankkitilien täsmäyttäminen erikseen| Microsoft Docs"
description: "Toimintaohje: Pankkitilien täsmäyttäminen erikseen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 916f655f9dba80f7c227519372633913b11641ea
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-bank-accounts-separately"></a>Toimintaohje: Pankkitilien täsmäyttäminen erikseen
Jos haluat täsmäyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilit pankista saatujen tiliotteiden kanssa, sinun on ensin täytettävä **Pankkitilin täsmäytys** -ikkunan rivit.

**Huomautus**: Voit täsmäyttää pankkitilit myös **Maksujen täsmäytyskirjauskansio** -ikkunassa. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee -pankkisyötepalvelu ja linkitä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).

**Pankkitilin täsmäytys** -ikkunan rivit jaetaan kahteen ruutuun. **Pankin tiliotteen rivit** -ruudussa näkyvät joko tuodut pankkitapahtumat tai tapahtumat, joilla on avoimia maksuja. **Pankkitilitapahtumat**-ruudussa näkyvät pankkitilin tapahtumat.

Täsmäytettävien tapahtumien etsimistä ja kohdistamista kutsutaan *kohdistukseksi*. Voit suorittaa kohdistuksen automaattisesti **Kohdista automaattisesti** -toiminnon avulla. Vaihtoehtoisesti voit valita rivit manuaalisesti molemmissa ruuduissa linkittääksesi jokaisen tilioterivin yhteen tai useampaan pankkitilin kirjanpitotapahtumaan ja käyttää sitten **Kohdista manuaalisesti** -toimintoa. Jos rivi sisältää kohdistettavia tapahtumia, rivin **Kohdistettu**-valintaruutu valitaan.

Voit täyttää **Pankin tiliotteen rivit** -ruudun **Pankkitilin täsmäytys** -ikkunassa seuraavalla tavalla:

* Automaattisesti täyttämällä rivit **Tuo pankin tiliote** -toiminnolla pankin toimittamien toteutuneiden tiliotteiden perusteella.
* Manuaalisesti **Ehdota rivejä** -toiminnolla, kun haluat täyttää riveille niiden laskujen tapahtumien tiedot, joilla on avoimia maksuja.

Kun **Kokonaissaldo**-kentän arvo**Pankin tiliotteen rivit** -ruudussa on sama kuin **Täsmäytettävä saldo** -kentän arvo **Pankkitilitapahtumat**-ruudussa, voit täsmäyttää kohdistetun pankkitilin tapahtumat valitsemalla **Kirjaa**-toiminnon. Kaikki ei käytössä olevat pankkitilin kirjanpitomerkinnät säilyvät ikkunassa, tämä ilmaisee, että pankkitilille käsitellyt maksut eivät näy viimeisimmässä tiliotteessa, tai että eräät maksuista vastaanotettiin sekkeinä.

**Huomautus**: Jos pankin tiliotteen rivit liittyvät sekkitapahtumiin, et voi käyttää kohdistustoimintoja. Sen sijaan sinun on valittava **Kohdista tapahtumat** -toiminto ja valittava sitten asianmukainen sekkitapahtuma, jota kohdistetaan pankin tiliotteen riviin.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pankin täsmäytysrivien täyttäminen tiliotteen tuomisen avulla
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilin täsmäytys** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Pankkitilin nro** -kentässä vastaava pankkitili. Pankkitilillä olevat tapahtumat näkyvät **Pankkitilitapahtumat**-ruudussa.
4. Syötä **Tiliotteen pvm** -kenttään pankin tiliotteen päivämäärä.
5. Syötä **Tiliotteen loppusaldo** -kenttään pankin tiliotteen saldo.
6. Jos sinulla on tiliotetiedosto, valitse **Tuo pankin tiliote** -toiminto.
7. Etsi tiedosto ja valitse sitten **Avaa**-painike tuodaksesi pankkitapahtumat **Pankkitilin täsmäytys** -ikkunan riveihin.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pankin täsmäytyksen rivien täyttäminen Ehdota rivejä -toiminnon avulla
1. Valitse **Pankkitilin täsmäytys** -ikkunassa **Ehdota rivejä** -toiminto.
2. Syötä **Aloituspvm**-kenttään ensimmäinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
3. Syötä **Lopetuspvm**-kenttään viimeinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
4. Valitse **Sisällytä sekit** -valintaruutu, kun haluat ehdottaa sekkitapahtumia vastaavien pankkitilitapahtumien sijaan.
5. Valitse **OK**-painike.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen automaattisesti
1. Valitse **Pankkitilin täsmäytys** -ikkunassa **Kohdista automaattisesti**. **Kohdista pankkitapahtumat** -ikkuna avautuu.
2. Määritä **Tapahtuman päivämäärätoleranssi (päivinä)** -kenttään ajanjakso ennen ja jälkeen pankkitilitapahtuman kirjauspäivämäärän, jonka aikana toiminto hakee vastaavia tapahtumapäivämääriä tiliotteesta.

    Jos kirjoitat arvon 0 tai jätät kentän tyhjäksi, **Kohdista automaattisesti** -toiminto etsii vain vastaavat tapahtumapäivämäärät pankkitilin kirjanpitotapahtuman kirjauspäivänä.  
3. Valitse **OK**-painike.  

    Kaikkien pankin tiliotteen rivien ja täsmäytettävissä olevien pankkitilitapahtumien kirjasin muuttuu vihreäksi, ja **Kohdistettu**-valintaruutu on valittuna.
4. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen manuaalisesti
1. Valitse **Pankkitilin täsmäytys** -ikkunan **Pankin tiliotteen rivit** -ruudussa kohdistamaton rivi.
2. Valitse **Pankkitilitapahtumat** -ruudussa yksi tai useampia pankkitilitapahtumia, joihin voidaan kohdistaa valitun pankin tiliotteen rivi. Voit valita useita rivejä pitämällä Ctrl-näppäimen painettuna.  
3. Valitse **Kohdista manuaalisesti** -toiminto.

    Valitun pankin tiliotteen rivin ja valittujen pankkitilitapahtumien fontti muuttuu vihreäksi, ja oikeanpuoleisen ruudun **Kohdistettu**-valintaruutu on valittuna.
4. Toista vaiheet 1–3 kaikille pankin tiliotteen riveille, joita ei ole kohdistettu.
5. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Puuttuvien tapahtumien luominen ja kohdistaminen pankkitapahtumiin
Joskus pankin tiliotteessa on koron tai veloitetun maksun summia. Tällaisia pankkitapahtumia ei voi kohdistaa, koska niillä ei ole vastaavia tapahtumia [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tällöin jokaiselle tapahtumalle on kirjattava päiväkirjarivi. Näin luodaan liittyvä tapahtuma, johon kohdistus voidaan tehdä.

1. Valitse **Pankkitilin täsmäytys** -ikkunassa **Siirrä yleiseen päiväkirjaan** -toiminto.  
2. Määritä **Siirrä p-til. täsm. yl. pvk:aan** -ikkunassa käytettävä yleinen päiväkirja. Valitse sitten **OK**-painike.

    **Yleinen päiväkirja** -ikkuna avautuu. Se sisältää kaikkien puuttuvia tapahtumia sisältävien tiliotteiden päiväkirjarivit.
3. Syötä päiväkirjariville tarvittavat tiedot, kuten vastatili. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
4. Valitse **Kirjaa**-toiminto.

    Kun tapahtuma on kirjattu, voit jatkaa pankkitapahtuman kohdistukseen.
5. Päivitä tai avaa **Pankkitilin täsmäytys** -ikkuna. Uusi tapahtuma näkyy **Pankkitilitapahtumat**-ruudussa.
6. Kohdista tiliotteen rivi pankkitilitapahtumaan manuaalisesti tai automaattisesti.

## <a name="see-also"></a>Katso myös
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

