---
title: Kontaktien tietojen määrittäminen | Microsoft Docs
description: 'Tässä ohjeaiheessa kerrotaan tehtävistä, joilla määritetään tietoja ja koodeja, kuten toimialaryhmiä ja liikesuhteita, ennen kontaktien määrittämistä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Kontaktien määrittäminen
Voit antaa kontaktien luomisen yhteydessä tietoja, kuten toimialan, johon kontakti kuuluu, sekä liikesuhteesi kontakteihin.

Ennen kontaktien luomista ja liikesuhteiden tietojen tallentamista on määritettävä koodit, joiden avulla tiedot liitetään kontaktin yrityksiin ja henkilöihin. Koodit voidaan määrittää postitusryhmille, toimialaryhmille, liikesuhteille, verkkolähteille, organisatorisille tasoille ja vastuualueille. Voit määrittää nämä valitsemalla **Uusi**-toiminnon, kun valitse luetteloita kontaktikortissa.  

Kun nämä tiedot on määritetty, kontaktien luominen on organisoidumpaa ja kontaktien etsiminen tietyn ryhmän perusteella tehokkaampaa. Jokainen yrityksen ryhmä saa tiedot käyttöönsä, ja näin kontakteihin voi pitää yhteyttä tehokkaammin.

##  Toimialaryhmien määrittäminen kontaktille
Toimialaryhmien avulla osoitetaan, minkä tyyppiseen toimialaryhmään (esimerkiksi vähittäistavarakauppa ja autoteollisuus) kontaktit kuuluvat.

> [!NOTE]
> Tämä on mahdollista vain, kun kontaktin tyyppi on **Yritys**.

Toimialaryhmän koodi määrittää ryhmän tyypin tai luokan, joka voi olla esimerkiksi mainonnalle MAINOS tai televisiolle ja radiolle TIED.VÄL. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Toimialaryhmät**-sivun avulla.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Yritys**-toiminto ja sitten **Toimialaryhmät**-toiminto. Näyttöön tulee **Kontaktin toimialaryhmät** -sivu.
3. Valitse **Toimialaryhmien koodi** -kentässä toimialaryhmät, jotka haluat liittää.

Toista nämä vaiheet ja luo niin monta toimialaryhmää kuin haluat. Voit luoda samaan tapaan toimialaryhmiä kontaktiluettelosta.

Kontaktille määritettyjen toimialaryhmien lukumäärä näkyy **Kontaktin kortti** -sivun **Segmentointi**-osan **Toimialaryhmien lkm** -kentässä.

Kun olet liittänyt toimialaryhmiä kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

##  Postitusryhmien määrittäminen kontaktiin
Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot. Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.

Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Postitusryhmät**-sivun avulla.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Postitusryhmät**-toiminto. Näyttöön tulee **Kontaktin postitusryhmät** -sivu.
3. Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.

Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat. Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.

Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontaktin kortti** -sivun **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.

Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## Kontaktin vaihtoehtoisen osoitteen määrittäminen
Voit määrittää vaihtoehtoisen osoitteen (esimerkiksi kesämökin osoitteen), johon kontakti haluaa vastaanottaa joskus lähetetään postia ja tietoja. Voit määrittää myös vähintään yhden päivämäärävälin jokaiseen vaihtoehtoiseen osoitteeseen, jonka olet antanut kontakteillesi määrittämään, milloin osoite on voimassa.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Vaihtoehtoinen osoite** -toiminto ja valitse sitten **Kortti**-toiminto.

    Jos haluat määrittää, että vaihtoehtoista osoitetta käytetään tiettynä aikana, valitse sen sijaan **Päivämääräväli**-toiminto.
3. Anna **Kontaktin vaiht.eht.osoit.luet** -sivulla uusi vaihtoehtoinen osoite ja täytä **Kontaktin vaihtoehtoinen osoite** -sivun kentät.

Toista nämä vaiheet ja määritä niin monta vaihtoehtoista osoitetta kuin haluat. Voit määrittää jokaiselle vaihtoehtoiselle osoitteelle vähintään yhden päivämäärävälin.

## Vastuualueiden liittäminen kontakteihin:
Voit lisätä kontaktihenkilöiden vastuualueiden tietoja, kun haluat osoittaa, mistä kontaktihenkilö vastaa yrityksessä (esimerkiksi IT, hallinto tai tuotanto). Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

> [!NOTE]
> Tämä on mahdollista vain, kun kontaktin tyyppi on **Henkilö**.

Vastuualueen koodi määrittää työn tyypin tai luokan. Se voi olla esimerkiksi MARKKINOINTI tai OSTO. Vastuualueen koodeja voi olla useita. Voit määrittää vastuualueen **Vastuualueet**-sivulla.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Henkilö**-toiminto ja valitse sitten **Vastuualueet**-toiminto. Näyttöön tulee **Kontaktin tehtäväalueet** -sivu.
3. Valitse **Vastuualueen koodi** -kentässä vastuualue, jonka haluat liittää.

Toista nämä vaiheet ja luo niin monta vastuualuetta kuin haluat. Voit liittää samaan tapaan vastuualueita myös kontaktiluettelosta.

Kontaktille liittämiesi vastuualueiden lukumäärä näkyy **Yhteyshenkilö**-sivun **Segmentointi**-osan **Vastuualueiden lkm** -kentässä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## Organisaatiotasojen määrittäminen kontaktille
Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä. Voit käyttää näitä tietoja kontaktien tietojen antamiseen.

> [!NOTE]
> Tämä on mahdollista vain, kun kontaktin tyyppi on **Henkilö**.

Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA. Organisaatiotason koodeja voi olla useita. Voit määrittää organisaatiotason **Organisaatiotasot**-sivun avulla.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.

Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.

Kun olet määrittänyt vastuualueita kontakteille, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## Verkkolähteiden määrittäminen kontaktille
Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä. Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

> [!NOTE]
> Tämä on mahdollista vain, kun kontaktin tyyppi on **Yritys**.

Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto. Näyttöön tulee **Kontaktin verkkolähteet** -sivu.
3. Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.
4. Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

##  Liikesuhteiden määrittäminen kontaktille
Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.

> [!NOTE]
> Tämä on mahdollista vain, kun kontaktin tyyppi on **Yritys**.

1. Avaa haluamasi kontaktin kortti.
2. Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.
3. Valitse **Kontaktin liikesuhteet** -sivun **Liikesuhteen koodi** -kentässä määritettävä liikesuhde.

Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat.

Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.

Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## Tiettyjen tietojen kopioiminen automaattisesti kontaktiyrityksistä kontaktihenkilöille
Jotkin kontaktiyritysten tiedoista ovat samat kuin tämän yrityksen kontaktihenkilön tiedot, esimerkiksi osoitetiedot. Voit määrittää **Kontaktienhallinnan asetukset** -sivun **Periytyminen**-pikavälilehdessä, mitkä yrityksen kontaktikortin kentät kopioidaan henkilön kontaktikorttiin aina, kun luot kontaktiyritykseen kontaktihenkilön.

Kun muutat yhtä näistä kentistä kontaktiyrityksen kortissa, samat kentät päivitetään kontaktihenkilön kortissa, mikäli et ole manuaalisesti muuttanut kenttää kontaktihenkilön kortissa.

Lisätietoja on kohdassa [Kontaktien luominen](marketing-create-contact-companies.md).

## Ennalta määritettyjen oletusarvojen käyttäminen uusissa kontakteissa
Voit päättää, että sovellus liittää automaattisesti tietyn kielikoodin, territoriokoodin, myyjäkoodin ja maa-/aluekoodin oletusarvon jokaiseen luomaasi uuteen kontaktiin. Voit myös antaa myyntisyklin oletuskoodin, jonka sovellus sitten liittää jokaiseen luomaasi uuteen mahdollisuuteen. Tämä määritetään **Kontaktienhallinnan asetukset** -sivun **Oletusarvot**-pikavälilehdessä.

Kenttien periytyminen syrjäyttää määrittämäsi oletusarvot. Jos olet esimerkiksi määrittänyt englannin oletuskieleksi, mutta kontaktiyrityksen kieli on saksa, sovellus liittää automaattisesti saksan kielikoodin yrityksen kontaktihenkilölle.

## Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa
Kontaktin kortti voidaan synkronoida linkitetyn asiakkaan, toimittajan tai pankkitiliin kortin kanssa, kun täytät asianmukaisen kentän **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehden **Liikesuhteen koodi kohteelle** -osassa.  

Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

## Kontaktien kaksoiskappaleiden hakeminen
Voit valita, että sovellus hakee kaksoiskappaleita automaattisesti aina, kun luot kontaktin. Vaihtoehtoisesti voit valita, että haet kaksoiskappaleet manuaalisesti kontaktien luomisen jälkeen. Voit myös valita, että sovellus päivittää hakumerkkijonot automaattisesti aina, kun muutat kontaktin tietoja tai luot uuden kontaktin. Voit päättää Haun osuma-%:n, siis sen identtisten merkkijonojen prosenttiosuuden, joka kahdella kontaktilla täytyy olla, jotta sovellus tulkitsee ne kopioiksi. Tämä määritetään **Kontaktienhallinnan asetukset** -sivun **Kopiot**-pikavälilehdessä.

Jos löydät kontaktin kaksoiskappaleen, voit yhdistää sen säilytettävään kontaktitietueeseen **Yhdistä kaksoiskappale** -sivulla. Lisätietoja on kohdassa [Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md).

## Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Kontaktien luominen](marketing-create-contact-companies.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]