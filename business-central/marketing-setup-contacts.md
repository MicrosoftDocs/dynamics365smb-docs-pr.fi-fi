---
title: "Kontaktien tietojen määrittäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tehtävistä, joilla määritetään tietoja ja koodeja, kuten toimialaryhmiä ja liikesuhteita, ennen kontaktien määrittämistä."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Kontaktien määrittäminen
Voit syöttää kontaktien luomisen yhteydessä tietoja, kuten toimialan, johon kontaktin yritykset kuuluvat, sekä liikesuhteesi kontakteihin.

Ennen kontaktien luomista ja liikesuhteiden tietojen tallentamista on määritettävä koodit, joiden avulla tiedot liitetään kontaktin yrityksiin ja henkilöihin. Koodit voidaan määrittää postitusryhmille, toimialaryhmille, liikesuhteille, verkkolähteille, organisatorisille tasoille ja vastuualueille.

Kun nämä tiedot on määritetty, kontaktien luominen on organisoidumpaa ja kontaktien etsiminen tietyn ryhmän perusteella tehokkaampaa. Jokainen yrityksen ryhmä saa tiedot käyttöönsä, ja näin kontakteihin voi pitää yhteyttä tehokkaammin.

Kontaktien määrittäminen yhteydessä on määritettävä, millainen liikesuhde sinulla on eri kontaktien (esimerkiksi prospektin, pankin, konsultin tai palvelun toimittajan) kanssa. Lisätietoja on kohdassa [Liikesuhteiden määrittäminen kontaktiyrityksissä](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Toimialaryhmien määrittäminen kontaktiyrityksille
Toimialaryhmien avulla osoitetaan, minkä tyyppiseen toimialaryhmään (esimerkiksi vähittäistavarakauppa ja autoteollisuus) kontaktit kuuluvat.

Kontaktien toimialaryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään toimialaryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle toimialaryhmälle. Kun toimialaryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

> [!NOTE]  
>   Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

### <a name="to-define-an-industry-group-code"></a>Toimialaryhmän koodin määrittäminen
Toimialaryhmän koodi määrittää ryhmän tyypin tai luokan, joka voi olla esimerkiksi mainonnalle MAINOS tai televisiolle ja radiolle TIED.VÄL. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Toimialaryhmät**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimialaryhmät** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

### <a name="AssignIndustryGroupContact"></a> Toimialaryhmien määrittäminen kontaktille
Toimialaryhmiä ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Toimialaryhmät**-toiminto. Näyttöön tulee **Kontaktin toimialaryhmät** -sivu.
3. Valitse **Toimialaryhmien koodi** -kentässä toimialaryhmät, jotka haluat liittää.

Toista nämä vaiheet ja luo niin monta toimialaryhmää kuin haluat. Voit luoda samaan tapaan toimialaryhmiä kontaktiluettelosta.

Kontaktille määritettyjen toimialaryhmien lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Toimialaryhmien lkm** -kentässä.

Kun olet liittänyt toimialaryhmiä kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Kontaktien postitusryhmien määrittäminen
Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot. Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.

Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään postitusryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle. Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

### <a name="to-define-mailing-group-codes"></a>Postitusryhmän koodien määrittäminen
Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Postitusryhmät**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Postitusryhmät** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

### <a name="AssignMailGroupContact"></a> Postitusryhmien määrittäminen kontaktiin
1. Avaa kontakti.
2. Valitse **Postitusryhmät**-toiminto. Näyttöön tulee **Kontaktin postitusryhmät** -sivu.
3. Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.

Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat. Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.

Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-sivun **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.

Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Vaihtoehtoisten osoitteiden määrittäminen kontakteille
Voit liittää vaihtoehtoisen osoitteen (esimerkiksi kesämökin osoitteen), johon kontakteille joskus lähetetään postia ja tietoa. Voit määrittää myös vähintään yhden päivämäärävälin jokaiseen vaihtoehtoiseen osoitteeseen, jonka olet antanut kontakteillesi määrittämään, milloin osoite on voimassa.

### <a name="to-assign-an-alternate-address"></a>Vaihtoehtoisen osoitteen määrittäminen
1. Avaa kontakti.
2. Valitse **Vaihtoehtoinen osoite** -toiminto ja valitse sitten **Kortti**. **Kontaktin vaiht.eht.osoit.luet** -sivu avautuu.
3. Syötä uusi vaihtoehtoinen osoite ja täytä **Kontaktin vaihtoehtoinen osoite** -sivun kentät.

Toista nämä vaiheet ja määritä niin monta vaihtoehtoista osoitetta kuin haluat. Voit määrittää jokaiselle vaihtoehtoiselle osoitteelle vähintään yhden päivämäärävälin.

Voit liittää vaihtoehtoisia osoitteita myös kontaktiluettelosivulla noudattaen samaa menettelytapaa.

### <a name="to-assign-an-alternate-address-date-range"></a>Vaihtoehtoisten osoitteiden päivämäärävälien määrittäminen
1. Avaa kontakti.
2. Valitse ensin **Vaihtoehtoinen osoite** ja valitse sitten **Pvm-väli**. **Kontaktin vaih.eht.osoit.välit** -sivu avautuu.
3. Valitse **Uusi**-toiminto.
4. Valitse **Kont. vaiht.eht. osoitt. koodi** -kentässä tämän kontaktin vaihtoehtoinen osoite. Täytä sitten **Aloituspvm**- ja **Lopetuspvm**-kentät.

Toista nämä vaiheet ja luo niin monta päivämääräväliä kuin haluat.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Kontaktihenkilöiden vastuualueiden määrittäminen
Voit lisätä kontaktihenkilöiden vastuualueiden tietoja, kun haluat osoittaa, mistä kontaktihenkilö vastaa yrityksessä (esimerkiksi IT, hallinto tai tuotanto). Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien vastuualueiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään vastuualueen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle vastuualueelle. Kun vastuualueen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

### <a name="to-define-a-job-responsibility-code"></a>vastuualueen koodin määrittäminen
Vastuualueen koodi määrittää työn tyypin tai luokan. Se voi olla esimerkiksi MARKKINOINTI tai OSTO. Vastuualueen koodeja voi olla useita. Voit määrittää vastuualueen **Vastuualueet**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vastuualueet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Vastuualueiden määrittäminen kontaktihenkilöille
Et voi liittää vastuualueita kontaktiyrityksiin.

1. Avaa yhteyshenkilö.
2. Valitse **Henkilö**-toiminto ja valitse sitten **Vastuualueet**-toiminto. Näyttöön tulee **Kontaktin tehtäväalueet** -sivu.
3. Valitse **Vastuualueen koodi** -kentässä vastuualue, jonka haluat liittää.

Toista nämä vaiheet ja luo niin monta vastuualuetta kuin haluat. Voit liittää samaan tapaan vastuualueita myös kontaktiluettelosta.

Kontaktille liittämiesi vastuualueiden lukumäärä näkyy **Yhteyshenkilö**-sivun **Segmentointi**-osan **Vastuualueiden lkm** -kentässä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Kontaktihenkilöiden organisaatiotasojen määrittäminen
Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä. Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien organisaatiotasojen käyttäminen on kaksivaiheinen prosessi. Ensin määritetään organisaatiotason koodi. Tämä vaihe suoritetaan vain kerran jokaiselle organisaatiotasolle. Kun organisaation koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

### <a name="to-define-an-organizational-level-code"></a>Organisaatiotason koodin määrittäminen
Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA. Organisaatiotason koodeja voi olla useita. Voit määrittää organisaatiotason **Organisaatiotasot**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Organisaation tasot** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Organisaatiotasojen määrittäminen kontaktihenkilölle
Organisaatiotasoja voi liittää vain kontaktihenkilöihin, ei kontaktiyrityksiin. Jokaiseen kontaktiin voi liittää vain yhden organisatorisen tason.

1. Avaa kontakti.
2. Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.

Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Kontaktiyritysten verkkolähteiden määrittäminen
Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä. Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

Kontaktien verkkolähteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään verkkolähteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle verkkolähteelle. Kun verkkolähteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

### <a name="to-define-a-web-source-code"></a>Verkkolähteen koodin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **WWW-lähteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Koodi**-, **Kuvaus**- ja **URL**-kentät.

    Kirjoita %1 **URL-osoite**-kenttään lisätäksesi hakusanan paikkamerkin URL-osoitekenttään. Kun avaat verkkolähteen kontaktista, %1 korvataan hakusanalla (esimerkiksi yrityksen nimellä), jonka annoit **Kontaktin verkkolähteet** -sivulla.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Verkkolähteiden määrittäminen kontaktiyritykselle
Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto. Näyttöön tulee **Kontaktin verkkolähteet** -sivu.
3. Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.
4. Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

Voit liittää verkkolähteitä myös **Kontaktiluettelo**-sivulla noudattaen samaa menettelytapaa.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

