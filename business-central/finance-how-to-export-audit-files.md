---
title: Tarkistustiedoston vienti
description: 'Tässä artikkelissa kerrotaan, miten eri vientimuotoja määritetään ja miten niitä käytetään tilintarkastajan tai viranomaisen vaatimusten perusteella.'
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# Tarkistustiedoston vienti

Kirjanpitotietojen vieminen järjestelmästä on joidenkin paikallisten viranomaisten tai tilintarkastajien tavallinen pyyntö. Muotojen ja vaadittavien tietojen vienti voi vaihdella. Viennin tapahtumat ovat yleensä pääkirjanpidon (KP) tapahtumia tai arvonlisäverotapahtumia (ALV). Joskus tarvitaan kuitenkin muita tietoja.

**Valvontatiedostojen vienti** on esiasennettu laajennus, jonka avulla voit viedä eri tapahtumia, jotka perustuvat tilintarkastajan tai viranomaisen vaatimuksiin. Muotoilutyypistä tai kirjauksista huolimatta voit käyttää laajennuksen toimintoja tietojen viennin hallintaan. Toiminnoilla ei ole esiasennettua tiedostomuotoa vientiä varten. Tämän vuoksi sinun on joko asennettava sovellus, jolla on tietty muoto (esimerkiksi SIE, SAF-T tai FAC), tai kehitettävä oma sovellus.

> [!NOTE]
> Tällä hetkellä voit valita SIE- tai SAF-T-formaatin lisäsovelluksena. Kumppanit voivat myös kehittää mukautetun muodon. Käytettävissä olevien muotojen määrä kasvaa ajan mittaan.

## Määritä tarkistustiedoston vienti

1. Valitse hakupainikkeen ![Suurennuslasi-painike, joka avaa Kerro minulle -toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), kirjoita **Tarkistustiedoston viennin asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Seuraa **Tarkistustiedoston viennin asetukset** -sivulla seuraavia vaiheita:

    1. Valitse **Yleinen**-pikavälilehden **Tarkistustiedoston viennin muotokoodi** -kentässä tarkistustiedoston oletusvientimuodon koodi. Vain ne muotoilut, jotka otettiin käyttöön, kun tietty tiedostomuoto asennettiin ominaisuuksien hallinnasta, ja ne, jotka on lisätty mukautettuina muotoina, ovat käytettävissä.
    2. Valitse **tietojen laatu** -pikavälilehden **Tarkista yritystiedot** -valintaruutu, jos haluat ilmoituksen yrityksen tietokentistä, joita ei ole määritetty oikein.
    3. Valitse **Tarkista asiakas** -valintaruutu saadaksesi ilmoituksen kentistä, joita ei ole määritetty oikein tiettyjä asiakkaita varten.
    4. Valitse **Tarkista toimittaja** -valintaruutu saadaksesi ilmoituksen kentistä, joita ei ole määritetty oikein tiettyjä toimittajia varten.
    5. Valitse **Tarkista pankkitili** -valintaruutu saadaksesi ilmoituksen kentistä, joita ei ole määritetty oikein tiettyjä pankkitilejä varten.
    6. Valitse **Tarkista postinumero** -valinta ruutu, jos haluat ilmoituksen postinumerosta, jota ei ole määritetty oikein.
    7. Valitse **Tarkista osoite** -valintaruutu, jos haluat ilmoituksen, kun osoitetta ei ole määritetty oikein.
    8. Syötä **Oletuspostinumero**-kenttään postinumero, jota käytetään, jos asiakkaan tai toimittajan korttiin ei ole määritetty postinumeroa.

3. Valitse hakupainikkeen ![Suurennuslasi-painike, joka avaa Kerro minulle -toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), kirjoita **Tarkistustiedoston vientimuodon asetukset** ja valitse sitten aiheeseen liittyvä linkki.
4. Seuraa **Tarkistustiedoston vientimuodon asetukset** -sivulla seuraavia vaiheita:

    1. Valitse tarkistustiedoston vientimuoto, jonka haluat määrittää. Vain ne muotoilut, jotka otettiin käyttöön, kun tietty tiedostomuoto asennettiin ominaisuuksien hallinnasta, ja ne, jotka on lisätty mukautettuina muotoina, ovat käytettävissä.
    2. Kirjoita **Tarkistustiedoston nimi** -kenttään vietävän tarkistustiedoston oletustiedostonimi tai tiedostonimimalli.
    3. Valitse **Arkistoi zip-tiedostoon** -valintaruutu, jos haluat automaattisesti pakata viedyt tiedostot.

## Määritä tarkistustiedoston viennin KP-tilin yhdistämismääritys

Useimmat viranomaisten KP-tileiltä vaatimat muodot edellyttävät tiettyä vakiotilikarttaa. Sen jälkeen kun olet määrittänyt KP-tilit, viety tiedosto perustuu yhdistämismäärityksiin. Voit käyttää järjestelmässä useampia yhdistämismäärityksiä.

Seuraa näitä ohjeita määrittääksesi tarkistustiedoston viennin KP-tilin yhdistämismäärityksen.

1. Valitse hakupainikkeen ![Suurennuslasi-painike, joka avaa Kerro minulle -toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), kirjoita **KP-tilin yhdistämismääritys** ja valitse sitten aiheeseen liittyvä linkki.
2. Luo yhdistämismääritys **KP-yhdistämismääritys**-sivulla valitsemalla **Uusi**.
3. Määritä raportointijaksoa kuvaavan yhdistämismäärityksen koodi **Koodi**-kentässä.
4. Valitse **Vakiotilityyppi**-kentässä KP-tilien vakiotyyppi.
5. Valitse **Tarkistustiedoston vientimuoto** -kentässä tarkistustiedoston vientimuoto, johon tavalliset KP-tilit on linkitetty.
6. **Kauden tyyppi** -kentässä järjestelmä määrittää sen kirjanpitojakson tai mukautetun kausityypin, jolla on joustava aloituspäivämäärä ja -aika valintasi mukaan. Jos valitset tietyn kirjanpitojakson, kentän arvoksi tulee **kirjanpitojakso**. Muussa tapauksessa se on asetettu **tietoalueelle**.
7. Määrittele **Kirjanpitojakso**-kentässä kirjanpitojakson aloituspäivämäärä, jota käytetään raportointijaksona, jos haluat niiden olevan samat.
8. Jos määrität **kirjanpitojakso**-kentän, **Aloituspäivämäärä** -ja **Lopetuspäivämäärä**-kentät määritetään automaattisesti määrittämäsi jakson perusteella. Muussa tapauksessa voit määrittää raporteille aloitus- ja lopetuspäivämäärät manuaalisesti.
9. Jos olet jo lisännyt vakiotilikartan, toimi seuraavasti:

    1. Määritä **Vakiotilin luokan numero**  -kentässä yhdistämismäärityksessä käytettävän vakiotili- tai -ryhmittelykoodin luokan.
    2. Määritä **Vakiotilinumero**-kentässä yhdistämismäärityksessä käytettävä vakiotili- tai -ryhmittelykoodi.

10. Valitse **Sisällytä saapuva saldo** -valintaruutu ottaaksesi **Tasetilitili**-tyypin pääkirjatilin saapuvan saldon huomioon kartoituksessa raportointikauden nettomuutoksen sijaan.
11. Voit aloittaa yhdistämismäärityksen seuraavien vaiheiden avulla:

    1. Valitse **Alusta yhdistämismäärityksen lähde** luodaksesi rivejä **KP-tilin yhdistämismääritys** -sivulla aiemman tilikartan perusteella. Jos haluat kopioida KP-tilin määrityksen jostain muusta yhdistämismäärityskoodista, valitse **Kopioi toisesta yhdistämismäärityksestä**. Kun olet lopettanut rivien luomisen, kaikki kirjatut KP-tilit on merkitty vihreällä.
    2. Jos haluat merkitä vain KP-tilit, joilla on tapahtumia, valitse **Päivitä KP-tapahtumien saatavuus**. Jos **Sisällytä saapuva saldo** -asetus on käytössä, kaikki kirjatut KP-tapahtumat otetaan huomioon laskennassa. Muussa tapauksessa otetaan huomioon vain raportointikauden KP-tapahtumat.

## Vie tarkistustiedosto

1. Valitse hakupainikkeen ![Suurennuslasi-painike, joka avaa Kerro minulle -toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), kirjoita **Tarkistustiedoston viennin tiedostot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Tarkistustiedoston vientiasiakirjat** -sivulta **Uusi**.
3. Noudata **Yleinen**-pikavälilehdellä seuraavia vaiheita:

    1. Valitse **Tarkistustiedoston viennin muoto** -kentässä muoto, jota käytetään tarkistustiedoston viemiseen.
    2. Valitse **KP-tilin yhdistämismäärityskoodi** -kentässä raportointijakson KP-tilin yhdistämismäärityskoodi.
    3. Valitse **Jaa kuukausittain** -valintaruutu, jos kuukausittain luodaan useampia tarkistustiedostoja.
    4. Valitse **Jaa päivittäin** -valintaruutu, jos päivittäin luodaan useampia tarkistustiedostoja.
    5. Syötä **Otsikon kommentti** -kenttään kommentti, joka sisällytetään tarkistustiedoston otsikkoon.
    6. Määritä **Yhteyshenkilö**-kentässä tarkistustiedoston otsikkoon viety yhteystieto.
    7. Luo useita zip-tiedostoja valitsemalla **Luo useita zip-tiedostoja** -valintaruutu.

        > [!IMPORTANT]
        > Valitse tämä valintaruutu vain, jos olet aiemmin asentanut joitain muotoilusovelluksia tai luonut mukautetun mallin. Yhden tai useamman tietyn muodon asentaminen lisää kenttiä ja toimintoja **tarkistustiedostojen tuonti** -toimintoon, joka perustuu muotovaatimuksiin.

4. Noudata **Käsittely**-pikavälilehdellä seuraavia vaiheita:

    1. Valitse **rinnakkainen käsittely** -valintaruutu, jos haluat, että tarkistustiedoston luonti suoritetaan rinnakkain taustatöiden kanssa. Poista valintaruudun valinta, jos haluat viedä tiedot käynnissä olevaan istuntoon.
    2. Jos valitsit **Rinnakkainen käsitteleminen** -valintaruudun, määritä **Töiden enimmäismäärä** -kentässä kerralla suoritettaville taustaprojekteille enimmäismäärä.
    3. Määritä **varhaisin alkamispäivä/-aika** -kentässä aikaisin päivämäärä ja aika, jolloin taustatyö tulee ajaa. Jos suoritat prosessin valitsemalla **Käynnistä**, voit seurata **käsittely**- ja **rivit**-pikavälilehtien tilaa.

5. Kun olet valmis, lataa valitulle riville tarkistustiedosto valitsemalla **Lataa tiedostona**.

> [!IMPORTANT]
> Jos viet useampia tapahtumia, Microsoft ei suosittele niiden viemistä käynnissä olevaan istuntoon mahdollisten suorituskykyongelmien vuoksi. Sen sijaan on suositeltavaa käyttää rinnakkaista käsittelyaikaa muiden kuin työpäivien tai -tuntien aikana.

## Katso myös
[Taloushallinto](finance.md)  
[Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md)  
[Dimensioiden käsitteleminen](finance-dimensions.md)  
[Business Centralin käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
