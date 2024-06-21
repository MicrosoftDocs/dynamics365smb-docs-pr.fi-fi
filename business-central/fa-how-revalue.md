---
title: Käyttöomaisuuden uudelleenarvostus
description: 'Tietoja käyttöomaisuuden arvoa muuttamisesta, uusien summien kirjaamisesta arvonalennuksiksi tai -korotuksiksi sekä muiden hankintakustannusten kirjaamisesta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5628, 5629, 5633'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="revalue-fixed-assets"></a>Käyttöomaisuuden uudelleenarvostus

Käyttöomaisuuserien uudelleenarvostus voi koostua arvonkorotuksista, arvonalennuksista tai yleisistä arvon oikaisuista.

Kun käyttöomaisuuserän arvo kasvaa, voit kirjata päiväkirjariville arvonkorotuksen poistokirjaan. Uusi summa kirjataan arvonkorotuksena käyttöomaisuuden kirjausasetusten mukaan.

Kun käyttöomaisuuden arvo pienenee, voit kirjata päiväkirjariville alhaisemman summan, arvonalennuksen, poistokirjaan. Uusi summa tallennetaan arvonalennuksena käyttöomaisuuden kirjausasetusten mukaan.

Indeksointia käytetään muuttamaan useiden käyttöomaisuuserien arvoja esimerkiksi yleisten hintatason muutosten mukaan. **Tee indeksimuutos KO:teen** -eräajon avulla voi muuttaa erilaisia summia, kuten arvonalennus- ja arvonkorotussummia.

## <a name="to-post-appreciation-from-the-fixed-asset-gl-journal"></a>Arvonkorotuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.
3. Valitse **KO:n kirjaustyyppi** -kentässä **Uudelleenarvostus**.
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty arvonkorotuksen kirjaamista varten.

    > [!NOTE]  
    >   Vaihe 4 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Arvonkorotustili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Arvonkorotuksen vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle arvonkorotuksen vastatilitapahtumat kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valitse **Kirjaa**-toiminto.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>Arvonalennuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.
3. Valitse **KO:n kirjaustyyppi** -kentässä **Arvonalennus**.
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty arvonalennuksen kirjaamista varten.

    > [!NOTE]  
    >   Vaihe 4 toimii vain, jos määritettynä ovat seuraavat arvot: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Arvonalennustili**-kenttä sisältää pääkirjanpidon kredit-tilin ja **Arvonalennuksen kustannustili** -kenttä sisältää sen pääkirjanpitotilin, jolle arvonalennusten vastatilitapahtumat kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Valitse **Kirjaa**-toiminto.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>Käyttöomaisuuden yleisen uudelleenarvostuksen suorittaminen

Indeksointia käytetään muuttamaan useiden käyttöomaisuuserien arvoja esimerkiksi yleisten hintatason muutosten mukaan. **Tee indeksimuutos KO:teen** -eräajon avulla voi muuttaa erilaisia summia, kuten arvonalennus- ja arvonkorotussummia. **Salli indeksimuutokset** -valintaruudun on oltava valittuna **Poistokirja**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tee indeksimuutos KO:teen** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.
3. Valitse **OK**-painike.

    Uudelleenarvostuksen rivit luodaan vaiheessa 2 tehtyjen asetusten mukaan. Rivit luodaan joko käyttöomaisuuden päiväkirjassa tai käyttöomaisuuden KP-päiväkirjassa **KO-päiväkirjan asetukset** -sivun mallin ja erän asetusten mukaan. Lisätietoja on kohdassa [Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  
5. Valitse päiväkirja, joka sisältää uudelleenarvostettavat käyttöomaisuuserät, ja valitse sitten **Tapahtumakirjaukset**-toiminto.  
6. Tarkista luodut tapahtumat ja kirjaa päiväkirja **Kirjaa**-toiminnon avulla.

    > [!TIP]  
    >   Jos indeksiluvut on tarkoitettu vain simulointia varten, niiden tallentamiseksi voi luoda erityisen poistokirjan. Tällä tavalla tapahtumat eivät vaikuta muihin poistokirjoihin.

## <a name="to-post-other-acquisition-costs"></a>Muiden hankintakustannusten kirjaaminen

Käyttöomaisuuden muut hankintamenot kirjataan ostolaskusta tai käyttöomaisuuden päiväkirjasta samalla tavalla kuin alkuperäinen hankintameno. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).  

Jos käyttöomaisuudelle on jo laskettu poisto, valitse **Poiston hankintameno** -valintaruutu tehdäksesi poiston muille hankintamenoille vähennettynä jäännösarvolla samassa suhteessa kuin aiemmin hankitulle käyttöomaisuudelle tehty poisto. Tämä menetelmä varmistaa, ettei poistojaksoa muuteta.  

Poistoprosentti lasketaan seuraavasti:  

*PR = (kokonaispoisto x 100) / poistopohja*

*Poistosumma = (PR/100) x (lisähankintameno - jäännösarvo)*  

Muista valita laskun käyttöomaisuuden KO-päiväkirjan tai päiväkirjarivien **Poisto KO-kirjauspvm:ään asti** -valintaruutu varmistuaksesi siitä, että poisto lasketaan viimeisestä käyttöomaisuuden kirjauspäivämäärästä muiden hankintamenojen kirjauspäivämäärään asti.

### <a name="example---posting-other-acquisition-costs"></a>Esimerkki – muiden hankintamenojen kirjaaminen

Kone ostetaan elokuun 1. päivä 2000. Hankintameno on 4 800. Poistomenetelmä on tasapoisto neljän vuoden ajalta.

**Laske poisto** -eräajo suoritetaan 31. elokuuta 2000. Poisto lasketaan seuraavasti:

*kirjanpitoarvo x poistopäivien lukumäärä / poistopäivien kokonaismäärä = 4 800 x 30 / 1 440 = 100*  

syyskuuta 2000 kirjataan lasku koneen maalaamisesta. Laskusumma on 480.

Jos valitsit laskun **Poisto KO-kirjauspvm:ään asti** -valintaruudun ennen kirjausta, suoritetaan seuraava laskenta:  

15 poistopäivää (01.09.00–15.09.00) lasketaan seuraavasti:

*kirjanpitoarvo x poistopäivien lukumäärä / jäljellä olevien poistopäivien lukumäärä = (4 800 - 100) x 15 / 1 410 = 50*

Jos valitsit laskun **Poiston hankintameno** -valintaruudun ennen kirjausta, suoritetaan seuraava laskenta:  

*Muu hankintameno poistetaan seuraavasti: ((150 x 100) / 4 800) / 100 x 480 = 15*

Poistopohja on nyt *5 280 = (4 800 + 480)*, ja kumulatiivinen poisto on *165 = (100 + 50 + 15)*, joka vastaa kokonaishankintamenon 45 poistopäivää. Tämä laskelma tarkoittaa sitä, että käyttöomaisuuserälle tehdään kokonaispoisto arvioidun neljän vuoden elinkaaren aikana.  

Kun **Laske poisto** -eräajo suoritetaan 30.09.00, käytetään seuraavaa laskentaa:  

*Jäljellä oleva poistoaika on 3 vuotta, 10 kuukautta ja 15 päivää = 1 395 päivää*  

*Kirjanpitoarvo on (5280 - 165) = 5115*  

*Poistosumma syyskuulle 2000: 5 115 x 15 / 1 395 = 55,00*  

*Kokonaispoisto = 165 + 55 = 220*  

Jos et valinnut **Poisto KO-kirjauspvm:ään asti** -valintaruutua, omaisuuserä menettää 15 poistopäivää, koska 30.9.2000 suoritettu **Laske poisto** -eräajo laskisi poiston 15.9.2000 ja 30.9.2000 väliseltä ajalta. Tämä tarkoittaa sitä, että kun **Laske poisto** -eräajo suoritetaan 30.09.00, laskenta tehdään seuraavasti:  

*Jäljellä oleva ikä on 3 vuotta, 10 kuukautta ja 15 päivää = 1 395 päivää*  

*Kirjanpitoarvo on (4800 + 480 - 100 - 15) = 5165*

*Poistosumma syyskuulle 2000: 5 165 x 15 / 1 395 = 55,54*  

*Kokonaispoisto = 100 + 15 + 55,54 = 170,54*

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
