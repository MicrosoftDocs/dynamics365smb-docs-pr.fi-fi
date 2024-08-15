---
title: Anna Business Centralin ehdottaa arvoja
description: 'Voit välttää manuaaliset laskutoimitukset sekä suorittaa tehtävät nopeasti ja tarkasti määrittämällä automaattisen tietojen antamisen, jolloin Business Central täyttää valitut kentät.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="let--suggest-values"></a>Anna [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa arvoja
[!INCLUDE[prod_short](includes/prod_short.md)] voi auttaa tehtävien suorittamisessa nopeammin ja tarkemmin täyttämällä kentät tai rivit tiedoilla, jotka muussa tapauksessa olisi laskettava ja annettava manuaalisesti. Vaikka automaattinen tietojen syöte on aina oikea, voit halutessasi muuttaa arvoja myöhemmin.

Toiminto, joka syöttää arvot puolestasi, sisältyy yleensä tehtäviin, joissa syötetään suuria määriä tapahtumatietoja. Niissä halutaan välttää virheet ja säästää aikaa. Tässä artikkelissa on tällainen toimintovalikoima. [!INCLUDE[prod_short](includes/prod_short.md)]in tulevat päivitykset sisältävät uusia osia.

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>**Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla
Kun esimerkiksi olet syöttämässä yleisen päiväkirjan rivejä useille kuluille, jotka kaikki täytyy kirjata samalle pankkitilille, niin aina kun syötät uuden päiväkirjan rivin kululle, voit **päivittää pankkitilirivin Summa-kentän** automaattisesti siihen summaan, joka täsmää kulut. Lisätietoja yleisten päiväkirjojen käsittelemisestä on ohjeaiheessa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>**Summa**-kentän täyttäminen automaattisesti yleisen päiväkirjan rivien täsmäyttämistä varten
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse haluamasi yleisen päiväkirjan erän rivillä **Ehdota vastasummaa** -valintaruutu.
3. Avaa yleinen päiväkirja ja jatka rekisteröitymiseen. Kirjaa tapahtumia edellä esiteltyjen toimintojen avulla, kun haluat, että kentän arvo syötetään automaattisesti.       

Lisätietoja henkilökohtaisen yleisen päiväkirjan erän määrittämisestä esimerkiksi kulujen käsittelemistä varten on ohjeaiheessa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>**Täytä vastaanottopäivämäärä automaattisesti** -kenttä **Maksurekisteröinti**-sivulla
Rekisteröi **asiakasmaksut -** sivulla näkyvät avoimet saapuvat maksut riveinä, jotka edustavat myyntiasiakirjoja, joiden maksuun erääntyy summa. Lisätietoja asiakkaan maksujen kohdistamisesta on kohdassa [Asiakasmaksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Sivun tärkeimmät toiminnot ovat Maksu suoritettu **-valintaruudun** ja **Vastaanottopvm-kentän** täyttäminen. Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in siten, että se lisää päivämäärän automaattisesti **Vastaanottopvm**-kenttään silloin, kun valitset **Maksu suoritettu** -valintaruudun.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>**Maksurekisteröinti**-sivun **Täytä vastaanottopäivämäärä automaattisesti** -kentän automaattinen täyttäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinnin asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu.
3.  **Avaa Rekisteröi asiakasmaksut -** sivu ja käsittele saapuvat asiakasmaksut käyttämällä kentän arvon automaattiseen syötykseen kuvattua toimintoa.

## <a name="see-also"></a>Katso myös
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Taloushallinto](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
