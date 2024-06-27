---
title: Toimittajille suoritettavien maksujen hallintatehtävien yleiskatsaus
description: 'Tässä ohjeaiheessa kerrotaan toimittajille tai luotonantajille suoritettavien maksujen hallintatehtävistä, kuten maksurivien kirjaamisesta ja erääntyvän saldon yleiskatsauksen hakemisesta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Maksujen suorittaminen

Maksat maksut toimittajille tai asiakkaille tai hyvityksiä työntekijöille, kirjaat liittyvät maksurivit **Maksupäiväkirja**-sivulle. Maksupäiväkirja on yleinen päiväkirja, joka on tarkoitettu erityisesti maksujen tekemiseen ja joka tarjoaa paljon vahvoja toimia. Esimerkki: **Ehdota toimittajamaksuja** -toiminto, joka etsii erääntyvät toimittajamaksut, ja **Toimittaja - Eräänt.yht.kohtainen** -raportti, jossa on yleiskuva erääntyvistä toimittajamaksuista.  

Voit aloittaa maksuprosessin toimittajille, asiakkaille ja työntekijöille luetteloista, korteista ja tapahtumista. Jokaisella sivulla on painike, joka aloittaa maksuprosessin ja auttaa täyttämään maksukirjauskansion.  

Maksupäiväkirjassa voit tulostaa tietokonesekkejä tai kirjata käsin kirjoitettuja sekkejä. Jos valitset **Tietokonetarkistus**-vaihtoehdon **Pankkimaksun tyyppi** -kenttään, sekkejä edustavat rivit on tulostettava, ennen kuin maksupäiväkirja voidaan kirjata.

Kun maksut kirjataan, voit viedä ne pankkitiedostoon, jolloin ne voidaan ladata verkkopankkiisi käsittelyä varten.

Kun maksut on tehty pankkiin, kohdista ne liittyviin avoimiin toimittaja- tai työntekijätapahtumiin. Voit ottaa ne käyttöön manuaalisesti tai tuomalla pankin tiliotetiedoston ja kohdistamalla maksut automaattisesti. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

| Vastaanottaja | Katso |
| --- | --- |
|Ymmärrä yleiseen päiväkirjaan perustuvan **Maksupäiväkirja**-sivun perustoiminnot, joiden avulla voit valmistella kirjaavasi maksut toimittajille tai työntekijöille.|[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)|
|Kirjaa maksut toimittajille tai työntekijöille ja hyvitykset asiakkaille. Valinnaisesti voit kohdistaa maksut liittyviin maksamattomiin laskuihin/hyvityslaskuihin ja sulkea ne maksettuina.|[Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md)|
| Käytä **Maksupäiväkirja**-sivun toimintoa ehdottaaksesi toimittajan maksuja valittujen ehtojen, kuten eräpäivän, alennuskelpoisuuden ja maksuvalmiutesi, mukaan. |[Ehdota toimittajamaksuja](payables-how-suggest-vendor-payments.md) |
| Myönnä sekkejä toimittajan maksuille tai asiakkaan hyvityksille joko tulosteina tai tietokonesekkeinä. Mitätöi sekit ennen kirjaamista tai sen jälkeen. |[Sekkimaksujen suorittaminen](payables-how-work-checks.md) |
|Suorita sähköiset maksut EU:n SEPA-tilisiirtostandardin mukaisesti.|[Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Maksaa toimittajalle käteisellä tai sekillä ja kirjaa maksu, kun lasku kirjataan. |[Ostolaskujen selvittäminen viipymättä](finance-how-to-settle-purchase-invoices-promptly.md) |
| Varmista lähettämällä toimittaja-, sekki- ja maksutiedot sisältävä tiedosto, että pankki vahvistaa vain tarkistetut sekit ja summat. |[Positive Pay -tiedoston vieminen](finance-how-positive-pay.md) |

## Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
