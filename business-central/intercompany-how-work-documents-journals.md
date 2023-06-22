---
title: Konsernin asiakirjojen ja päiväkirjojen kirjaaminen
description: 'Tämä aihe selitää, miten voit kirjata tapahtumat konsernikumppanien kanssa konsernin asiakirjojen tai päiväkirjojen avulla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals" />Konserniasiakirjojen ja -päiväkirjojen käyttäminen

Voit kirjata konsernin asiakirjojen tai päiväkirjojen avulla tapahtumia yhdessä konsernikumppanien kanssa. Voit kirjata tapahtumia KP-tileille, ja jos olet määrittänyt konsernin pankkitilit, voit myös kirjata pankkien välisiä tilisiirtoja. Lisätietoja konsernin pankkitiliasetuksista on ohjeaiheessa [Konsernikumppanien käyttöön tarkoitettujen pankkitilitapahtumien määrittäminen](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Kun kirjaat konsernin asiakirja- tai päiväkirjarivin omassa yrityksessä, vastaava asiakirja- ja päiväkirjarivi luodaan konsernin Lähtevät-kansioon. Siirrät rivin Lähtevät-kansiosta kumppanillesi. Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.

Myynti- ja ostoasiakirjojen osalta asiakkaan tai toimittajan konsernikumppanin koodi varmistaa, että kaikki kumppaneiden välisten tapahtumien tilaukset ja laskut tuottavat kumppaniyrityksissä vastaavia asiakirjoja. Yritystilin saldo on oikein.

Sama pätee konsernin yleisen päiväkirjan riveihin. Sinun ei tarvitse määrittää tilejä, valitse vain kumppaniyritys. Vastaavat konsernin yleisen päiväkirjan rivit luodaan sitten kumppaniyrityksessä.

## <a name="fill-in-and-send-an-intercompany-sales-order" />Konsernin myyntitilauksen täyttäminen ja lähettäminen

Voit lähettää myynti- ja ostotilauksia sekä palauttaa tilauksia ennen kirjaamista. Laskut ja hyvityslaskut voi lähettää vasta, kun ne on kirjattu.

Seuraavissa ohjeissa neuvotaan, kuinka voit täyttää ja lähettää konsernin myyntitilauksen. Samat ohjeet koskevat myös konsernin osto- ja palautustilauksia sekä kirjattuja konsernin laskuja ja hyvityslaskuja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi myyntitilaus valitsemalla **Uusi**. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Varmista, että asiakas konsernikumppani.
5. Voit lähettää myyntitilauksen ennen sen kirjaamista valitsemalla **Lähetä konsernin myyntitilaus** -toiminto.

> [!NOTE]
> Jos teet vaiheen 5, myyntitilaus siirretään konsernin Lähtevät-kansioon, josta voit lähettää sen myöhemmin. Jos haluat lisätietoja konsernin Saapuneet-kansiosta ja Lähtevät-kansiosta, siirry [Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md) -kohtaan.

## <a name="fill-in-and-post-an-intercompany-journal" />Voit täyttää ja kirjata konsernin päiväkirjan seuraavasti

Kun kirjaat konsernin yleisen päiväkirjan rivin omassa yrityksessä, vastaava päiväkirjarivi luodaan konsernin Lähtevät-kansioon kumppanille lähettämistä varten. Alkaen vuoden 2022 julkaisuaallosta 1 voit myös määrittää yrityksen konsernikumppaneilta saatujen konsernin sisäisten tapahtumien automaattista luontia varten, jotka on kirjattu konsernin yleiseen päiväkirjaan. Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin yleiset päiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa päiväkirjan erä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Anna **Konsernikumppanin KP-tilinro** kentässä se konsernin kirjanpitotilin numero, jolle summa kirjataan kumppaniyrityksessä.

    > [!NOTE]
    > Tämä kenttä on täytettävä, jos rivin **Tilinro**- tai **Vastatilin nro** -kentässä on pankkitili tai kirjanpitotili.  
5. Valitse **Kirjaa**-toiminto.

Tapahtumat kirjataan omaan yritykseen ja päiväkirjaan. Lisäksi vastaavat tapahtumat luodaan konsernin Lähtevät-kansioon, josta voit lähettää ne kumppaniyritykselle.

## <a name="see-also" />Katso myös

[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
