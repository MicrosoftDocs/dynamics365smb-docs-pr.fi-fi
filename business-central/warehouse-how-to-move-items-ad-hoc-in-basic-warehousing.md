---
title: Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä
description: Tässä artikkelissa käsitellään suunnittelemattomia sisäisiä siirtoja varastopaikkojen välillä ilman lähdeasiakirjasta peräisin olevaa kysyntää.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# Nimikkeiden siirtäminen sisäisesti fyysisen varastoinnin perusmäärityksissä

Nimikkeitä halutaan ehkä siirtää varastopaikkojen välillä lähdeasiakirjasta peräisin olevaa kysyntää. Se voidaan tehdä esimerkiksi seuraavien toimintojen osana:

* Fyysisen varaston järjestäminen uudelleen.
* Nimikkeiden tuominen tarkastusalueelle.
* Ylimääräisten nimikkeiden siirtäminen tuotantoalueelle ja sieltä pois. 

Nimikkeiden siirtäminen määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Jos **Varastopaikka pakollinen** on otettu käyttöön vaihtopainikkeella fyysisen varastoinnin määrityksessä mutta **Ohjattu poiminta ja hyllytys** ei ole käytössä, suunnittelemattomat varastosiirrot voidaan rekisteröidä seuraavilla sivuilla:  

* **Sisäinen siirto** -sivu.
* **Nimikkeen uudellenluokituspvk** -sivu.  

## Sisäiset siirrot

**Sisäiset siirrot** sivulla voidaan määrittää otto- ja asetusrivit, kun kysyntä ei ole peräisin lähdeasiakirjasta. Sisäinen siirto -sivu on eräänlainen järjestelemisen työkirja. Varsinaista varastosiirto ei voi käsitellä suoraan tältä sivulta. Kun rivi on täytetty, rivi lähetetään **Luo varastosiirto** -toiminnolla **Varastosiirto**-sivulle, jossa varastosiirto käsitellään ja rekisteröidään.

### Siirrä kohteita sisäisenä siirtona

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sisäiset siirrot** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Varmista, että **Nro**-kenttä täytetään **Yleinen**-pikavälilehdessä.
3. Anna **Sijaintikoodi**-kentässä sijainti, jossa varaston siirto tapahtuu.  

    Jos sijainti on varastotyöntekijän oletussijainti, sijaintikoodi lisätään automaattisesti.  
4. Syötä **Varastopaikkakoodiin**-kentässä sen varastopaikan koodi, johon nimikkeet siirretään.

    Esimerkiksi tuotannossa varastopaikka voi olla sijaintikortissa tai tuotantosolussa määritetty avoin tuotannon varastopaikka.  
5. Syötä **Eräpäivä**-kentässä päivämäärä, jona varastosiirron on oltava valmis.  
6. Täytä kunkin rivin muut kentät tarvittaessa. Sisäisissä siirtoasiakirjoissa kullakin varastosiirrolla on yksi rivi. Rivi sisältää sekä otto- että asetustoiminnot.
7. Avaa **Varastopaikan sisältöluettelo** -sivu valitsemalla **Nimikenro**-kenttä. Valitse siirrettävä kenttä sen varastopaikkasaatavuuden perusteella, Sisäisen siirron rivit voidaan täyttää myös suodattimen perusteella valitsemalla **Hae var.paikan sisältö** -toiminto.  

    Kun nimike on valittu, **Var.paikasta**-kenttä täytetään automaattisesti valitun varastopaikan sisällön mukaan. Mikä tahansa varastopaikka, jossa nimike on saatavana, voidaan valita. **Nimikenro**- ja **Var.paikasta**-kentät liittyvät toisiinsa. Arvon muuttaminen yhdessä kentässä voi muuttaa toisen kentän arvon.  

    **Varastopaikkakoodiin**-kenttään täytetään ylätunnistetiedoissa syötetty arvo. Sen tilalle voidaan rivillä vaihtaa mikä tahansa varastopaikkakoodi, jota ei ole estetty tai jota ei ole varattu erityistarkoituksiin. Lisätietoja on kohdassa [Erityinen-kenttä](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Kun varastopaikat, joista nimikkeitä siirretään ja joihin niitä siirretään, on määritetty, syötä siirrettävä määrä **Määrä**-kenttään.  

    > [!NOTE]  
    > Määrä on oltava saatavana **Var.paikasta**-kentässä määritetystä varastopaikasta.  

9. Kun varastosiirron käsittelyyn ollaan valmiita, , valitse **Luo varastosiirto** -toiminto.  

    > [!NOTE]  
    >  Sisäisen siirron rivit poistetaan varastosiirron luonnin jälkeen.  

Suorita loput suunnittelemattomasta varaston siirrosta **Varastosiirto**-sivulla samalla tavoin kuin lähdeasiakirjojen varaston siirtoon perustuva siirto.

### Varastosiirron kirjaaminen

1. Avaa **Varastosiirto**-sivulla asiakirja, johon varaston siirto kirjataan.  
2. **Varastopaikkakoodi**-kentän varaston siirron riveillä varastopaikka, josta nimikkeet on poimitettava, on se varastopaikka, jossa nimike on saatavana. Varastopaikkaan voi muuttaa tarvittaessa.
3. Suorita varastosiirto ja syötä siirrettävän määrän tiedot **Käsiteltävä määrä** -kentässä. Ota- ja Aseta-rivien arvojen on oltava samat. Varaston siirron rekisteröiminen ei ole muutoin mahdollista.

    Jos rivin nimikkeitä on otettava useammasta kuin yhdestä varastopaikasta esimerkiksi siksi, että varastopaikassa ei ole koko määrää, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.  
4. Valitse **Rekisteröi varastosiirto** -toiminto.  

Kirjausprosessin sisältö:

* Fyysisen varaston tapahtumat ilmaisevat ottovarastopaikoista asetusvarastopaikkoihin siirretyn määrän.

## Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan kanssa

Varaston siirtoasiakirjojen käytön sijaan varaston siirrot voidaan kirjata uudelleenluokittelemalla nimikkeiden varastopaikkakoodit. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Uudelleenluokituspäiväkirjojen avulla kirjatut varaston siirrot eivät muuta varaston siirtoasiakirjoja siirrettäviksi.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimik. uud.luok.pvk** ja valitse sitten vastaava linkki.  
2. Määritä kullekin päiväkirjariville varastopaikat, joihin nimikkeitä siirretään ja joista niitä siirretään, täyttämällä **Varastopaikkakoodi**- ja **Uusi varastopaikkakoodi**-kentät.  

    1. Jos haluat siirtää koko sisällön toiseen varastopaikkaan, valitse **Hae var.paikan sisältö** -toiminto.  
    2. Suodattimien avulla voi etsiä siirrettävät nimikkeet sisältävä varastopaikka. Valitse sitten **OK**. Kirjauskansioriveille on täytetty varastopaikan sisältö.  
3. Täytä kunkin päiväkirjan rivin muut kentät.
4. Kirjaa uudelleenluokituspäiväkirja.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
