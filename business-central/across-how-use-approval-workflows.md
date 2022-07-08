---
title: Hyväksy tai hylkää asiakirjoja työnkuluissa| Microsoft Docs
description: Pyydä, hylkää tai delegoi esimerkiksi osto- tai myyntiasiakirjan hyväksyntä työnkulun osana.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: 46c81fa887af70e7a2f516df38ec003392b1dabd
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079348"
---
# <a name="use-approval-workflows"></a>Hyväksymistyönkulkujen käyttäminen

Jos organisaatiosi henkilön pitää hyväksyä tietue, kuten ostoasiakirja tai asiakaskortti, hänelle lähetetään hyväksyntäpyyntö työnkulun osana. Hyväksyjä saa työnkulun määrityksen mukaan ilmoituksen siitä, että tietue odottaa hänen hyväksyntäänsä.

Hyväksyntätyönkulut määritetään **Työnkulku**-sivulla. Hyväksynnän käyttäjät, mukaan lukien mahdolliset asianmukaiset summan rajoitukset, täytyy määrittää **Hyväksynnän käyttäjäasetukset** -sivulla. Lisätietoja on kohdassa [Työnkulkujen määrittäminen](across-set-up-workflows.md).  

Tässä ohjeaiheessa kuvattujen hyväksyntätyönkulkujen lisäksi voit suorittaa useita muita työnkulun tehtäviä. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).

Ostoasiakirjojen, myyntiasiakirjojen, maksupäiväkirjojen, asiakaskorttien ja nimikekorttien perushyväksyntätyönkulut ovat valmiita käynnistettäväksi oppaina. Lisätietoja on kohdassa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>Tietueen hyväksynnän pyytäminen

Hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

1. Valitse tietueen sivulla **Lähetä hyväksymispyyntö** -toiminto.
2. Kaikki hyväksymispyynnöt nähdäksesi valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksymispyyntötapahtumat** ja valitse sitten vastaava linkki.  

Hyväksyntämerkinnän tila muuttuu **Luotu** -tilasta **Avoin**-tilaksi. Tietueen, kuten esimerkiksi ostolaskun, tila päivitetään **Avoin**-tilasta **Odottaa hyväksyntää** -tilaksi. Tietue pysyy lukittuna käsittelyltä, kunnes hyväksyjät ovat hyväksyneet tietueen.

Kun hyväksyjä on hyväksynyt tietueen, sen tilaksi muuttuu **Vapautettu**. Tämän jälkeen voit jatkaa tietueeseen liittyviä tehtäviä.

## <a name="to-cancel-requests-for-approval"></a>Hyväksymispyyntöjen peruuttaminen

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Tilanne voi toisinaan edellyttää, että asiakkaan täytyy tehdä muutoksia tilaukseen, joka on lähetetty hyväksyttäväksi. Tällöin voit peruuttaa hyväksyntäprosessin ja tehdä tarvittavat muutokset tilaukseen, ennen kuin pyydät hyväksyntää uudelleen.

- Valitse tietueen näyttävällä sivulla **Peruuta hyväksymispyyntö** -toiminto.

Kun hyväksyntäpyyntö on peruutettu, siihen liittyvän hyväksyntämerkinnän tilaksi tulee **Peruutettu**. Tietueen tila muuttuu **Odottaa hyväksyntää** -tilasta **Avoin**-tilaksi. Tämän jälkeen hyväksyntäprosessi voi alkaa uudelleen.

## <a name="to-approve-or-reject-requests-for-approval"></a>Hyväksymispyyntöjen hyväksyminen tai hylkääminen

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Voit käsitellä hyväksymispyynnöt **Hyväksyttävät pyynnöt** -sivulla esimerkiksi silloin, kun haluat hyväksyä kerralla useita pyyntöjä. Vaihtoehtoisesti voit käsitellä liittyvän tietueen, kuten **Ostolasku**-sivun, jokaisen pyynnön valitsemalla vastaanottamasi ilmoituksen linkin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksyttävät pyynnöt** ja valitse sitten vastaava linkki.
2. Valitse yksi tai useampi rivi tietueesta tai tietueista, jonka haluat hyväksyä tai hylätä.
3. Valitse **Hyväksy**-, **Hylkää**- tai **Delegoi**-toiminto.

Kun tietue on hyväksytty tai hylätty, hyväksynnän **Tila**-kentän arvoksi muutetaan **Hyväksytty** tai **Hylätty**.

Jos hyväksyjähierarkia on määritelty, tietueen tilaksi määritellään **Odottaa hyväksyntää** siihen asti, että kaikki hyväksyjät ovat hyväksyneet tietueen. Tietueen tilaksi tulee tämän jälkeen **Vapautettu**.

Hyväksynnän tila muuttuu samanaikaisesti **Luodusta** **Avoimeksi** heti, kun tietueelle luodaan hyväksymispyyntö. Jos pyyntö hylätään, hyväksynnän tilaksi muutetaan **Hylätty**. Tila pysyy **Avoimena** tai **Hylättynä** kunnes kaikki hyväksyjät ovat hyväksyneet pyynnön.

## <a name="to-delegate-requests-for-approval"></a>Hyväksymispyyntöjen delegoiminen

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Työnkulun tukkiutumisen tai asiakirjojen kasaantumisen estämiseksi hyväksyjä ja hyväksynnän valvoja voi delegoida hyväksymispyynnöt sijaiselle. Korvaava voi olla joko nimetty korvaaja, suora hyväksyjä tai hyväksynnän järjestelmänvalvoja, tässä järjestyksessä. Tätä toimintoa käytetään yleensä, kun alkuperäinen hyväksyjä on poissa töistä eikä pysty käsittelemään pyyntöjä ennen eräpäivää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksyttävät pyynnöt** ja valitse sitten vastaava linkki.
2. Valitse vähintään yksi pyyntörivi, jonka haluat delegoida sijaiselle, ja valitse sitten **Delegoi**-toiminto.

Ilmoitus hyväksyttävästä pyynnöstä lähetetään sijaiselle.

## <a name="to-manage-overdue-approval-requests"></a>Myöhässä olevien hyväksymispyyntöjen hallinta

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Hyväksynnän työnkulun käyttäjiä on muistutettava säännöllisin väliajoin myöhässä olevista hyväksyntäpyynnöistä, joihin heidän pitäisi reagoida. Tähän käytetään **Lähetä ilmoituksia myöhässä olevista hyväksynnöistä** -toimintoa.

**Lähetä ilmoituksia myöhässä olevista hyväksynnöistä** -toiminto tarkistaa kaikki avoimet myöhässä olevat hyväksyntäpyynnöt. Toiminto lähettää luettelon kaikista myöhässä olevista hyväksynnöistä jokaiselle hyväksyjälle, jolla on vähintään yksi myöhässä oleva hyväksyntämerkintä. Ilmoitus lähetetään myös hyväksyjän esimiehelle ja kaikille myöhässä olevien hyväksyntöjen pyytäjille. Tästä on apua, jos hyväksyntä on siirrettävä sijaiselle.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Erääntyneet hyväksymispyynnöt** ja valitse sitten vastaava linkki.
2. Valitse **Myöhässä olevat hyväksyntäpyynnöt** -sivulla **Lähetä erääntyneiden hyväksyntöjen ilmoitukset** -toiminto.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/use-approval-workflows/)

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Myynti](sales-manage-sales.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]