---
title: Luettelonimikkeiden luominen ja hallinta
description: 'Tietoja siitä, miten myydään nimikkeitä, joita ei pidä nimikeluettelossa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items"></a><a name="work-with-catalog-items"></a><a name="work-with-catalog-items"></a>Luettelonimikkeiden käsitteleminen

Luettelonimikkeet ovat nimikkeitä, joita et hallitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ennen kuin myyt ne. Kun lisäät luettelonimikkeen myyntitilauksen tai -tarjouksen tai puitemyyntitilauksen riviin käyttämällä **Valitse luettelonimike** -toimintoa, luettelonimike muunnetaan tavalliseksi nimikkeeksi.

> [!NOTE]  
> Luettelonimikettä ei voi valita **Myyntilasku**-sivulla.

Luettelonimikkeellä on yleensä sen toimittavan toimittajan nimikenumero. Ennen kuin voit muuntaa luettelonimikkeen tavalliseksi nimikkeeksi, sinun täytyy määrittää, miten toimittajan nimikenumerot muunnetaan nimikenumerointisi mukaisiksi. Lisätietoja nimikkeiden numeroinnista on kohdassa [Määritä, miten luettelonimikenumerot muunnetaan omaksi numeroinniksi](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Luettelonimikkeitä ei tule sekoittaa muihin kuin varastonimikkeisiin, jotka ovat tavallisia nimikkeitä, joiden tyyppi on **Muu kuin varasto**. Niitä ei oteta mukaan saatavuus- ja arvostuslaskelmiin esimerkiksi sen vuoksi, että niitä käytetään vain sisäisesti ja niiden arvo on vähäinen. Jos haluat oppia lisää muista kuin varastonimikkeistä, siirry kohtaan [Tietoja nimiketyypeistä](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a><a name="create-a-catalog-item"></a><a name="create-a-catalog-item"></a>Luettelonimikkeen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a><a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a><a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Määritä, miten luettelonimikenumerot muunnetaan omaksi numeroinniksi

Ennen kuin voit muuntaa luettelonimikkeen tavalliseksi nimikkeeksi, sinun täytyy määrittää, miten toimittajan nimikenumerot muunnetaan nimikenumeroidesi rakenteen mukaisiksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeen asetukset** ja valitse sitten vastaava linkki.
2. Valitse haluamasi asetukset **Nromuoto**-kentässä.

## <a name="convert-a-catalog-item-to-a-normal-item"></a><a name="convert-a-catalog-item-to-a-normal-item"></a><a name="convert-a-catalog-item-to-a-normal-item"></a>Muunna luettelonimike normaaliksi nimikkeeksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen luettelonimikkeen kortti, jonka haluat muuntaa normaaliksi nimikkeeksi.
3. Valitse **Luettelonimikkeen kortti**-sivulla **Luo nimike** -toiminto.

Luodaan uusi nimikekortti, johon on täytetty luettelonimikkeen tiedot, ja nimikemalli. Voit tarvittaessa muokata uuden nimikkeen tietoja. Saat lisätietoja nimikkeiden luomisesta valitsemalla [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a><a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a><a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Luettelonimikkeen myyminen ja muuntaminen normaaliksi nimikkeeksi

Seuraava prosessi käyttää myyntitilausta, mutta työvaiheet ovat samat puitemyyntitilauksille ja -tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Täytä **Yleinen**-pikavälilehden kentät samalla tavalla kuin myyntitilauksen kentät. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3. Valitse uuden tilausrivin **Tyyppi**-kentässä **Nimike**, mutta jätä **Nro**-kenttä tyhjäksi.
4. Valitse ensin **Rivi**-toiminto ja sitten **Valitse luettelonimikkeet** -toiminto.
5. Valitse **Luettelonimikkeet**-sivulla luettelonimike, jonka haluat myydä, ja valitse sitten **OK**-painike.
6. Kun myyntitilaus on valmis, valitse **Kirjaa**-toiminto.

> [!NOTE]  
> Nimikkeen viittaus on automaattisesti nimike, jonka numero on toimittajan nimikenumeron ja uuden nimikenumeron välissä. Saat lisätietoja nimikeviitteistä siirtymällä kohtaan [Käytä nimikeviittauksia](inventory-how-use-item-cross-refs.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Erikoistilausten luominen](sales-how-to-create-special-orders.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
