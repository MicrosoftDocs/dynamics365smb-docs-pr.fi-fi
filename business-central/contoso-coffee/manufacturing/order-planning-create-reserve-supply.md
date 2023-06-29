---
title: Käytä tilauksen suunnittelua tarjonnan luomiseksi ja varaamiseksi
description: 'Vaihekuvauksessa on tietoja siitä, miten tilauksen suunnittelua käytetään tarvittavan tuotantotilauksen luomiseen Business Centralin tarjonnassa.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a><a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Vaihekuvaus: Käytä tilauksen suunnittelua tarjonnan luomiseksi ja varaamiseksi

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä tilauksen suunnittelussa.

## <a name="scenario"></a><a name="scenario"></a>Esimerkkitilanne

Olet Contoso Coffeen tuotantosuunnittelija. Tuotantotilaus luotiin 100 yksikölle nimikkeelle **SP-SCM1009, Airpot**, ja haluat suunnitella osakokoonpanoja tälle tilaukselle. Tilauksen suunnittelua käytetään tarjonnan edellyttämän tuotantotilauksen luomiseen. Koska olet luomassa tuotantotilausta tietyn tilauksen tarpeiden täyttämiseksi, päätät varata tuotantotilauksen tuotoksen.  

## <a name="steps"></a><a name="steps"></a>Vaiheet

1. Luo uusi vapautettu tuotantotilaus **SP-SCM1009, Airpot** -nimikkeen 100 yksikölle.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Lähdetyyppi** |Nimike|
        |**Lähteen nro** |SP-SCM1009|
        |**määrä** |100|
    3. Valitse **Päivitä tuotantotilaus** -toiminto.  

    Huomioi vapautetun tuotantotilauksen numero.

2. Avaa **Tilauksen suunnittelu** -sivu ja laske uusi suunnitelma.

    1. Valitse **Suunnittelu**-toiminto.  

    2. Valitse **Tilauksen suunnittelu** -sivulla **Laske suunnitelma** -toiminto.  

    3. Vieritä alas kysyntäriville, joka kuvaa aiemmin luomaasi vapautettua tuotantotilausta.  

    4. Laajenna rivejä tarkastellaksesi kysyntärivin tietoja. Vahvista, että kyseessä on ehdotus 1001-nimikkeen 100 yksikön tuotantotilaukselle.  

3. Luo uusi tuotantotilaus 100 yksikölle nimikkeelle **SP-BOM2000, Reservoir Assy.** ja varaa tuotantotilauksen tuotos liittyvän päätilauksen puolesta.  

    1. Valitse **Varaa**-kentän valintaruutu kysyntärivillä nimikkeen SP-BOM2000 100 yksikölle.

    2. Valitse **Tee tilaukset** -toiminto.  

    3. Määritä **Tee tilaukset** -kentän arvoksi *Aktiivinen rivi*.  

    4. Määritä **Luo tuotantotilaus** -kentän arvoksi *Sitovasti suunniteltu*.

    5. Valitse **OK** luodaksesi tuotantotilauksen.

    6. Varmista **Tilauksen suunnittelu** -sivulla, että nimikkeen 1001 100 yksikön kysyntärivi on poistettu.

Siinä kaikki tilauksen suunnittelusta kohteessa [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Johdatus Contoson kahvidemotietoihin](../contoso-coffee-intro.md)  
[Tietoja tuotantotilauksista](../../production-about-production-orders.md)  
