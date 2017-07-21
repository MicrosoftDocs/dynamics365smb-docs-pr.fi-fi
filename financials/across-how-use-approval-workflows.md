---
title: "Hyväksy tai hylkää asiakirjoja työnkuluissa| Microsoft Docs"
description: "Pyydä, hylkää tai delegoi esimerkiksi osto- tai myyntiasiakirjan hyväksyntä työnkulun osana."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ffeffe725025dc03d2053333f75249679103b6a4
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-approval-workflows"></a>Toimintaohje: Hyväksyntätyönkulkujen käyttäminen
Jos organisaatiosi henkilön pitää hyväksyä tietue, kuten ostoasiakirja tai asiakaskortti, hänelle lähetetään hyväksyntäpyyntö työnkulun osana. Hyväksyjä saa työnkulun määrityksen mukaan ilmoituksen siitä, että tietue odottaa hänen hyväksyntäänsä.

Hyväksyntätyönkulut määritetään **Työnkulku**-ikkunassa.

Ostoasiakirjojen, myyntiasiakirjojen, maksupäiväkirjojen, asiakaskorttien ja nimikekorttien perushyväksyntätyönkulut ovat valmiita käynnistettäväksi avustetuissa asennuksissa. Lisätietoja on kohdassa [Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin(index.md).

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Tietueen hyväksynnän pyytäminen
Hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

1. Valitse tietueen ikkunassa **Lähetä hyväksymispyyntö** -toiminto.
2. Kun haluat nähdä kaikki hyväksymispyynnöt, valitse ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Hyväksymispyyntötapahtumat** ja valitse liittyvä linkki.  

Hyväksyntämerkinnän tila muuttuu **Luotu** -tilasta**Avoin**-tilaksi. Tietueen, kuten esimerkiksi ostolaskun, tila päivitetään **Avoin**-tilasta **Odottaa hyväksyntää** -tilaksi. Tietue pysyy lukittuna käsittelyltä, kunnes hyväksyjät ovat hyväksyneet tietueen.

Kun hyväksyjä on hyväksynyt tietueen, sen tilaksi muuttuu **Vapautettu**. Tämän jälkeen voit jatkaa tietueeseen liittyviä tehtäviä.

## <a name="to-cancel-requests-for-approval"></a>Hyväksymispyyntöjen peruuttaminen
Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Tilanne voi toisinaan edellyttää, että asiakkaan täytyy tehdä muutoksia tilaukseen, joka on lähetetty hyväksyttäväksi. Tällöin voit peruuttaa hyväksyntäprosessin ja tehdä tarvittavat muutokset tilaukseen, ennen kuin pyydät hyväksyntää uudelleen.

- Valitse tietueen näyttävässä ikkunassa **Peruuta hyväksymispyyntö** -toiminto.

Kun hyväksyntäpyyntö on peruutettu, siihen liittyvän hyväksyntämerkinnän tilaksi tulee **Peruutettu**. Tietueen tila muuttuu **Odottaa hyväksyntää** -tilasta**Avoin**-tilaksi. Tämän jälkeen hyväksyntäprosessi voi alkaa uudelleen.

## <a name="to-make-minor-changes-to-approved-records"></a>Pienten muutosten tekeminen hyväksyttyihin tietueisiin
Jos haluat tehdä tietueeseen pienen muutoksen hyväksymisen jälkeen, voit avata tietueen uudelleen, tehdä haluamasi muutoksen ja vapauttaa sitten tietueen. Tee pienet muutokset **Avaa uudelleen**- ja **Vapauta**-painikkeiden avulla.

1. Avaa tietueen, kuten ostolaskun, sisältävä ikkuna ja valitse sitten **Avaa uudelleen** -toiminto.

    **Asiakirjan tila** -kentän arvoksi muuttuu **Avoin**.
2. Tee tietueeseen tarvittavat muutokset (esimerkiksi toimittajan osoite).
3. Valitse **Vapauta**-toiminto.

Kun avaat lähdetiedoston uudelleen, siihen liittyvän hyväksyntämerkinnän tila on edelleen Hyväksytty **Hyväksymistapahtumat**-ikkunassa.

## <a name="to-approve-or-reject-requests-for-approval"></a>Hyväksymispyyntöjen hyväksyminen tai hylkääminen
Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Voit käsitellä hyväksymispyynnöt **Hyväksyttävät pyynnöt** -ikkunassa esimerkiksi silloin, kun haluat hyväksyä kerralla useita pyyntöjä. Vaihtoehtoisesti voit käsitellä liittyvän tietueen, kuten **Ostolasku**-ikkunan, jokaisen pyynnön valitsemalla vastaanottamasi ilmoituksen linkin.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Hyväksyttävät pyynnöt** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse yksi tai useampi rivi tietueesta tai tietueista, jonka haluat hyväksyä tai hylätä.
3. Valitse **Hyväksy**-, **Hylkää**- tai **Delegoi**-toiminto.

Kun tietue on hyväksytty tai hylätty, hyväksynnän **Tila**-kentän arvoksi muutetaan **Hyväksytty** tai **Hylätty**.

Jos hyväksyjähierarkia on määritelty, tietueen tilaksi määritellään **Odottaa hyväksyntää** siihen asti, että kaikki hyväksyjät ovat hyväksyneet tietueen. Tietueen tilaksi tulee tämän jälkeen **Vapautettu**.

Hyväksynnän tila muuttuu samanaikaisesti **Luodusta** **Avoimeksi** heti, kun tietueelle luodaan hyväksymispyyntö. Jos pyyntö hylätään, hyväksynnän tilaksi muutetaan **Hylätty**. Tila pysyy **Avoimena** tai **Hylättynä** kunnes kaikki hyväksyjät ovat hyväksyneet pyynnön.

## <a name="to-delegate-requests-for-approval"></a>Hyväksymispyyntöjen delegoiminen
Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Työnkulun tukkiutumisen tai asiakirjojen kasaantumisen estämiseksi hyväksyjä ja hyväksynnän valvoja voi delegoida hyväksymispyynnöt sijaiselle. Korvaava voi olla joko nimetty korvaaja, suora hyväksyjä tai hyväksynnän järjestelmänvalvoja, tässä järjestyksessä. Tätä toimintoa käytetään yleensä, kun alkuperäinen hyväksyjä on poissa töistä eikä pysty käsittelemään pyyntöjä ennen eräpäivää.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Hyväksyttävät pyynnöt** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse vähintään yksi pyyntörivi, jonka haluat delegoida sijaiselle, ja valitse sitten **Delegoi**-toiminto.

Ilmoitus hyväksyttävästä pyynnöstä lähetetään sijaiselle.

## <a name="to-manage-overdue-approval-requests"></a>Myöhässä olevien hyväksymispyyntöjen hallinta
Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Hyväksynnän työnkulun käyttäjiä on muistutettava säännöllisin väliajoin myöhässä olevista hyväksyntäpyynnöistä, joihin heidän pitäisi reagoida. Tähän käytetään **Lähetä ilmoituksia myöhässä olevista hyväksynnöistä** -toimintoa.

**Lähetä ilmoituksia myöhässä olevista hyväksynnöistä** -toiminto tarkistaa kaikki avoimet myöhässä olevat hyväksyntäpyynnöt. Toiminto lähettää luettelon kaikista myöhässä olevista hyväksynnöistä jokaiselle hyväksyjälle, jolla on vähintään yksi myöhässä oleva hyväksyntämerkintä. Ilmoitus lähetetään myös hyväksyjän esimiehelle ja kaikille myöhässä olevien hyväksyntöjen pyytäjille. Tästä on apua, jos hyväksyntä on siirrettävä sijaiselle.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Erääntyneiden hyväksymispyyntöjen työnkulku** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Myöhässä olevat hyväksyntäpyynnöt** -ikkunassa **Lähetä erääntyneiden hyväksyntöjen ilmoitukset** -toiminto.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)    
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen(ui-work-product.md)

