---
title: Projektin myyntilaskun luominen projektin laskuttamiseksi
description: 'Käsitellään sitä, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä ja kustannusten kertyessä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# <a name="invoice-projects"></a>Projektien laskuttaminen

Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista. Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan. On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.
Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.

Voit laskuttaa:

* Useita projekteja, jotka **käyttävät Projekti luo myyntilasku -** tehtävää.
* Kokonaisia projekteja, projekteja, joissa on projekti, tai yksittäisiä projektin suunnittelurivejä, jotka käyttävät asiaankuuluvaa projektisivujen toimintoa.
* Yhdistä useita projektin suunnittelurivejä eri projekteista yhdeksi myyntilaskuksi käyttämällä **Hae projektin suunnittelurivit** -toimintoa **Myyntilasku-sivulla** .

## <a name="to-create-multiple-project-sales-invoices"></a>Usean projektin myyntilaskun luominen

Asiakkaalle voidaan luoda lasku projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.

Seuraavaksi näytetään, miten eräajoa käytetään useiden projektien laskuttamiseen.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.
4. Luo laskut valitsemalla **OK**.  

Voit tarkistaa ja kirjata luotuja laskuja **Myyntilaskut-sivulla** .

> [!NOTE]
> Vaihtoehtoisesti voit laskuttaa asiakasta valitsemalla projektin ja valitsemalla **sitten Luo projektin myyntilasku -** toiminnon tai käyttämällä **Luo myyntilasku -** toimintoa projektitehtävissä.

## <a name="to-create-and-post-project-sales-invoice-from-project-planning-lines"></a>Projektin myyntilaskun luominen ja kirjaaminen projektin suunnitteluriveiltä

Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.
2. Avaa sopiva projekti.
3. Valitse projektitehtävä, jonka **Projektitehtävän tyyppi** -kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Syötä projektin suunnittelurivin **Laskuun siirrettävä määrä** -kenttään nimikkeen, resurssin tai pääkirjanpitotilin tyyppi, jonka haluat laskuttaa.  
5. Valitse **Luo myyntilasku** -toiminto.
6. Syötä **Siirrä projekti myyntilaskuun** -sivulla kirjauspäivämäärä. Määritä, haluatko luoda uuden laskun vai kohdistaa tämän laskun aiemmin luotuun laskuun.
7. Valitse **OK**-painike.  
8. Valitse **Projektin suunnittelurivit** -sivulla **Myyntilaskut/hyvityslaskut**-toiminto.

    Avautuvassa **Myyntilasku**-sivulla näkyy laskuun siirretty määrä.
9. Tee tarvittavat muutokset ja valitse **Kirjaa**-toiminto.

> [!NOTE]  
> Projektiin liittyvän myyntihyvityslaskun luominen, tarkistaminen ja kirjaaminen tapahtuu vastaavalla tavalla.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Useiden projektitehtävien laskuttaminen yhdeltä asiakkaalta

Laskutusprosessia voidaan yksinkertaistaa lähettämällä asiakkaalle yksi lasku, joka sisältää useita projekteja. Useiden projektien projektin suunnittelurivit lisätään kerralla myyntilaskuun. Tämä prosessi muistuttaa myyntilaskun luontia projektin suunnitteluriviltä ja arvon syöttämistä **Liitä myyntilaskun nroon** -kenttään.

Prosessin yleiskatsaus:

1. Luo uusi myyntilasku ja määritä arvo **Tilausasiakkaan nro** -kentässä. Täytä tarvittaessa myös **Laskutusasiakkaan nro**- ja **Valuuttakoodi**-kentät.
2. Valitse **Rivit**-pikavälilehdessä **Hae projektin suunnittelurivit** -toiminto. **Hae projektin suunnittelurivit** -sivulla on näkyvissä tilausasiakkaan projektien laskutettavat projektin suunnittelurivit, laskutusasiakas ja laskutusvaluutta, jos laskutettava määrä on suurempi kuin nolla. 
3. Valitse laskuun lisättävät rivit ja valitse sitten **OK**.

Toista nämä vaiheet, jos haluat lisätä toiseen projektin suunnittelurivijoukon. Lasku tai sen rivit voidaan myös poistaa ja aloittaa alusta.

> [!NOTE]
> Rajoitukset:
>
> * **Hae projektin suunnittelurivit** -toiminto ei ole saatavana myyntitilauksissa tai myyntitarjouksissa.
> * Suodatus ei ole mahdollista **Toimitusasiakkaan koodi**- tai **Yhteyshenkilön nro** -kentässä.


## <a name="see-also"></a>Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
