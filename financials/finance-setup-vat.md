---
title: "Tietoja arvonlisäveron määrittämisestä | Microsoft Docs"
description: "Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bf06b41a87e24af9e7657dd0585d7d13e3cad1b2
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---

# <a name="setting-up-included365finlongincludesd365finlongmdmd-to-calculate-and-post-value-added-tax"></a>[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in määrittäminen laskemaan ja kirjaamaan arvonlisävero
Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa määrittämään prosentti, jolla verosummat lasketaan, seuraavien tekijöiden perusteella: 

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  
  
Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. Voit helpottaa määritysten tekemistä avustetun **ALV-asetukset**-asennusoppaan avulla. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.

**Huomautus**: Voit käyttää opasta vain siinä tapauksessa, että olet luonut oman yrityksen etkä ole kirjannut ALV:n sisältäviä tapahtumia. Muussa tapauksessa on erittäin helppoa käyttää vahingossa eri ALV-prosentteja, mikä johtaisi virheellisiin ALV-raportteihin.  
  
Jos haluat määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä ohjeaiheessa. Esimerkiksi seuraavat aiheet käsitellään:  
  
* Liiketoiminnan ALV-kirjausryhmien määrittäminen määrittämään ALV-prosentit niille markkinoille, joilla sinulla on liiketoimintaa. Kirjausryhmät määritetään asiakkaille ja toimittajille.  
* Tuotteen ALV-kirjausryhmän määrittäminen määrittämään ALV-prosentit tuotteille ja palveluille, joita ostat tai myyt.  
  
   **Huomautus**: liiketoiminnan ja tuotteen ALV-kirjausryhmiin liittyvät käsitteet vastaavat yleisiä kirjausryhmiä. Lisätietoja on kohdassa [Kirjausryhmien asetukset](finance-posting-groups.md).
* Liiketoiminnan ja tuotteen ALV-kirjausryhmien luomaan ALV-asetuksia, jolla lasketaan myynnin ja ostojen ALV-summat.  
* Tuotteen ALV-kirjausryhmien määrittäminen niille pääkirjanpidon tileille, joita käytät myynnille ja ostoille sekä nimikkeille ja resursseille.  

   **Huomautus**: määritettäessä ALV:n resursseille, yrityksen **Ohjelmistopaketti**-käyttäjäkokemus on otettava käyttöön. Lisätietoja on kohdassa [Dynamics 365 for Financials -kokemuksen mukauttaminen](ui-experiences.md).
* ALV-vastakirjaus EU-maiden tai alueiden välisessä kaupassa.  
* ALV:n pyöristäminen asiakirjoja varten.  
* Poikkeavien ALV-prosenttien käyttöä selittävien lauseiden määrittäminen.
* ALV-numeroiden tarkistaminen.

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Avustetun ALV-asetusoppaan käyttö ALV:n määrityksessä (suositus)
Avustetun ALV-asetusten asennus oppaan käyttö on suositeltavaa määritettäessä ALV:tä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. 

Avaa avustettu asennusopas seuraavasti:
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Avustettu asennus** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-asetukset **.

## <a name="set-up-vat-business-posting-groups"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen
Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU **tai **Kotimaa**. Koodin tulee olla yksilöivä. Voit määrittää niin monta koodia kuin haluat, mutta koodin on oltava yksilöivä eli sama koodi ei voi olla samassa taulukossa kahdesti.
  
Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Liiketoim. ALV-kirjausryhmä** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot luodaan linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin. 

## <a name="set-up-vat-product-posting-groups"></a>Tuotteen ALV-kirjausryhmien määrittäminen
Tuotteen ALV-kirjausryhmät vastaavat nimikkeitä tai resursseja, joita ostat tai myyt, ja määrittävät ALV:n laskennan ja kirjaamisen ostettavan tai myytävän nimikkeen tai resurssin mukaan.
Olisi hyvä käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 %, ja **ALV25** tai **Vakio**, jos ALV on 25 %.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Tuotteen ALV-kirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Jos haluat ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet, voit määrittää **ALV-tunnuksen** kullekin ryhmälle ja liittää tunnuksen ryhmän jäsenille.

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille
Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tekemään niin oletusarvoisesti. Määrityksen voi tehdä kahdella tavalla:

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin. 
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>ALV-kirjausryhmien määrittäminen yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille
Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille 
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Avaa valitun tilin **KP-tilin** kortti.
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
5. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille  
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse liiketoiminnan ALV-kirjausryhmä.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille  
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimike** tai **Resurssi** ja valitse sitten liittyvä linkki.  
2. Tee jompikumpi seuraavista toimista:
* Laajenna **Nimike**-kortin **Hinta ja kirjaus** -pikavälilehti ja valitse sitten **Näytä lisää**.  
* Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Poikkeavien ALV-prosenttien käyttöä selittävien lauseiden määrittäminen.
Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Tietoja voidaan vaatia hallituksen asetuksella. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää. 

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.
  
### <a name="to-set-up-vat-clauses"></a>ALV-lauseiden määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **ALV-lauseet** ja valitse sitten liittyvä linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään teksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla riveillä.  
5. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin ALV-kirjausten asetukset -sivulla.  
6. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>ALV-lauseen määrittäminen ALV-kirjausryhmään
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-lause**-sarakkeessa lause, jota käytetään kussakin ALV-kirjauksen asetuksissa, joihin sitä sovelletaan.  

### <a name="to-specify-translations-for-vat-clauses"></a>ALV-lauseiden käännösten määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **ALV-lauseet** ja valitse sitten liittyvä linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>ALV-kirjausten asetukset luominen käsittelemään tuonnin ALV:tä
Tuonnin ALV -ominaisuudella kirjataan asiakirja, jossa koko summaa on ALV:tä. Tämä on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  
  
Määritä tuonnin ALV:n koodit seuraavasti:  
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Tuotteen ALV-kirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **ALV-kirjausten asetukset** ja valitse sitten liittyvä linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  
  
## <a name="verify-vat-registration-numbers"></a>ALV-numeroiden tarkistaminen.
On tärkeää, että käytössäsi olevat asiakkaiden, toimittajien ja yhteystietojen ALV-rekisteröintinumerot ovat oikeita. Yritykset esimerkiksi joskus muuttavat verovelkatilaansa, ja joissakin maissa veroviranomaiset voivat pyytää raportteja, kuten EU-myyntiluetteloraportin, joissa on luettelo liiketoiminnassasi käyttämistäsi ALV-rekisteröintinumeroista.  
  
Euroopan komission sivustossa on julkinen ja maksuton ALV-tietojen vaihtojärjestelmä (VIES-palvelu). Palvelun käyttö kuitenkin edellyttää sivustoon siirtymistä. [!INCLUDE[d365fin](includes/d365fin_md.md)]ia käytettäessä sivustoon siirtyminen ei ole tarpeellista, sillä voit tarkistaa sovelluksessa VIES-palvelusta asiakkaiden, toimittajien ja yhteystietojen ALV-numerot asiakkaan, toimittajan ja yhteystiedon kortista. Voit myös seurata kyseisiä ALV-numeroita. Tämän [!INCLUDE[d365fin](includes/d365fin_md.md)]in palvelun nimi on EU:n ALV- Nro tarkistuspalvelu. Sitä voi käyttää **Palvelun yhteydet** -sivulla, ja voit aloittaa sen käytön valitsemalla valintaruudun. Palvelu on maksuton eikä kirjautumista tarvita.

Kun käytät palvelua, kunkin asiakkaan, toimittajan tai yhteystiedon ALV-numeroiden ja tarkistusten historiatiedot kirjataan **ALV-rekisteröintilokiin**, joten niiden seuraaminen on helppoa. Loki on asiakaskohtainen. Lokin avulla voi esimerkiksi kätevästi todistaa, että olet tarkistanut nykyisen ALV-numeron oikeellisuuden. Kun tarkistat ALV-numeron, lokin **Pyynnön tunnus** -sarake osoittaa, että tehnyt niin. 

Voit tarkastella ALV-rekisteröintilokia asiakkaan, toimittajan tai kontaktin kortissa valitsemalla **Laskutus**-pikavälilehdessä hakupainikkeen **ALV-rekisterinro** -kentässä.  

Palvelu säästää myös hieman aikaa, kun luot asiakasta tai toimittajaa. Jos tiedät asiakkaan ALV-numeron, voit antaa sen **ALV-rekisterinro** -kentässä asiakkaan tai toimittajan kortissa, jolloin asiakkaan nimi etsitään valmiiksi. Joissakin maissa myös yrityksen osoitteet ilmoitetaan jäsennetyssä muodossa. Näissä maissa myös osoitetiedot täytetään puolestasi.  

**Huomautus**: ALV-tietojen vaihtojärjestelmän (VIES-palvelun) on hyvä muistaa pari asiaa:

* Palvelu käyttää http-protokollaa, joten palvelun kautta siirretyt tiedot eivät ole salattuja.
* Palvelu voi olla ajoittain pois käytöstä Microsoftista riippumattomista syistä. Palvelu on osa EU:n laajaa kansallisten ALV-rekisterien verkostoa.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>ALV-vastakirjaus EU-maiden tai alueiden välisessä kaupassa
Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.

**Huomautus**: Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa tai toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

**Vihje**: Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa. Palvelua voi käyttää maksutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on tämän ohjeaiheen osassa _ALV-rekisteröintinumeroiden tarkistaminen_.

### <a name="sales-to-eu-countries-or-regions"></a>Myynti EU-maihin tai -alueille
ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.
Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  
  
* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos olet jo määrittänyt rivejä EU-maista/alueilta tapahtuvia ostoja varten ALV-kirjausten asetukset -ikkunassa, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on lisättävä myös **ALV-rekisterinro** kenttään **Ulkomaankauppa**-pikavälilehdessä.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta (ALV-summan laskemiseen käytettävästä summasta). Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

## <a name="understanding-vat-rounding-for-documents"></a>ALV:n pyöristäminen asiakirjoja varten
Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. ALV lasketaan koko asiakirjalle, mikä tarkoittaa sitä, että ALV, joka on laskettu asiakirjasta perustuu kaikkien rivien summaan, joilla on sama ALV-tunnus asiakirjassa.

## <a name="see-also"></a>Katso myös  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)
