---
title: Pankkitilitalletusten luominen
description: 'Voit tehdä talletuksia ja ylläpitää tapahtumatietueita, jotka sisältävät tietoja, joita voi käyttää avoimiin laskuihin ja hyvityslaskuihin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'bank, deposit'
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 07/25/2024
ms.custom: bap-template
---

# <a name="create-bank-deposits"></a>Pankkitilitalletusten luominen

> [!NOTE]
> Mahdollisuus luoda pankkitalletuksia- on uusi ominaisuus useissa maissa ja useilla alueilla Business Centralin vuoden 2022 1. julkaisuaallossa. Jos käytit Business Centralia Yhdysvalloissa, Kanadassa tai Meksikossa ennen kyseistä julkaisua, käytössäsi saattaa olla aiemmat ominaisuudet. Voit jatkaa, mutta uudet ominaisuudet korvaavat vanhat ominaisuudet tulevassa versiossa. Jos haluat käyttää tässä artikkelissa kuvattuja uusia ominaisuuksia, järjestelmänvalvoja voi siirtyä **Ominaisuuksien hallinta** -sivulle ja ottaa käyttöön **Ominaisuuspäivitys: Standardoidut pankkitäsmäytykset ja -talletukset** -asetuksen.  

**Pankkitalletukset**-sivulla voit rekisteröidä talletuksia yhtenä asiakirjana, joka kirjaa yhden tai useamman merkinnän pankkitiliin. Yleensä pankkitalletuksia käytetään käteistalletusten rekisteröimiseen. Pankkitalletukset-sivu on käytettävissä Business Managerin roolikeskuksessa **Kassan hallinta** -valikossa ja muissa kassanhallintaa käsittelevissä roolikeskuksissa.

Pankkitalletuksiin liittyvät summat voivat olla peräisin useista lähteistä:

* Myynti, tuoton KP-tilin avulla.
* Asiakasmaksut.
* Käteishyvitykset toimittajilta tai käteismaksut toimittajille. 

Pankkitalletusrivit sisältävät tietoja yksittäisistä talletuksista, kuten asiakkailta saaduista sekeistä. Rivien summien kokonaissumman täytyy olla sama talletuksen kokonaissumman kanssa.

Kun olet täyttänyt talletustiedot ja -rivit, sinun täytyy kirjata se. Kirjaus päivittää asianmukaiset kirjanpidot. Nämä kirjanpidot sisältävät pääkirjanpidon sekä pankki-, asiakas-ja toimittajakirjauskansiot. Kirjatut talletukset tallennetaan myöhempää tarvetta varten **Kirjatut pankkitalletukset** -sivulle.

**Pankkitalletus**-raportissa näkyvät asiakkaan ja toimittajan talletukset, joissa on alkuperäinen talletussumma, avoimena jäljellä olevan talletuksen summa ja kohdistettu summa. Raportissa näkyy myös kirjatun talletuksen kokonaissumma täsmäytystä varten.

## <a name="before-you-start"></a>Ennen kuin aloitat

On määritettävä muutamia asioita ennen pankkitalletusten käyttämistä. Sinulla täytyy olla numerosarja ja yleisen päiväkirjan malli valmiina. Sinun tulisi myös määrittää, kirjataanko pankkitalletusten summat kokonaissummana. Tämä tarkoittaa, että kaikkien talletusrivien summien yhteenlaskettu kokonaissumma. Muussa tapauksessa jokainen rivi kirjataan yksittäisenä tapahtumana. Talletuksen kirjaaminen yhtenä pankkitapahtumana voi helpottaa pankkitäsmäytyksen tekemistä.

### <a name="number-series-and-lump-sum-deposits"></a>Numerosarjat ja kertasummatalletukset

Sinun täytyy määrittää pankkitalletuksille numerosarja ja määrittää sitten sarja **Myynnin ja saamisten asetukset** -sivun **Pankkitalletusten nrot** -kentässä. Lue lisätietoja numerosarjoista kohdassa [Numerosarjojen luominen](ui-create-number-series.md).

Ota **Myynnin ja saamisten asetukset** -sivulla **Kirjaa pankkitalletukset kertasummana** -valitsin käyttöön kirjataksesi myös talletuksia kertasuorituksina yksittäisten rivien sijaan. Talletuksen kirjaaminen kertasuorituksena luo yhden pankkitapahtuman koko talletuksen summaa varten, joka voi helpottaa pankkitäsmäytyksen tekemistä.

### <a name="general-journal-templates-for-bank-deposits"></a>Pankkitalletuksiin liittyvät yleisen päiväkirjan mallit

Talletuksille on myös luotava yleisen päiväkirjan malli. Yleisiä päiväkirjoja käytetään pankki-, asiakas-, toimittaja- ja käyttöomaisuus- ja KP-tilien tapahtumien kirjaamiseen. Päiväkirjan mallit suunnittelevat yleisen päiväkirjan sopimaan työsi tarkoitukseen. Tämä tarkoittaa sitä, että päiväkirjan mallin kentät ovat juuri niitä, joita tarvitset.

Talletukset ovat kassakuitteja, joten haluat ehkä käyttää numerosarjaa uudelleen kassapäiväkirjoissa. Vaihtoehtoisesti, jos sinun täytyy erottaa pankkitalletukset ja kassapäiväkirjatapahtumat, käytä eri numerosarjaa.

Mallille on myös luotava erätyö. Voit luoda erätyön valitsemalla **Yleisen päivä kirjan mallit** -sivulla **Erät**-toiminnon. Jos haluat lisätietoja eristä, siirry kohtaan [Päiväkirjan mallien ja erien käyttäminen](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a>Dimensiot pankkitalletusriveillä

Pankkitalletuksen rivit käyttävät automaattisesti **osastokoodi**- ja **asiakasryhmäkoodi**-kentissä määritettyjä oletusdimensioita. Kun valitset **Tilityyppi**  -kentässä **asiakas** tai **toimittaja**, asiakkaalle tai toimittajalle määritetyt dimensiot korvaavat oletukset. Voit muuttaa rivien dimensioita tarvittaessa.

> [!TIP]
> Rivien dimensio määritetään oletusdimensioprioriteettien mukaisesti. Rivin dimensiot priorisoidaan ennen otsikon dimensioita. Voit välttää ristiriitoja luomalla sääntöjä, jotka priorisoivat dimension käyttöä lähteen mukaan. Jos haluat muuttaa dimensioiden priorisointia, voit muuttaa niiden sijoitusta **Oletusdimensioprioriteetit**-sivulla. Lisätietoja on kohdassa [Oletusdimensioprioriteettien määrittäminen](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit"></a>Pankkitalletuksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitalletukset** ja valitse sitten vastaava linkki.
2. Avaa **Pankkitalletus**-sivu valitsemalla **Uusi**.
3. Valitse yleisen päiväkirjan malli, jonka loit pankkitalletuksille.  

    > [!NOTE]
    > Jos yleisenpäivä kirjan mallissa on enemmän kuin kaksi erää, ohjelma pyytää valitsemaan yhden.

4. Valitse **Pankkitilin nro**-kentässä pankkitili, johon haluat tehdä talletuksen.

    > [!TIP]
    > Voit tuplatarkistaa, että olet tallettamassa oikealle tilille, käyttämällä **Tilin kortti** -ja **Tilitapahtumat**-toimintoa, kun haluat etsiä valitulle pankkitilille liittyviä tapahtumia. Voit esimerkiksi tarkistaa, onko tilille tehty samanlaisia talletuksia.

5. Syötä **Kokonaistalletussumma** -kenttään talletuksen kokonaissumma. Tämän summan on oltava kaikkien rivien summien yhteenlaskettu summa.
6. Täytä tarvittavat jäljellä olevat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Kirjauspvm-kentän **päivämäärä** ja Osastokoodi **- ja** Asiakasryhmäkoodi-kenttien **dimensiot** määritetään riveille, jotka luot pankkitalletusta varten. Niitä voidaan muuttaa tarvittaessa.

7. Sen mukaan, haluatko kirjata pankkitalletuksen kertasummana vai jokaisen rivin erikseen pankkitilille, käännä **Kirjaa kertasummana** -valitsin päälle tai pois päältä. Oletusasetuksena on sama valitsin **Myynnin ja saamisten asetukset** -sivulla.

    > [!NOTE]
    > **Valuuttakoodi**-kentässä näkyy valitsemallesi pankkitilille määritetty valuutta. Et voi valita eri valuuttaa.

8. Luo **Rivit**-pikavälilehdessä uusi rivi jokaista talletettavaa käteismaksua kohti.
9. Määritä **Tilityyppi**-kentässä, mistä maksu on peräisin. Pankkitalletuksille tyyppi on yleensä **asiakas** tai **toimittaja**.

    > [!NOTE]
    > Voit myös rekisteröidä käteismaksun toimittajalle. Voit tehdä sen valitsemalla **Toimittaja** ja syöttämällä sitten maksusumman negatiivisena lukuna rivin **Kredit-summa** -kenttään.

10. Lisää **Asiakirjan nro** -kenttään toimittajan laskun asiakirjanumero, josta kredit-summa on peräisin. Voit käyttää asiakirjanumeroa jokaiselle riville tai samaa numeroa kaikille riveille.

    > [!TIP]
    > Yleensä rahoitustapahtumien **asiakirjatyyppi**-kenttää ei tarvitse täyttää. Jos esimerkiksi talletat rahaa päivän myynnistä, jätät kentän tyhjäksi. Jos talletat käteistä asiakasmaksusta, valitset **Maksu**.

11. Jos talletat käteismaksun tietylle myyntilaskulle, valitse **Kohdista tapahtumat** -toiminto ja syötä sitten laskun numero **Kohdistetaan tunnisteeseen** -kenttään.
12. Jos olet valmis kirjaamaan pankkitalletuksen, valitse **Kirjaa**-toimenpide.

    > [!TIP]
    > Voit tarkistaa tiedot ennen talletuksen kirjaamista valitsemalla **Testiraportti** -toiminnon. Raportissa näkyy, onko ongelmia, kuten puuttuvia tietoja, jotka estävät kirjauksen.  

## <a name="find-posted-bank-deposits"></a>Kirjattujen pankkitalletusten etsiminen

**Kirjatut pankkitalletukset** -sivulla on luettelo yrityksesi aiemmista talletuksista. Luettelossa voit tarkistaa talletuksille määritetyt kommentit ja dimensiot. Voit avata pankkitalletuksen nähdäksesi lisätietoja, ja sieltä voit tutkia tarkemmin. Voit esimerkiksi valita **Etsi tapahtumat** -toiminnon, jos haluat tarkastella kirjattuja pankkitapahtumia. Pankkitapahtumasta löytyy sitä vastaava kirjattu pääkirjanpidon tapahtuma.

Jos haluat hakea kirjattujen talletusrivien kaikki pääkirjanpidon tapahtumat, siirry **KP-rekisteri** -sivulle ja käytä **Pääkirjanpito**-toimintoa. Sieltä löydät kaikki pääkirjanpidon tapahtumat, myös asiakkaiden ja toimittajien tapahtumat.

## <a name="reverse-a-posted-bank-deposit"></a>Kirjatun pankkitalletuksen peruuttaminen

Kirjatun pankkitalletuksen voi peruuttaa kahdella eri tavalla:

* Valitse **Kirjatut pankkitilitalletukset** -sivulla talletus ja valitse **Peruuta kirjaus** -toiminto.
* Siirry **KP-rekisterit** -sivulle, etsi talletuksen rekisteri ja valitse sitten **Peruuta rekisteri** -toiminto.

> [!NOTE]
> Voit peruuttaa vain yhden tapahtumatyypin sisältävän rekisterin. Rekisterissä täytyy siis olla vain asiakastapahtumia tai toimittajatapahtumia, mutta ei molempia. Jos rekisterissä on molempia, sinun täytyy manuaalisesti peruuttaa talletus.

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Financen määrittäminen](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]



