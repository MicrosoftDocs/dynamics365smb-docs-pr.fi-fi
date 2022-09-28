---
title: Pankkitilien täsmäytys
description: Tässä ohjeaiheessa kuvataan, miten voit täsmäyttää sisäisten pankkitiliesi kauppatapahtumat pankin tiliotteiden kanssa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.search.form: 379, 388, 389, 1290, 1692, 10124
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: d12ac9b5aa8718c2445cd7a4054ff0549e5d8ada
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534937"
---
# <a name="reconcile-bank-accounts"></a>Pankkitilien täsmäytys

Pankkitilin täsmäytyksen avulla voit varmistaa, että yrityksesi eri liiketoimintatapahtumat ja kulut näkyvät oikein yrityksen kirjoissa. Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä. Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.

Seuraavassa kuvataan, miten pankkitilin täsmäytys suoritetaan **Pankkitilin täsmäytys** -sivulla.

> [!TIP]
> Voit myös täsmäyttää pankkitilejä **Maksujen täsmäytyskirjauskansio** -sivulla, kun käsittelet maksuja. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä täsmäyttää automaattisesti pankkitilin päiväkirjaan kirjattaville maksuille. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Pohjois-Amerikan versioissa tämän työn voi suorittaa myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille mutta ei sisällä pankin tiliotetiedostojen tuontia. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja on kohdan [Pankkitilien täsmäyttäminen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) Yhdysvaltain paikallisissa toimintoja käsittelevässä osassa.

**Pankkitilin täsmäytys** -sivun rivit jaetaan kahteen ruutuun. **Pankin tiliotteen rivit** -ruudussa näkyvät joko tuodut pankkitapahtumat tai tapahtumat, joilla on avoimia maksuja. **Pankkitilitapahtumat**-ruudussa näkyvät sisäisen pankkitilin tapahtumat.

Pankkitapahtumien täsmäytystä sisäisten pankkitapahtumien kanssa kutsutaan *kohdistukseksi*. Voit suorittaa kohdistuksen automaattisesti **Kohdista automaattisesti** -toiminnon avulla. Vaihtoehtoisesti voit valita rivit manuaalisesti molemmissa ruuduissa linkittääksesi jokaisen tilioterivin yhteen tai useampaan pankkitilin kirjanpitotapahtumaan ja käyttää sitten **Kohdista manuaalisesti** -toimintoa. Jos rivi sisältää kohdistettavia tapahtumia, rivin **Kohdistettu**-valintaruutu valitaan. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Jos pankin tiliotteen rivit liittyvät sekkitapahtumiin, et voi käyttää kohdistustoimintoja. Sen sijaan sinun on valittava **Kohdista tapahtumat** -toiminto ja valittava sitten asianmukainen sekkitapahtuma, jota kohdistetaan pankin tiliotteen riviin.

Kun **Tiliotteen rivit** -ruudun **Kokonaissaldo**-kentän arvo on yhtä suuri kuin **Täsmäytettävä saldo** -kentän ja **Tilin reskontrakirjaukset** -ruudun **Viimeinen saldo** -kentän kokonaisarvo, voit valita **Kirjaa**-toiminnon. Täsmäyttämättömät pankkitilitapahtumat säilyvät sivulla, ja osoittavat eroa, joka tulee ratkaista pankkitilin täsmäyttämiseksi.

Kaikki rivit, joita ei voi kohdentaa, ilmaistuina arvoina **Erotus**-kentässä, pysyvät **Pankkitilin täsmäytys** -sivulla kirjauksen jälkeen. Ne edustavat eroa, joka sinun on ratkaistava, ennen kuin voit suorittaa pankkitilin täsmäytyksen. Tyypilliset liiketoimintatilanteet, jotka voivat aiheuttaa eroja:

| Ero | Syy | Ratkaisu |
|------------|--------|------------|
| Sisäisen pankkitilin tapahtuma ei ole pankin tiliotteessa. | Pankkitapahtumaa ei tapahtunut, vaikka kirjaus tehtiin kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. | Tee puuttuva rahatapahtuma (tai pyydä velkojaa tekemään se) ja tuo sitten tiliotetiedosto uudelleen tai syötä tapahtuma manuaalisesti. |
| Pankin tiliotteen tapahtumaa ei ole asiakirjana tai kirjauskansion rivinä järjestelmässä [!INCLUDE[prod_short](includes/prod_short.md)]. | Pankkitapahtuma tehtiin ilman vastaavaa kirjausta kohteessa [!INCLUDE[prod_short](includes/prod_short.md)], esimerkiksi kulun kirjauskansiorivin kirjausta varten. | Luo ja kirjaa puuttuva tapahtuma. Lisätietoja nopeasta tavasta tämän aloittamiseksi on aiheessa [Puuttuvien tapahtumien luominen pankkitapahtumien kohdistamiseksi.](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with) kanssa. |
| Sisäisen pankkitilin tapahtuma vastaa pankkitapahtumaa, mutta jotkin tiedot ovat liian erilaisia, jotta ne antaisivat vastaavuuden. | Tiedot, kuten summa tai asiakkaan nimi, on syötetty eri tavalla pankkitapahtuman tai sisäisen kirjauksen yhteydessä. | Tarkista tiedot ja kohdenna nämä kaksi manuaalisesti. Vaihtoehtoisesti voit korjata tietojen ristiriidan. |

Erot on ratkaistava esimerkiksi luomalla puuttuvia merkintöjä ja korjaamalla ei-vastaavia tietoja tai tekemällä puuttuvia rahatapahtumia, kunnes pankkitilin täsmäytys on suoritettu ja kirjattu.

Voit täyttää **Pankin tiliotteen rivit** -ruudun **Pankkitilin täsmäytys** -sivulla seuraavalla tavalla:

* Automaattisesti käyttämällä **Tuo pankin tiliote** -toimintoa täyttämään **Pankin tiliotteen rivit** -ruutu pankkitapahtumilla tuodun tiedoston tai pankin tarjoaman tietovirran mukaisesti.
* Manuaalisesti **Ehdota rivejä** -toiminnolla täyttämään **Pankin tiliotteen rivit** -ruutu niiden kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] olevien laskujen mukaisesti, joilla on maksamattomia maksuja.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pankin täsmäytysrivien täyttäminen tiliotteen tuomisen avulla

**Pankin tiliotteen rivit** -ruutu täytetään pankkitapahtumilla tuodun tiedoston tai pankin antaman tietovirran mukaan.

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee Bank Feeds -palvelu ja linkitä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Tiliotetiedostoja voi tuoda myös pilkuin tai puolipistein erotellussa muodossa (.CSV). Tiliotteen tuontimuodot voidaan määrittää ja muoto liittää pankkitiliin käyttämällä asetusten ohjattua määritystä **Määritä tiliotetiedoston tuontimuoto**. Näitä muotoja voi sitten käyttää, kun tiliotteita tuodaan **Pankkitilin täsmäytys** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytys** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Pankkitilin nro** -kentässä asianmukainen pankkitilin koodi. Pankkitilillä olevat tapahtumat näkyvät **Pankkitilitapahtumat**-ruudussa.
4. Syötä **Tiliotteen pvm** -kenttään pankin tiliotteen päivämäärä.
5. Syötä **Tiliotteen loppusaldo** -kenttään pankin tiliotteen saldo.
6. Jos sinulla on tiliotetiedosto, valitse **Tuo pankin tiliote** -toiminto.
7. Etsi tiedosto ja valitse sitten **Avaa**-painike tuodaksesi pankkitilin tapahtumat **Pankin tiliotteen rivit** -ruutuun **Pankkitilin täsmäytys** -sivulla.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pankin täsmäytyksen rivien täyttäminen Ehdota rivejä -toiminnon avulla

**Pankin tiliotteen rivit** -ruutu täytetään niiden, kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] olevien laskujen mukaan, joissa on maksamattomia maksuja.  

1. Valitse **Pankkitilin täsmäytys** -sivulla **Ehdota rivejä** -toiminto.
2. Syötä **Aloituspvm**-kenttään ensimmäinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
3. Syötä **Lopetuspvm**-kenttään viimeinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.

> [!NOTE]
> Yleensä lopetuspvm on sama kuin **Tiliotteen pvm** -kentässä määritetty päivämäärä. Jos kuitenkin haluat täsmäyttää transaktiot vain jakson osaa varten, voit syöttää eri lopetuspäivämäärän. 

1. Valitse **Sisällytä sekit** -valintaruutu, kun haluat ehdottaa sekkitapahtumia vastaavien pankkitilitapahtumien sijaan.
1. Valitse **OK**-painike.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen automaattisesti

Sivu **Pankkitilin täsmäytys** tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (vasemmassa ruudussa) olevan tekstin vastaavuuden perusteella verrattuna yhden tai useamman pankkitilitapahtuman (oikealla puolella) tekstiin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisäohjeita on kohdassa [Pankin tiliotteen rivien ja pankkitilin tapahtumien kohdistaminen manuaalisesti](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Voit tutkia vastaavuuksien perusteita käyttämällä **Vastaavuuden tiedot** -toimintoa. Tiedot sisältävät esimerkiksi niiden kenttien nimet, jotka sisälsivät vastaavat arvot.  

1. Valitse **Pankkitilin täsmäytys** -sivulla **Kohdista automaattisesti**. **Kohdista pankkitapahtumat** -sivu avautuu.
2. Määritä **Tapahtuman päivämäärätoleranssi (päivinä)** -kenttään ajanjakso ennen ja jälkeen pankkitilitapahtuman kirjauspäivämäärän, jonka aikana toiminto hakee vastaavia tapahtumapäivämääriä tiliotteesta.

    Jos kirjoitat arvon 0 tai jätät kentän tyhjäksi, **Kohdista automaattisesti** -toiminto etsii vain vastaavat tapahtumapäivämäärät pankkitilin kirjanpitotapahtuman kirjauspäivänä.
3. Valitse **OK**-painike.

    Kaikkien pankin tiliotteen rivien ja täsmäytettävissä olevien pankkitilitapahtumien kirjasin muuttuu vihreäksi, ja **Kohdistettu**-valintaruutu on valittuna.
4. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

> [!TIP]
> Voit yhdistellä manuaalista ja automaattista vastaavuutta. Jos olet täsmäyttänyt manuaalisesti, automaattinen täsmäytyksen toiminto ei korvaa valittuja kohteita. 

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen manuaalisesti
1. Valitse **Pankkitilin täsmäytys** -sivun **Pankin tiliotteen rivit** -ruudussa kohdistamaton rivi.
2. Valitse **Pankkitilitapahtumat** -ruudussa yksi tai useampia pankkitilitapahtumia, joihin voidaan kohdistaa valitun pankin tiliotteen rivi. Voit valita useita rivejä pitämällä CTRL-näppäimen painettuna.

   > [!TIP]
   > Voit myös manuaalisesti täsmäyttää useita pankin tiliotteen rivejä yhteen pankkitilitapahtumaan. Tämä voi olla hyödyllistä esimerkiksi silloin, jos pankkitalletuksessa on useita maksutapoja, kuten eri liikkeellelaskijoiden luottokortit, ja pankkisi luettelee ne erillisinä riveinä. 
3. Valitse **Kohdista manuaalisesti** -toiminto.

    Valitun pankin tiliotteen rivin ja valittujen pankkitilitapahtumien fontti muuttuu vihreäksi, ja oikeanpuoleisen ruudun **Kohdistettu**-valintaruutu on valittuna.
4. Toista vaiheet 1–3 kaikille pankin tiliotteen riveille, joita ei ole kohdistettu.

> [!TIP]
> Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto. Jos olet täsmäyttänyt useita pankin tiliotteen rivejä yhteen tapahtumaan ja haluat poistaa yhden tai useamman täsmäytetyn rivin, kaikki manuaaliset vastaavuudet poistetaan tapahtumakirjauksesta, kun valitset **Poista vastaavuus**. 

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Puuttuvien tapahtumien luominen ja kohdistaminen pankin tiliotteen riveihin

Joskus pankin tiliotteessa on koron tai veloitetun maksun summia. Tällaisia tiliotteen rivejä ei voi kohdistaa, koska niillä ei ole vastaavia tapahtumia kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Tällöin jokaiselle tapahtumalle on kirjattava päiväkirjarivi. Näin luodaan liittyvä tapahtuma, johon kohdistus voidaan tehdä.

1. Valitse **Pankkitilin täsmäytys** -sivulla **Siirrä yleiseen päiväkirjaan** -toiminto.  
2. Määritä käytettävä yleinen päiväkirja **Siirrä p-til. täsm. yl. pvk:aan** -sivulla ja valitse sitten **OK**.

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää kaikkien puuttuvia tapahtumia sisältävien tiliotteiden päiväkirjarivit.
3. Syötä päiväkirjariville tarvittavat tiedot, kuten vastatili. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  
4. Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla **Testiraportti** -toiminto. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Pankkitilin täsmäytys** -sivun otsikot.
5. Valitse **Kirjaa**-toiminto.

    Kun tapahtuma on kirjattu, voit jatkaa tiliotteen rivin kohdistukseen.
6. Päivitä tai avaa **Pankkitilin täsmäytys** -sivu. Uusi tapahtuma näkyy **Pankkitilitapahtumat**-ruudussa.
7. Kohdista tiliotteen rivi pankkitilitapahtumaan manuaalisesti tai automaattisesti.

## <a name="undo-a-bank-account-reconciliation"></a>Pankkitilin täsmäytyksen peruuttaminen
Jos huomaat virheen kirjatussa pankkitäsmäytyksessä, voit korjata virheen käyttämällä **Pankkitilin tiliote** -sivun **Kumoa**-toimintoa. Kun peruutat kirjatun pankkitäsmäytyksen, tapahtumat siirretään **Pankkitilin täsmäytys** -sivulle ja merkitään **avoimiksi**, mikä tarkoittaa, että niitä ei ole täsmäytetty. Tämän jälkeen voit korjata pankkitäsmäytyksen ja kirjata sen uudelleen.

> [!NOTE]
> Pohjoisamerikkalaisessa versiossa voit käyttää Kumoa-toimintoa kirjattujen pankkitilien täsmäytysten ja tiliotteiden peruutukseen vain, kun otat käyttöön **Pankin täsmäytys ja autom. vastaavuus** -valitsimen **Pääkirjanpidon asetukset** -sivulla. Kumoa-toiminto ei ole käytettävissä pankkitiliotteissa, jotka on kirjattu pankkitilin täsmäytysten työkirjoista.

### <a name="reusing-the-bank-statement-number"></a>Pankintiliotteen numeron uudelleenkäyttö
Uuden pankkitilin täsmäytyksen tiliotteen numero otetaan pankkitililtä Viimeisen tiliotteen saldo -tiliotteena. Voit muuttaa näitä arvoja ennen uuden pankkitäsmäytyksen aloittamista. Kun kuitenkin luot uuden pankkitäsmäytyksen, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, onko tiliotteen numero jo määritetty kirjatulle tiliotteelle. Jos numero on käytössä, mutta haluat sen sijaan käyttöön uuden tiliotteen, voit käyttää **Muuta tiliotteen nroa** -toimintoa **Pankkitilin täsmäytys** -sivulla.

### <a name="examples"></a>Esimerkkejä
Seuraavassa on muutamia esimerkkejä siitä, miten korjataan kirjatun pankkitäsmäytyksen virhe käyttämällä samaa tai eri tiliotteen numeroa.

#### <a name="example-1"></a>Esimerkki 1
Teit pankkitäsmäytykset tammi-, helmi- ja maaliskuussa. Pankkitiliotteen numero oli maaliskuussa 100. Myöhemmin huomaat, että maaliskuu sisälsi merkinnät vain 30. päivä asti, mikä tarkoittaa merkinnät 31. päivältä puuttuvat. Joten sinun täytyy tehdä pankkitäsmäytys maaliskuulle uudelleen. Avaa tässä tapauksessa **Pankkitilin tiliote** -sivu, valitse maaliskuun tiliote ja valitse sitten **Kumoa**. 

Uudelle pankkitäsmäytykselle annetaan tilitteen numero 101. Voit määrittää numeron 100 uudelleen valitsemalla **Muuta tiliotteen nroa** ja syöttämällä arvon **100**. 

> [!TIP]
> Muista asettaa asianmukainen tilioteen lopetuspäivämäärä (tässä esimerkissä 31. maaliskuuta) ja muokkaa **Viimeisen tiliotteen saldo** -kenttää. 

#### <a name="example-2"></a>Esimerkki 2
Teit pankkitäsmäytykset tammi-, helmi, kesä- ja heinäkuussa. Huomaat, että helmikuu oli virheellinen. Oletetaan, että helmikuun tiliotteen numero oli 100. Kuten esimerkissä 1, käytetään Kumoa- ja Muuta tiliotteen nroa -toimintoja, jotka muuttavat tiliotteen numeron kuten yllä olevassa esimerkissä 1, jotta nyt voit tehdä uudelleen helmikuun pankkitilin täsmäytyksen.  

Sen jälkeen kun olet kirjannut helmikuun oikaistun pankkitäsmäytyksen, vastaavas Pankkitili-kortin **Viimeinen tiliotteen nro** -kentässä näkyy **100**, ja **Viimeisen tiliotteen saldo** -kentässä näkyy helmikuun tiliotteen loppusaldo. 

Jos teet seuraavan pankkitäsmäytyksen maaliskuussa, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää tiliotteen numeroksi 101 ja antaa sille oikean **Viimeisen tiliotteen saldo** -arvon.

Jos teet seuraavan pankkitäsmäytyksen elokuun osalta, harkitse arvojen muuttamista **Viimeinen tiliotteen nro**- ja **Viimeisen tiliotteen saldo** -kentissä **Pankkitili**-kortissa ennen seuraavan pankkitäsmäytyksen luomista tai käytä Muuta tiliotteen nroa -toimintoa ja muuta myös "Viimeisen tiliotteen saldo" -kentän arvoa pankkitilin täsmäytyssivulla.

> [!NOTE]
> Tiliotteen numero on tärkeä, kun teet pankkitäsmäytyksiä tuotujen CAMT-tiedostojen kanssa, jotka sisältävät tiliotteen numeroita, tai kun täsmäytetään tulostettujen tiliotteiden perusteella. Jos vain lataat joukon pankkitapahtumia verkkopankista, tiliotteen numero ei yleensä ole tärkeä. 
>
>Viimeisen tiliotteen saldo -arvoa pidetään pankkitilillä virheiden minimoimiseksi pankkitäsmäytyksiä tehtäessä. Sitä voi myös muokata, joten pankkitilin täsmäytykset voidaan tehdä missä tahansa järjestyksessä. Tämä tarkoittaa myös sitä, että jos peruutat pankin tiliotteen, uusi loppusaldo ei ehkä ole seuraavassa tiliotteessa Viimeisen tiliotteen saldo. Ei ole mitään toimintoa, jolla voi siirtää saldon eteenpäin kaikille myöhemmille tiliotteille. Tämä on hyvä ottaa huomioon Kumoa-toimintoa käytettäessä. 

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Automaattinen maksujen soveltamisen sääntöjen määrittäminen](receivables-how-set-up-payment-application-rules.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
