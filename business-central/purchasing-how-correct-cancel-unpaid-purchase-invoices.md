---
title: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen (sisältää videon)
description: 'Tässä ohjeaiheessa kerrotaan, miten kirjattua lasku korjataan, peruutetaan tai kumotaan ja miten ostohyvityslasku luodaan automaattisesti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Maksamattomien ostolaskujen korjaaminen tai peruuttaminen

Voit korjata tai peruuttaa maksamattoman ostolaskun. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.

Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta. Sen sijaan sinun on peruutettava osto luomalla ostohyvityslasku, jota voi tarvittaessa hallinta ostopalautustilauksella. Samaa koskee tilannetta, jossa halutaan muokata yhdistettyihin ostovastaanottoihin perustuvaa ostolaskua. Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Valitse **Kirjattu ostolasku** -sivulla **Korjaa**- tai **Peruuta**-painike. Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin. Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten. Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Kirjatun ostolaskun korjaamiseksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse kirjattu ostolasku, jonka haluat korjata.  

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu ostolasku** -sivulla **Korjaa**.

    Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md). Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Kirjatun ostolaskun peruuttamiseksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse kirjattu ostolasku, jonka haluat peruuttaa.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu ostolasku** -sivulla **Peruuta**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku. Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

### <a name="partial-invoice-posting-also-supported"></a>Osittaisen laskun kirjausta tuetaan myös

Jos peruutus liittyy osittaiseen laskun kirjaukseen, alkuperäinen ostotilausrivi päivitetään peruutetun laskutetun määrän mukaiseksi. **Laskutettava määrä** - ja **Laskutettu määrä** -kentät liittyvässä ostotilauksessa palautetaan arvoihin ennen osittaista kirjausta.

## <a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaaminen](purchasing-how-record-purchases.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
