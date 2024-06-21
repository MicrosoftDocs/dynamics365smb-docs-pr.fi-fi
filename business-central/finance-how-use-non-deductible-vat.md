---
title: 'Vähennyskelvottoman ALV:n käyttö'
description: 'Tässä artikkelissa kerrotaan, miten vähennyskelvotonta ALV:tä voidaan käyttää ja raportoida.'
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
ms.reviewer: bholtorf
---

# <a name="use-non-deductible-vat"></a>Vähennyskelvottoman ALV:n käyttö

Tässä artikkelissa kerrotaan, miten vähennyskelvotonta ALV:tä voidaan käyttää ja raportoida.

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Ostolaskun luominen ilman vähennyskelpoista ALV:tä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Luo ostolasku valitsemalla **Uusi** ja syötä tarvittavat tiedot laskun otsikkoon.
3. Luo **Rivit**-osassa uusi minkä tahansa tyyppinen rivi, joka perustuu liiketoiminnan ALV-kirjausryhmään ja tuotteen ALV-kirjausryhmään, jossa määritetään vähennyskelvoton ALV.
4. Syötä **Määrä**- ja **Välitön yksikkökustannus** -kenttiin asianmukaiset arvot.

    Jos valitsit **Näytä vähennyskelv. ALV -riveillä** -valintaruudun **ALV-asetukset** -sivulla, **Vähennyskelvottoman ALV:n peruste**- ja **Vähennyskelvoton ALV-summa** -kenttien summat lasketaan **ALV-kirjausten asetukset** -sivun **vähennyskelvoton ALV-%** -kentän perusteella.

5. Kirjaa lasku.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a>Ostotilauksen luominen ilman vähennyskelpoista ALV:tä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Luo ostotilaus valitsemalla **Uusi** ja syötä tarvittavat tiedot asiakirjan otsikkoon.
3. Luo **Rivit**-osassa uusi minkä tahansa tyyppinen rivi, joka perustuu liiketoiminnan ALV-kirjausryhmään ja tuotteen ALV-kirjausryhmään, jossa määritetään vähennyskelvoton ALV.
4. Syötä **Määrä**- ja **Välitön yksikkökustannus** -kenttiin asianmukaiset arvot.

    Jos valitsit **Näytä vähennyskelv. ALV -riveillä** -valintaruudun **ALV-asetukset** -sivulla, **Vähennyskelvottoman ALV:n peruste**- ja **Vähennyskelvoton ALV-summa** -kenttien summat lasketaan **ALV-kirjausten asetukset** -sivun **vähennyskelvoton ALV-%** -kentän perusteella.

5. Kirjaa ostotilaus.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a>Oikaise pyöristetyt ALV-summat ennen asiakirjan kirjausta

Jos ALV-summia ei ole pyöristetty samalla tavalla ympäristössäsi ja ulkoisessa kirjanpitojärjestelmässä (alkuperäisessä laskuasiakirjassa), voit muuttaa ALV-summaa ennen asiakirjan kirjaamista. Voit tehdä tämän muutoksen tekemällä seuraavat toimet ennen asiakirjan kirjaamista.

1. Valitse toimintoruudussa **Tilastot**.
2. Jos käytät ostolaskua, toimi seuraavasti:

    1. Valitse **Rivit**-pikavälilehdessä ALV-summa tai vähennyskelvoton ALV-summa.
    2. Määritä tarvitsemasi arvot alkuperäisestä asiakirjasta ja sulje **Ostolaskun tilastot** -sivu.

3.  Jos käytät ostotilausta, toimi seuraavasti:

    1. Avaa **ALV-summarivit** -sivu valitsemalla **Laskutus**-pikavälilehdessä **Verorivien määrä**.
    2. Valitse ALV-summa tai vähennyskelvoton ALV-summa, jonka haluat korjata.
    3. Syötä tarvitsemasi arvot alkuperäisestä asiakirjasta, sulje **ALV-summarivit**-sivu ja sulje **Ostotilaustilastot**-sivu.

Jotta voisit käyttää ALV-summan muutoksia, muutokset on otettava käyttöön. Syötä **Pääkirjanpidon asetukset** -sivun **Suurin sallittu ALV-ero** -kenttään suurimman sallitun ALV-summan korjaus. Valitse sitten **Ostojen ja ostovelkojen asetukset** -sivulla **Salli ALV-ero**.

Voit muuttaa **ALV-summan** ja **Vähennyskelvoton ALV-summa** -kentän arvoja. **Vähennyskelpoinen ALV-summa** -kentän arvo on näiden kahden arvon tulos. Summa, jonka syötät **Vähennyskelvoton ALV-summa** -kenttään, ei voi olla suurempi kuin summa, jonka syötät **ALV-summa**-kenttään. **Pääkirjanpidon asetukset** -sivun **Suurin sallittu ALV-ero** -kenttä toimii itsenäisesti vähennettävissä ja vähennyskelvottomissa ALV-summissa tilastosivuilla, kun haluat muuttaa ALV-summaa.

> [!IMPORTANT]
> Ennakkomaksulaskuissa ei voi käyttää vähennyskelvotonta ALV:ta.

## <a name="see-also"></a>Katso myös

[Taloushallinto](finance.md)

[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  

[Vähennyskelvottoman ALV:n määrittäminen](finance-setup-nondeductible-vat.md)

[Rakennetiedot vähennyskelvottomasta ALV:stä](design-details-nondeductible-vat.md)

[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)

[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
