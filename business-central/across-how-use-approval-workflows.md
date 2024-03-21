---
title: Asiakirjojen hyväksyminen tai hylkääminen työnkuluissa
description: 'Pyydä, hylkää tai delegoi esimerkiksi osto- tai myyntiasiakirjan hyväksyntä työnkulun osana.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="how-to-use-approval-workflows"></a>Toimintaohje: Hyväksyntätyönkulkujen käyttäminen

Jos organisaatiosi henkilön pitää hyväksyä tietue, kuten ostoasiakirja tai asiakaskortti, hänelle lähetetään hyväksyntäpyyntö työnkulun osana. Hyväksyjä saa työnkulun määrityksen mukaan ilmoituksen siitä, että tietue odottaa hänen hyväksyntäänsä.

Hyväksyntätyönkulut määritetään **Työnkulku**-sivulla. Hyväksynnän käyttäjät, mukaan lukien mahdolliset asianmukaiset summan rajoitukset, täytyy määrittää **Hyväksynnän käyttäjäasetukset** -sivulla. Lisätietoja kohdassa [Hyväksynnän työnkulkujen määrittäminen](across-set-up-workflows.md).  

Tässä artikkelissa kuvattujen hyväksyntätyönkulkujen lisäksi voit suorittaa useita muita työnkulun tehtäviä. Lisätietoja on kohdassa [Hyväksyntätyönkulkujen käyttäminen](across-use-workflows.md).

Ostoasiakirjojen, myyntiasiakirjojen, maksupäiväkirjojen, asiakaskorttien ja nimikekorttien perushyväksyntätyönkulut ovat valmiita käynnistettäväksi oppaina. Lue lisätietoja kohdasta [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

## <a name="request-a-record-approval"></a>Tietueen hyväksynnän pyytäminen

Hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

1. Valitse tietueen sivulla **Lähetä hyväksymispyyntö** -toiminto.
2. Kaikki hyväksymispyynnöt nähdäksesi valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksymispyyntötapahtumat**, valitse sitten vastaava linkki.  

Hyväksyntämerkinnän tila muuttuu **Luotu** -tilasta**Avoin**-tilaksi. Tietueen, kuten ostolaskun, tila päivitetään **Avoin**-tilasta **Odottaa hyväksyntää** -tilaksi. Tietue pysyy lukittuna käsittelyltä, kunnes hyväksyjät ovat hyväksyneet tietueen.

Kun kaikki vaaditut hyväksyjät ovat hyväksyneet tietueen, sen tilaksi muuttuu **Vapautettu**. Tämän jälkeen voit jatkaa tietueeseen liittyviä tehtäviä.

## <a name="cancel-approval-requests"></a>Peruuta hyväksymispyyntö

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Tilanne voi toisinaan edellyttää, että asiakkaan täytyy tehdä muutoksia tilaukseen, joka on lähetetty hyväksyttäväksi. Tällöin voit peruuttaa hyväksyntäprosessin, tehdä tarvittavat muutokset tilaukseen, ja sitten pyytää hyväksyntää uudelleen.

- Valitse tietueen näyttävällä sivulla **Peruuta hyväksymispyyntö** -toiminto.

Kun hyväksyntäpyyntö on peruutettu, siihen liittyvän hyväksyntämerkinnän tilaksi tulee **Peruutettu**. Tietueen tila muuttuu **Odottaa hyväksyntää** -tilasta**Avoin**-tilaksi. Tässä vaiheessa hyväksyntäprosessi voi alkaa uudelleen.

## <a name="approve-or-reject-approval-requests"></a>Hyväksymispyyntöjen hyväksyminen tai hylkääminen

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Voit käsitellä hyväksymispyynnöt **Hyväksyttävät pyynnöt** -sivulla, mukaan lukien useiden pyyntöjen hyväksyminen kerralla. Voit vaihtoehtoisesti hyväksyä yksittäisiä tietueita valitsemalla saamasi ilmoituksen linkin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksyttävät pyynnöt** ja valitse sitten vastaava linkki.
2. Valitse yksi tai useampi rivi tietueesta tai tietueista, jonka haluat hyväksyä tai hylätä.
3. Valitse **Hyväksy**-, **Hylkää**- tai **Delegoi**-toiminto.

Kun tietue on hyväksytty tai hylätty, hyväksynnän **Tila**-kentän arvoksi muutetaan vastaavasti **Hyväksytty** tai **Hylätty**.

Jos hyväksyjähierarkia on määritelty, tietueen tilaksi määritellään **Odottaa hyväksyntää** siihen asti, että kaikki pyydetyt hyväksyjät ovat hyväksyneet tietueen. Tietueen tilaksi tulee tämän jälkeen **Vapautettu**.

Hyväksynnän tila muuttuu samanaikaisesti **Luodusta** **Avoimeksi** heti, kun tietueelle luodaan hyväksymispyyntö. Jos pyyntö hylätään, hyväksynnän tilaksi muutetaan **Hylätty**. Tila pysyy **Avoimena** tai **Hylättynä** kunnes kaikki hyväksyjät ovat hyväksyneet pyynnön.

## <a name="delegate-approval-requests"></a>Delegoi hyväksymispyynnöt

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Työnkulun tukkiutumisen tai tietueiden kasaantumisen estämiseksi hyväksyjä ja hyväksynnän valvoja voi delegoida hyväksymispyynnöt sijaiselle. Korvaava voi olla joko nimetty korvaaja, suora hyväksyjä tai hyväksynnän järjestelmänvalvoja, tässä järjestyksessä. Tätä toimintoa käytetään yleensä, kun alkuperäinen hyväksyjä ei ole käytettävissä eikä pysty käsittelemään pyyntöjä ennen eräpäivää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksyttävät pyynnöt**, valitse sitten vastaava linkki.
2. Valitse vähintään yksi pyyntörivi, jonka haluat delegoida sijaiselle, valitse sitten **Delegoi**-toiminto.

Ilmoitus hyväksyttävästä pyynnöstä lähetetään sijaiselle.

## <a name="manage-overdue-approval-requests"></a>Myöhässä olevien hyväksymispyyntöjen hallinta

Hyväksymisoikeudet omaava hyväksynnän käyttäjä suorittaa seuraavan tehtävän.

Sinun on säännöllisin väliajoin muistutettava hyväksynnän työnkulun käyttäjiä erääntyneistä hyväksymispyynnöistä. Voit käyttää **Lähetä erääntyneet hyväksymisilmoitukset** -toimintoa.

**Lähetä ilmoituksia myöhässä olevista hyväksynnöistä** -toiminto tarkistaa kaikki avoimet myöhässä olevat hyväksyntäpyynnöt. Toiminto lähettää luettelon kaikista myöhässä olevista hyväksynnöistä jokaiselle hyväksyjälle, jolla on vähintään yksi myöhässä oleva hyväksyntämerkintä. Ilmoitus lähetetään myös hyväksyjän esimiehelle ja kaikille myöhässä olevien hyväksyntöjen pyytäjille. Tästä viimeisestä vaiheesta on apua, jos hyväksyntä on siirrettävä sijaiselle.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Erääntyneet hyväksymispyynnöt** ja valitse sitten vastaava linkki.
2. Valitse **Myöhässä olevat hyväksyntäpyynnöt** -sivulla **Lähetä erääntyneiden hyväksyntöjen ilmoitukset** -toiminto.

## <a name="see-also"></a>Katso myös

[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  
[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Myynti](sales-manage-sales.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
