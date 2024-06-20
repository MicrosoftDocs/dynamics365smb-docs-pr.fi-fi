---
title: Digitaalisten tositteiden määrittäminen
description: 'Tässä artikkelissa kerrotaan, kuinka pakotettuja digitaalisia tositteita määritetään ja käytetään Microsoft Dynamics 365 Business Centralissa.'
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
ms.reviewer: bholtorf
---

# Digitaalisten tositteiden määrittäminen

Järjestelmänvalvojat voivat käyttää digitaalisia tositetoimintoja vaatiakseen, että asiakirjat liitetään tiettyihin tapahtumiin, kun ne kirjataan. Siksi tämä toiminto mahdollistaa lähdelähtöisen lähestymistavan ja tarjoaa paremman kirjausketjun. Tätä tarkoitusta varten voidaan konfiguroida eri tyyppisiä täytäntöönpanotoimia tositteiden tai lokityyppien mukaan.

Termi *digitaalinen tosite* viittaa perinteisen kirjanpidon tositteen digitaaliseen tai sähköiseen muotoon. Tosite on asiakirja, jota käytetään rahoitustapahtumien tukemiseen ja valtuutukseen. Kirjanpidossa tosite toimii tyypillisesti todisteena kulusta tai varojen vastaanottamisesta. Tosite voi sisältää tietoja, kuten tapahtuman päivämäärän, kuvauksen, summan ja mahdolliset valtuutusallekirjoitukset.

> [!IMPORTANT]
> Joissakin maissa ja joillakin alueilla joidenkin asetusten määrittäminen saattaa olla rajoitettua, koska lakisääteiset vaatimukset saattavat edellyttää tiettyjä asetuksia. Jos kohtaat näitä rajoituksia, etsi yksityiskohtaista selitystä maasi tai alueesi dokumentaatiosivulta.

## Digitaalisten tositteiden käyttöönotto

Ota digitaalinen tositetoiminto käyttöön noudattamalla näitä ohjeita.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Digitaalisten tositteiden asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Käytössä**-valintaruutu.

## Digitaalisten tositteiden määrittäminen

Voit käyttää erilaisia ​​asetuksia seuraaville asiakirjoille ja päiväkirjoille.

| Tapahtuman tyyppi | Kuvaus |
|------------|-------------|
| Myyntiasiakirja | Määrittää kirjaukset, jotka täydennetään myyntitositteista. |
| Ostoasiakirja | Määrittää kirjaukset, jotka täydennetään ostoasiakirjoista. |
| Yleinen päiväkirja | Määrittää kirjaukset, jotka suoritetaan yleisestä päiväkirjasta kaikille tilityypeille paitsi niille, jotka liittyvät asiakkaaseen ja toimittajaan. Jos valitset jonkin näistä tilityypeistä, muutat kirjausprosessin hallintaa. Jos valitset tilityypiksi **Asiakas**, järjestelmä tarkistaa myyntipäiväkirjaan liittyvät asetukset. Jos valitset tilityypiksi **Toimittaja**, järjestelmä tarkistaa ostopäiväkirjaan liittyvät asetukset. |
| Myyntipäiväkirja | Määrittää kirjaukset, jotka suoritetaan myyntipäiväkirjasta ja yleisestä päiväkirjasta, joissa **Asiakas** on valittu tilityypiksi. |
| Ostopäiväkirja | Määrittää kirjaukset, jotka suoritetaan ostopäiväkirjasta ja yleisestä päiväkirjasta, joissa **Toimittaja** on valittu tilityypiksi. |

Seuraa näitä ohjeita määrittääksesi, kuinka organisaatiosi käyttää pakotettuja digitaalisia tositteita.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Digitaalisten tositteiden tapahtumien asetukset** ja valitse sitten vastaava linkki. Vaihtoehtoisesti valitse **Digitaalisen tositteen asetukset** -sivulla **Tapahtuman asetukset**.
2. Valitse **Tapahtumatyyppi**-sarakkeessa vaihtoehto.
3. Valitse **Tarkistustyyppi**-sarakkeessa toimeenpanovaihtoehto. Jos valitset **Ei mitään**, voit lähettää valitun merkinnän ilman digitaalista tositetta. Jos valitset **Liite**, tapahtumassa on oltava liite. Jos valitset **Liite tai huomautus**, voit liittää tapahtumaan liitteen tai huomautuksen. 
4. Valitse **Luo automaattisesti** -valintaruutu luodaksesi digitaalisen tositteen automaattisesti. Jos et esimerkiksi halua lisätä tapahtumaasi manuaalisesti myyntilaskua, valitse tämä valintaruutu. Sitten sinun tarvitsee vain lähettää asiakirja. Järjestelmä luo asiakirjan automaattisesti raportin asettelun perusteella ja liittää sen tapahtumaan.
5. Valitse **Ohita, jos lisätty manuaalisesti** -valintaruutu, jos et halua lisätä automaattisesti luotua digitaalista tositetta, jos käyttäjä on jo lisännyt manuaalisen liitteen.

### Käytä asennuksessa lähdekoodeja

Jos haluat käyttää valvontaa päiväkirjoille, mutta ei kaikille tapahtumatyypeille, yhdistä tietty lähdekoodi merkintätyypin tunnistamiseksi yleiseksi päiväkirjaksi, myyntipäiväkirjaksi tai ostopäiväkirjaksi.

Seuraa näitä vaiheita, jotta voit luoda digitaalisten tositteiden erityisiä lähdekoodeja.

1. Vaihtoehtoisesti valitse **Digitaalisen tositteen tapahtuman asetukset** -sivulla **Lähdekoodit**.
2. Valitse **Tositteen lähdekoodit** -sivulla lähdekoodit, jotka haluat määrittää.
3. Sulje sivu.

## Käytä toimintoa

Avaa osto- tai myyntitosite ja kirjoita tiedot vaadittuihin kenttiin. Ennen kuin lähetät asiakirjan, sinun on liitettävä digitaalinen tosite noudattamalla näitä ohjeita.

1. Valitse **Saapuvat asiakirjatiedostot** -FactBoxissa **Liitä tiedosto**.
2. Vedä tiedosto suoraan **Lisää tiedosto** -sivulle tai selaa tiedostoa tältä sivulta.

Tiedosto liitetään **saapuvat asiakirjatiedostot** -FactBoxiin. Jokaiselta riviltä löydät asiakirjan nimen ja tyypin.

Jos liität vahingossa väärän tositteen, poista se näiden ohjeiden mukaisesti ennen asiakirjan lähettämistä.

1. Valitse **Saapuvat asiakirjatiedostot** -FactBoxista asiakirjariviltä **Saapuva asiakirja**.
2. Valitse **Saapuva asiakirja** -sivulla **Poista**.

> [!NOTE]
> Jos digitaalisen tositteen liittäminen on määritetty pakolliseksi ja yrität kirjata asiakirjoja tai päiväkirjoja liittämättä tositteita, järjestelmä estää kirjaamisen. Näyttöön tulee seuraava virhesanoma: "Ei ole mahdollista lähettää liittämättä digitaalista tositetta."

### Etsi liitetyt tositteet tapahtumista

Löydät liitteenä olevan tositteen lähetetystä asiakirjasta tai **Pääkirjan merkinnät** -sivulta katsomalla **Saapuvat tositetiedostot** -FactBoxista.

Et voi poistaa liitettyä asiakirjaa, kun lähetys on valmis. Voit kuitenkin lisätä liitteitä, kun lähetys on valmis.

## Katso myös

[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
