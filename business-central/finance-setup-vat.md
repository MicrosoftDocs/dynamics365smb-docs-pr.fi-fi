---
title: "Tietoja arvonlisäveron määrittämisestä | Microsoft Docs"
description: "Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5f22880f56cd2834c9bd92061f166cd457bc58c1
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---

# <a name="setting-up-calculations-and-posting-methods-for-value-added-tax"></a>Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen
Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa määrittämään prosentti, jolla verosummat lasketaan, seuraavien tekijöiden perusteella:

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  

Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. Voit helpottaa määritysten tekemistä **ALV-asetusten** ohjatun määrityksen avulla. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.

> [!NOTE]  
>   Voit käyttää opasta vain siinä tapauksessa, että olet luonut oman yrityksen etkä ole kirjannut ALV:n sisältäviä tapahtumia. Muussa tapauksessa on erittäin helppoa käyttää vahingossa eri ALV-prosentteja, mikä johtaisi virheellisiin ALV-raportteihin.  

Jos haluat määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä ohjeaiheessa.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>ALV-asetusten ohjatun määritysoppaan käyttäminen ALV:n määrityksessä (suositus)
Avustetun ALV-asetusten asennus oppaan käyttö on suositeltavaa määritettäessä ALV:tä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.

Avaa avustettu asennusopas seuraavasti:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys**.  
2. Valitse **Määritä ALV**.

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>Oman maan tai alueen ALV-rekisteröintinumeroiden määrittäminen
Voit auttaa varmistamaan, että annettavat ALV-rekisteröintinumerot ovat kelvollisia, määrittämällä niiden maiden tai alueiden ALV-rekisteröintinumeroiden muodot, joissa sinulla on liiketoimintaa. [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää virhesanoman, kun joku tekee virheen tai käyttää muotoa, jota ei hyväksytä maassa tai alueella.

ALV-rekisteröintinumeroiden määritysohjeet:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maat/alueet**.
2. Valitse ensin maa tai alue ja sitten **ALV-rekisteröintinron muodot** -toiminto.
3. Määritä muoto **Muodot**-kenttään antamalla vähintään yksi seuraavista merkeistä:  

* **#** - edellyttää yksimerkkistä lukua.  
* **@** - edellyttää kirjainta. Kirjainkoolla ei ole merkitystä.  
* **?** Mikä tahansa merkki sallitaan.  

    > [!Tip]
    > Voit käyttää muita merkkejä, kunhan niitä käytetään maan tai alueen muodossa. Jos sinun on sisällytettävä esimerkiksi numeroiden välinen piste tai yhdysviiva, voit määrittää muodon seuraavasti: ##.####.### tai @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Liiketoiminnan ALV-kirjausryhmien luominen
Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU** tai **Kotimaa**. Koodin tulee olla yksilöivä. Voit määrittää niin monta koodia kuin haluat, mutta koodin on oltava yksilöivä eli sama koodi ei voi olla samassa taulukossa kahdesti.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoim. ALV-kirjausryhmä** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot luodaan linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin.

## <a name="to-set-up-vat-product-posting-groups"></a>Tuotteen ALV-kirjausryhmien luominen
Tuotteen ALV-kirjausryhmät vastaavat nimikkeitä tai resursseja, joita ostat tai myyt, ja määrittävät ALV:n laskennan ja kirjaamisen ostettavan tai myytävän nimikkeen tai resurssin mukaan.  
Olisi hyvä käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 %, ja **ALV25** tai **Vakio**, jos ALV on 25 %.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Jos haluat ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet, voit määrittää **ALV-tunnuksen** kullekin ryhmälle ja liittää tunnuksen ryhmän jäsenille.

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille
Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tekemään niin oletusarvoisesti. Määrityksen voi tehdä kahdella tavalla:

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin.
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## <a name="to-assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>ALV-kirjausryhmien määrittäminen yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille
Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Avaa valitun tilin **KP-tilin** kortti.  
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
5. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse liiketoiminnan ALV-kirjausryhmä.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** tai **Resurssi** ja valitse sitten liittyvä linkki.  
2. Tee jompikumpi seuraavista toimista:  

* Laajenna **Nimike**-kortin **Hinta ja kirjaus** -pikavälilehti ja valitse sitten **Näytä lisää**. **Tuotteen ALV-kirjausryhmä** -kenttä avautuu.  
* Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.  

## <a name="setting-up-vat-statement-templates-and-vat-statement-names"></a>ALV-ilmoitusmallien ja ALV-ilmoitusten nimien määrittäminen
Veroviranomaiset voivat muuttaa ALV:n kirjausvaatimuksia. **ALV-ilmoitusmallit** ja **ALV-ilmoitusten nimet** voivat auttaa tulevien muutosten valmistelemisessa. Niiden avulla siirtyminen uusiin vaatimuksiin on sujuva. Voit käyttää ALV-ilmoitusmalleja, kun määrität laskelmien määrittämisessä käytettäviä ALV-ilmoituksen sisältäviä kenttiä. Voit luoda uuden ALV-ilmoitusmallin, kun vaatimukset muuttuvat. Esimerkiksi yksi malli voi laskea tämän vuoden ALV:n nykyisten vaatimusten ja toinen malli seuraavan vuoden vaatimusten perusteella. Mallien avulla voi myös ylläpitää ALV-ilmoitusten muotojen historiaa esimerkiksi niin, että voit katsoa, miten edellisen vuoden ALV laskettiin.

## <a name="how-to-define-and-preview-vat-statements"></a>ALV-ilmoitusten määrittäminen ja esikatselu
ALV-ilmoitusten avulla voi laskea ALV-laskelman summan tietyltä kaudelta, esimerkiksi neljännesvuoden ajalta. Kun ALV-ilmoitus on määritetty, voit esikatsella sitä ja varmistaa, että se täyttää tarpeet.

Voit määrittää ALV-ilmoituksen seuraavien vaiheiden avulla:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-ilmoitukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Nimi**-kenttä ja valitse sitten **ALV-ilmoitusten nimet** -sivulla **Uusi** .
3. Täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Tip]
> Voit suodattaa ilmoituksen sisältämät tiedot sen mukaan, mikä arvo **Tyyppi**-kentässä on valittu. **Tilien summat** -kohta on hyödyllinen silloin, kun haetaan tietyn tilin ALV.
**ALV-tapahtumien summat** hakee ALV:n **Yleinen kirjaustyyppi**-, **Liiketoiminnan ALV-kirjausryhmä**- ja/tai **Tuotteen ALV-kirjausryhmä** -kenttien valikoimaan liitetyistä tileistä. Voit syöttää arvon **Rivien summat** -kenttään tai pikasuodattimen ehdot **Rivien summat** -kenttään. Lisätietoja on kohdassa [Tietojen hakeminen, suodattaminen ja lajitteleminen](ui-enter-criteria-filters.md). **Kuvaus**-kohtaa käytetään usein, kun ilmoitukseen lisätään huomautus. Voit käyttää sitä esimerkiksi otsikkona, kun käytössä on rivien summa.

Voit esikatsella ALV-ilmoitusta seuraavien vaiheiden avulla:

1. Valitse **Esikatselu**.
2. Aseta päivämääräsuodatus, jos haluat rajoittaa ilmoituksen tietylle kaudelle. Lisätietoja sivun mukauttamisesta niin, että sivulla näkyy päivämääräsuodatin, on kohdassa [Tietojen hakeminen, suodattaminen ja lajitteleminen](ui-enter-criteria-filters.md).
3. Voit valita eri vaihtoehtoja ja siten määrittää, minkä tyyppiset ALV-tapahtumat sisällytetään ALV-ilmoitukseen.
4. Niillä riveillä, joiden **Tyyppi**-kentässä lukee **ALV-tapahtumien summat**, näkyy luettelo ALV-tapahtumista, kun valitset summan **Sarakkeen summa** -kentässä.   

## <a name="to-set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Poikkeavien ALV-prosenttien käyttöä selittävien lauseiden määrittäminen
Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Tietoja voidaan vaatia hallituksen asetuksella. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää.

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.

Voit muokata tai poistaa ALV-lauseen, ja muutokset näkyvät luodussa raportissa. [!INCLUDE[d365fin](includes/d365fin_md.md)] ei kuitenkaan säilytä muutoshistoriaa. Raportissa ALV-lauseen kuvaukset tulostetaan ja näytetään raportin kaikille riveille ALV-summan ja ALV-perusteen summan rinnalla. Jos ALV-lausetta ei ole määritetty millekään myyntiasiakirjan riville, koko osa jätetään pois raporttia tulostettaessa.

### <a name="to-set-up-vat-clauses"></a>ALV-lauseiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten liittyvä linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään teksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla riveillä.  
5. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin ALV-kirjausten asetukset -sivulla.  
6. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>ALV-lauseen määrittäminen ALV-kirjausryhmään
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-lause**-sarakkeessa lause, jota käytetään kussakin ALV-kirjauksen asetuksissa, joihin sitä sovelletaan.  

### <a name="to-specify-translations-for-vat-clauses"></a>ALV-lauseiden käännösten määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten liittyvä linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>ALV-kirjausten asetusten luominen käsittelemään tuonnin ALV:tä
Tuonnin ALV -ominaisuudella kirjataan asiakirja, jossa koko summaa on ALV:tä. Tämä on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  

Määritä tuonnin ALV:n koodit seuraavasti:  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  

## <a name="to-verify-vat-registration-numbers"></a>ALV-numeroiden tarkistaminen
On tärkeää, että käytössäsi olevat asiakkaiden, toimittajien ja yhteystietojen ALV-rekisteröintinumerot ovat oikeita. Yritykset esimerkiksi joskus muuttavat verovelkatilaansa, ja joissakin maissa veroviranomaiset voivat pyytää raportteja, kuten EU-myyntiluetteloraportin, joissa on luettelo liiketoiminnassasi käyttämistäsi ALV-rekisteröintinumeroista.

Euroopan komission sivustossa on julkinen ja maksuton ALV-tietojen vaihtojärjestelmä (VIES-palvelu). [!INCLUDE[d365fin](includes/d365fin_md.md)]ia käytettäessä sivustoon siirtyminen ei ole tarpeellista, sillä voit tarkistaa sovelluksessa VIES-palvelusta asiakkaiden, toimittajien ja yhteystietojen ALV-numerot asiakkaan, toimittajan ja yhteystiedon kortista. Voit myös seurata kyseisiä ALV-numeroita. [!INCLUDE[d365fin](includes/d365fin_md.md)]in palvelun nimi on **EU:n ALV-nron tarkistuspalvelun määritys**. Palvelua voi käyttää **Palvelun yhteydet** -sivulla ja sen käytön voi aloittaa heti. Palveluyhteys on maksuton eikä kirjautumista tarvita.

> [!Note]
> Voit ottaa käyttöön EU:n ALV-nron tarkistuspalvelun, jos sinulla on järjestelmänvalvojan käyttöoikeudet.

Kun käytät palveluyhteyttä, kunkin asiakkaan, toimittajan tai yhteystiedon ALV-numeroiden ja tarkistusten historiatiedot kirjataan **ALV-rekisteröintilokiin**, joten niiden seuraaminen on helppoa. Loki on asiakaskohtainen. Lokin avulla voi esimerkiksi kätevästi todistaa, että olet tarkistanut nykyisen ALV-numeron oikeellisuuden. Kun tarkistat ALV-numeron, lokin **Pyynnön tunnus** -sarake osoittaa, että olet tehnyt niin.

Voit tarkastella ALV-rekisteröintilokia asiakkaan, toimittajan tai kontaktin kortissa valitsemalla **Laskutus**-pikavälilehdessä **ALV-rekisterinro** -kentässä hakupainikkeen.  

Palvelu voi myös säästää aikaa asiakasta tai toimittajaa luotaessa. Jos tiedät asiakkaan ALV-numeron, voit antaa sen asiakkaan tai toimittajan kortin **ALV-rekisterinro** -kentässä, jolloin asiakkaan nimi täytetään valmiiksi. Joissakin maissa myös yrityksen osoitteet ilmoitetaan jäsennetyssä muodossa. Näissä maissa myös osoitetiedot täytetään valmiiksi.  

ALV-tietojen vaihtojärjestelmästä (VIES-palvelusta) on hyvä muistaa pari asiaa:

* Palvelu käyttää http-protokollaa, joten palvelun kautta siirretyt tiedot eivät ole salattuja.  
* Palvelu voi olla ajoittain pois käytöstä Microsoftista riippumattomista syistä. Palvelu on osa EU:n laajaa kansallisten ALV-rekisterien verkostoa.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>ALV-vastakirjaus EU-maiden tai -alueiden välisessä kaupassa
Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.  

> [!NOTE]  
> Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa / toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

> [!TIP]  
> Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa. Palvelua voi käyttää maksutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on tämän ohjeaiheen osassa _ALV-rekisteröintinumeroiden tarkistaminen_.

### <a name="sales-to-eu-countries-or-regions"></a>Myynti EU-maihin tai -alueille
ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.  

Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  

* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos olet jo määrittänyt rivejä EU-maista/alueilta tapahtuvia ostoja varten ALV-kirjausten asetukset -sivulla, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on myös lisättävä **Ulkomaankauppa**-pikavälilehden **ALV-rekisterinro**-kenttään.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta (ALV-summan laskemiseen käytettävästä summasta). Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

## <a name="understanding-vat-rounding-for-documents"></a>ALV:n pyöristäminen asiakirjoja varten
Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. ALV lasketaan koko asiakirjalle, mikä tarkoittaa sitä, että laskettu ALV perustuu kaikkien rivien summaan, joilla on sama ALV-tunnus asiakirjassa.

## <a name="understanding-the-vat-rate-conversion-process"></a>Tietoja ALV-prosentin muutosprosessista  
ALV-prosentin muutostyökalu suorittaa päätietojen, päiväkirjojen ja tilauksien ALV-prosenttimuunnoksia eri tavoilla. Valitut perustiedot ja kirjauskansiot päivitetään uuden yleisen tuotteen kirjausryhmän tai ALV-tuotteen kirjausryhmän toimesta. Jos tilaus on kokonaan tai osittain toimitettu, toimitetut nimikkeet säilyvät nykyisessä tuotteen kirjausryhmässä tai tuotteen ALV-kirjausryhmässä. Uusi tilausrivi luodaan lähettämättömiä kohteita varten ja päivitetään nykyisen ja uuden ALV- tai yleisen tuotekirjausryhmän mukaan. Lisäksi nimikekulujen määritykset, varaukset ja nimikkeiden seurantatiedot päivitetään tämän mukaisesti.  

Työkalu ei kuitenkaan tee muutoksia seuraavissa tilanteissa:

* Myynti- tai ostotilaukset ja laskut, jossa toimitukset on kirjattu. Nämä asiakirjat kirjataan käyttämällä nykyistä ALV-prosenttia.  
* Asiakirjat, joissa kirjattuja ennakkomaksulaskuja. Olet ehkä tehnyt ennakkomaksuja tai vastaanottanut niitä laskuista, joita ei ole tehty valmiiksi ennen ALV-prosentin muutostyökalun käyttämistä. Tässä tapauksessa erääntyvän ALV:n ja ennakkomaksuissa maksetun ALV:n välillä on ero, kun lasku on valmis. ALV-prosentin muutostyökalu ohittaa nämä asiakirjat ja ne täytyy päivittää manuaalisesti.  
* Suora toimitukset tai erikoistilaukset.  
* Varaston integroinnin sisältävät myynti- tai ostotilaukset, jos ne on osittain toimitettu tai vastaanotettu.  
* Huoltosopimukset.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Suorita ALV-kurssimuutoksen muunnokset  
Ennen ALV:n muutostyökalun määrittämistä sinun on tehtävä seuraavat valmistelut.

* Jos sinulla on eri kursseja käyttäviä tapahtumia, ne on erotettava eri ryhmiin joko luomalla jokaiselle kurssille uusi pääkirjanpitotili tai ryhmittelemällä tapahtumat kurssin mukaan tietosuodattimien avulla.  
* Jos luot uusia kirjanpitotilejä, sinun on luotava myös uusia yleisiä kirjausryhmiä.  
* Vähentääksesi muunnettavien asiakirjojen määrää, kirjaa niin monta asiakirjaa kuin mahdollista ja vähennä kirjaamattomat asiakirjat minimiin.  
* Tietojen varmuuskopiointi.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Määritä ALV-prosentin muutostyökalu  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosenttimuutoksen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Päätiedot**-, **Päiväkirjat**- ja **Asiakirjat**-pikavälilehdissä kirjausryhmän arvo tarvittavien kenttien asetusluettelosta.  

### <a name="to-set-up-product-posting-group-conversion"></a>Määritä tuotteiden ALV-kirjausryhmien muunnos  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosenttimuutoksen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-prosenttimuutoksen asetukset** -ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä joko **Tuotteen ALV-kirjausryhmän muunto** tai **Yleisen tuotteen kirjausryhmän muunto**.  
3. Anna **Koodista** -kentässä nykyinen kirjausryhmä.  
4. Syötä uusi kirjausryhmä **Koodiin**-kenttään.  

### <a name="to-perform-vat-rate-change-conversion"></a>Suorita ALV-kurssimuutoksen muunnos  
ALV-prosentin muutostyökalun avulla voit hallita muutoksia ALV:n vakiokorvauksesta. Voit tehdä ALV- ja yleisen kirjausryhmän muunnokset muuttaaksesi ALV-prosentetia ja ylläpitääksesi ALV- raportointia. Asetusten mukaan tehdään seuraavat muutokset:  

* ALV-kirjausryhmät ja yleiset kirjauryhmät on muunnettu.  
* Muutokset toteutetaan esimerkiksi pääkirjanpitotileissä, asiakkaissa, toimittajissa, avoimissa asiakirjoissa ja päiväkirjariveillä.  

> [!IMPORTANT]  
>  Testaa muunto ennen ALV-prosentin muutosta. Voit tehdä sen seuraavien ohjeiden mukaisesti, mutta muista poistaa **Suorita muuntaminen**- ja **ALV-prosentin muutostyökalu valmis** -valintaruutujen valinta. Testimuunnoksen aikana **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä tyhjennetään ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kenttä on tyhjä. Kun muuntaminen on valmis, voit tarkastella testimuutoksen tulokset valitsemalla **ALV-prosentin muutoslokin tapahtumat**. Tarkista jokainen tapahtuma ennen muuntamista. Tarkista erityisesti tapahtumat, jotka käyttävät vanhaa ALV-prosenttia.     

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosenttimuutos**, ja valitse sitten **ALV-prosenttimuutoksen asetukset** -linkki.  
2. Varmista, että olet jo määrittänyt tuotteen ALV-kirjausryhmän muunnoksen tai yleisen tuotteen kirjausryhmän muunnoksen.  
3. Valitse **Suorita muuntaminen** -valintaruutu.  

    > [!IMPORTANT]  
    >  Poista **ALV-prosentin muutostyökalu valmis** -valintaruudun valinta. Valintaruutu merkitään automaattisesti, kun ALV:n määrän muunnos on valmis.  

4. Valitse **Muunna**-toiminto.  
5. Kun muuntaminen on valmis, valitse **Koti**-välilehdeltä **Prosessi**-ryhmä, ja valitse **ALV-prosentin muutoslokin tapahtumat** nähdäksesi muunnoksen tulokset.  

> [!IMPORTANT]  
>  Muutoksen jälkeen **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä on valittuna ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kentässä näkyy muunnospäivämäärä.  

## <a name="see-also"></a>Katso myös  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[Toimintaohje: ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  

