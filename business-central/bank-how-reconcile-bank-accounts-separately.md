---
title: Pankkitilien täsmäyttäminen| Microsoft Docs
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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e53c1f7b0b2af4a94579863197ec7348c9b6ff18
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186306"
---
# <a name="reconcile-bank-accounts"></a>Pankkitilien täsmäytys
Pankkitilin täsmäytyksen avulla voit varmistaa, että yrityksesi eri liiketoimintatapahtumat ja kulut näkyvät oikein yrityksen kirjoissa. Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä. Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.

Seuraavassa kuvataan, miten pankkitilin täsmäytys suoritetaan **Pankkitilin täsmäytys** -sivulla.

> [!TIP]
> Voit myös täsmäyttää maksukäsittelyyn liittyviä pankkitilejä **Maksujen täsmäytyskirjauskansio** -sivulla maksujen käsittelyyn liittyen. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Pohjois-Amerikan versioissa, voit suorittaa tämän työn myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen "Pankkitilien täsmäyttäminen" -kohdasta.

**Pankkitilin täsmäytys** -sivun rivit jaetaan kahteen ruutuun. **Pankin tiliotteen rivit** -ruudussa näkyvät joko tuodut pankkitapahtumat tai tapahtumat, joilla on avoimia maksuja. **Pankkitilitapahtumat**-ruudussa näkyvät sisäisen pankkitilin tapahtumat.

Pankkitapahtumien täsmäytystä sisäisten pankkitapahtumien kanssa kutsutaan *kohdistukseksi*. Voit suorittaa kohdistuksen automaattisesti **Kohdista automaattisesti** -toiminnon avulla. Vaihtoehtoisesti voit valita rivit manuaalisesti molemmissa ruuduissa linkittääksesi jokaisen tilioterivin yhteen tai useampaan pankkitilin kirjanpitotapahtumaan ja käyttää sitten **Kohdista manuaalisesti** -toimintoa. Jos rivi sisältää kohdistettavia tapahtumia, rivin **Kohdistettu**-valintaruutu valitaan. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Jos pankin tiliotteen rivit liittyvät sekkitapahtumiin, et voi käyttää kohdistustoimintoja. Sen sijaan sinun on valittava **Kohdista tapahtumat** -toiminto ja valittava sitten asianmukainen sekkitapahtuma, jota kohdistetaan pankin tiliotteen riviin.

Kun **Kokonaissaldo**-kentän arvo**Pankin tiliotteen rivit** -ruudussa on sama kuin **Täsmäytettävä saldo** -kentän arvo **Pankkitilitapahtumat**-ruudussa, voit valita **Kirjaa**-toiminnon. Täsmäyttämättömät pankkitilitapahtumat säilyvät sivulla, ja osoittavat eroa, joka tulee ratkaista pankkitilin täsmäyttämiseksi.

Kaikki rivit, joita ei voi kohdentaa, ilmaistuina arvoina **Erotus**-kentässä, pysyvät **Pankkitilin täsmäytys** -sivulla kirjauksen jälkeen. Ne edustavat eroa, joka sinun on ratkaistava, ennen kuin voit suorittaa pankkitilin täsmäytyksen. Tyypilliset liiketoimintatilanteet, jotka voivat aiheuttaa eroja:

|Ero|Syy|Ratkaisu|
|-|-|
|Sisäisen pankkitilin tapahtuma ei ole pankin tiliotteessa.|Pankkitapahtumaa ei tapahtunut, vaikka kirjaus tehtiin kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)].|Tee puuttuva rahatapahtuma (tai pyydä velkojaa tekemään se) ja tuo sitten tiliotetiedosto uudelleen tai syötä tapahtuma manuaalisesti.|
|Pankin tiliotteen tapahtumaa ei ole asiakirjana tai kirjauskansion rivinä järjestelmässä [!INCLUDE[d365fin](includes/d365fin_md.md)].|Pankkitapahtuma tehtiin ilman vastaavaa kirjausta kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)], esimerkiksi kulun kirjauskansiorivin kirjausta varten.|Luo ja kirjaa puuttuva tapahtuma. Lisätietoja nopeasta tavasta tämän aloittamiseksi on aiheessa [Puuttuvien tapahtumien luominen pankkitapahtumien kohdistamiseksi.](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with) kanssa.|
|Sisäisen pankkitilin tapahtuma vastaa pankkitapahtumaa, mutta jotkin tiedot ovat liian erilaisia, jotta ne antaisivat vastaavuuden.|Tiedot, kuten summa tai asiakkaan nimi, on syötetty eri tavalla pankkitapahtuman tai sisäisen kirjauksen yhteydessä.|Tarkista tiedot ja kohdenna nämä kaksi manuaalisesti. Vaihtoehtoisesti voit korjata tietojen ristiriidan.||

Erot on ratkaistava esimerkiksi luomalla puuttuvia merkintöjä ja korjaamalla ei-vastaavia tietoja tai tekemällä puuttuvia rahatapahtumia, kunnes pankkitilin täsmäytys on suoritettu ja kirjattu.

Voit täyttää **Pankin tiliotteen rivit** -ruudun **Pankkitilin täsmäytys** -sivulla seuraavalla tavalla:

* Automaattisesti käyttämällä **Tuo pankin tiliote** -toimintoa täyttämään **Pankin tiliotteen rivit** -ruutu pankkitapahtumilla tuodun tiedoston tai pankin tarjoaman tietovirran mukaisesti.
* Manuaalisesti **Ehdota rivejä** -toiminnolla täyttämään **Pankin tiliotteen rivit** -ruutu niiden kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)] olevien laskujen mukaisesti, joilla on maksamattomia maksuja.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pankin täsmäytysrivien täyttäminen tiliotteen tuomisen avulla
**Pankin tiliotteen rivit** -ruutu täytetään pankkitapahtumilla tuodun tiedoston tai pankin antaman tietovirran mukaan.

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee Bank Feeds -palvelu ja linkitä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Pankkitilin täsmäytys** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Pankkitilin nro** -kentässä asianmukainen pankkitilin koodi. Pankkitilillä olevat tapahtumat näkyvät **Pankkitilitapahtumat**-ruudussa.
4. Syötä **Tiliotteen pvm** -kenttään pankin tiliotteen päivämäärä.
5. Syötä **Tiliotteen loppusaldo** -kenttään pankin tiliotteen saldo.
6. Jos sinulla on tiliotetiedosto, valitse **Tuo pankin tiliote** -toiminto.
7. Etsi tiedosto ja valitse sitten **Avaa**-painike tuodaksesi pankkitilin tapahtumat **Pankin tiliotteen rivit** -ruutuun **Pankkitilin täsmäytys** -sivulla.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pankin täsmäytyksen rivien täyttäminen Ehdota rivejä -toiminnon avulla
**Pankin tiliotteen rivit** -ruutu täytetään niiden, kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)] olevien laskujen mukaan, joissa on maksamattomia maksuja.  
1. Valitse **Pankkitilin täsmäytys** -sivulla **Ehdota rivejä** -toiminto.
2. Syötä **Aloituspvm**-kenttään ensimmäinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
3. Syötä **Lopetuspvm**-kenttään viimeinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
4. Valitse **Sisällytä sekit** -valintaruutu, kun haluat ehdottaa sekkitapahtumia vastaavien pankkitilitapahtumien sijaan.
5. Valitse **OK**-painike.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen automaattisesti
Sivu **Pankkitilin täsmäytys** tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (vasemmassa ruudussa) olevan tekstin vastaavuuden perusteella verrattuna yhden tai useamman pankkitilitapahtuman (oikealla puolella) tekstiin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisäohjeita on kohdassa [Pankin tiliotteen rivien ja pankkitilin tapahtumien kohdistaminen manuaalisesti](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

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

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Puuttuvien tapahtumien luominen ja kohdistaminen pankin tiliotteen riveihin
Joskus pankin tiliotteessa on koron tai veloitetun maksun summia. Tällaisia tiliotteen rivejä ei voi kohdistaa, koska niillä ei ole vastaavia tapahtumia kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tällöin jokaiselle tapahtumalle on kirjattava päiväkirjarivi. Näin luodaan liittyvä tapahtuma, johon kohdistus voidaan tehdä.

1. Valitse **Pankkitilin täsmäytys** -sivulla **Siirrä yleiseen päiväkirjaan** -toiminto.  
2. Määritä käytettävä yleinen päiväkirja **Siirrä p-til. täsm. yl. pvk:aan** -sivulla ja valitse sitten **OK**.

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää kaikkien puuttuvia tapahtumia sisältävien tiliotteiden päiväkirjarivit.
3. Syötä päiväkirjariville tarvittavat tiedot, kuten vastatili. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  
4. Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla **Testiraportti** -toiminto. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Pankkitilin täsmäytys** -sivun otsikot.
4. Valitse **Kirjaa**-toiminto.

    Kun tapahtuma on kirjattu, voit jatkaa tiliotteen rivin kohdistukseen.
5. Päivitä tai avaa **Pankkitilin täsmäytys** -sivu. Uusi tapahtuma näkyy **Pankkitilitapahtumat**-ruudussa.
6. Kohdista tiliotteen rivi pankkitilitapahtumaan manuaalisesti tai automaattisesti.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Automaattinen maksujen soveltamisen sääntöjen määrittäminen](receivables-how-set-up-payment-application-rules.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
