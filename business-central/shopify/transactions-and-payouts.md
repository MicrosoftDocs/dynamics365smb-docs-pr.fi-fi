---
title: Synkronoi tapahtumat ja maksut
description: Määritä ja suorita tapahtumien ja maksujen tuonti Shopifysta.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30124, 30125, 30130, 30131, 30132, 30133, 30134,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: f4833a3fa77cdff587947a9686e61e3255b66a7c
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728723"
---
# <a name="transactions-and-payouts"></a>Tapahtumat ja maksut

Kun asiakas suorittaa kassaprosessin loppuun verkkokaupassa, maksujen tiedot tallennetaan **tapahtumana**. Tilaukseen voi liittyä useita tapahtumia, esimerkiksi kun asiakas maksaa osan tilauksestaan lahjakortilla ja loput luottokortilla tai PayPalilla.

Jos maksupalvelun tarjoajasi on Shopify Payment, näet tietoja asiakkailta saaduista maksuista maksupalvelun tarjoajan mukaan sekä Shopifysta pankkitilillesi lähetetyt maksut.

## <a name="transactions"></a>Tapahtumat

Shopifyssa tapahtuvat maksutapahtumat synkronoidaan tilausten kanssa ja näytetään **Shopify-tilaukset**-sivulla.

Tarkastellaksesi kaikkia tapahtumia, valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tapahtumat** ja valitse vastaava linkki.

Jos olet määrittänyt maksutapojen kartoituksen, luodulle myyntiasiakirjalle kohdistetaan maksutavan koodi. Lisätietoja on kohdassa [Maksutavan yhdistäminen](#payment-method-mapping).

## <a name="payouts"></a>Maksut

Jos kauppasi käyttää Shopify Payment -palvelua, saat maksut **Shopify-maksuina**, kun asiakas maksaa käyttämällä Shopify Payments -palvelua ja nopeutettua kassaprosessia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida maksuja avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Synkronoi maksut** -toiminto.

Tarkastellaksesi kaikkia maksuja, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksut** ja valitse vastaava linkki.

**Maksut** on tarkoitettu vain tiedonannoksi eivätkä ne vaikuta pääkirjanpitoon tai pankkikirjanpitoon, mutta ne voivat olla hyödyllisiä, kun tarkastat tiliotettasi.

## <a name="payment-method-mapping"></a>Maksutavan yhdistäminen

Täyttääksesi **Maksutapakoodin** myyntiasiakirjoille, jotka on automaattisesti tuotu Shopifysta, sinun tulee määrittää **Maksutavan yhdistämismääritys**.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Maksutavan yhdistämismääritys** -toiminto.
4. Syötä Shopifyn maksutavan nimi kenttiin **Yhdyskäytävä** ja **Luottokorttiyhtiö**. Tietueet luodaan automaattisesti, kun tuot Shopify-tilauksia.
5. **Syötä maksuehdon koodi** ja vastaava maksutapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.
6. Määritä **prioriteetti** tapauksissa, joissa asiakas käyttää useaa maksutapaa. Korkeimman prioriteetin maksutapa valitaan myyntiasiakirjassa. Jos molemmilla maksutavoilla on sama prioriteetti, käytetään maksutapaa, jossa on korkein summa.

> [!NOTE]  
> Jos vastaavan maksutavan **Vastatilin tyyppi**- ja **Vastatilin nro** -kentät on täytetty [!INCLUDE[prod_short](../includes/prod_short.md)]issa, järjestelmä luo laskun kirjaamisen yhteydessä *Maksu*-tyyppisen vastatapahtuman ja lisää sen *Lasku*-tyyppiin asiakkaan kirjanpitotapahtumassa.

## <a name="use-cases"></a>Käyttötapaukset
  
Osapuolet:

* Ostaja - henkilö, joka ostaa tuotteita Shopify-verkkokaupastamme.
* Myyjä - yrityksesi.
* Maksupalvelun tarjoaja - yritys, joka helpottaa maksujen käsittelemistä puolestasi. Voi olla Shopify Payments tai kolmas osapuoli.

### <a name="how-money-flows"></a>Miten raha liikkuu

Ostaja ostaa tuotteita verkkokaupastamme. Viimeinen vaihe on maksujen käsitteleminen.

>[!NOTE]
> Tämä esimerkki ei kata tapauksia, joissa maksu suoritetaan Shopifyn uloskuittauksen ulkopuolella, mikä pätee B2B-skenaarioissa.
  
Ostaja maksaa luottokortilla, PayPalilla tai jollakin paikallisella maksutavalla kuten MobilePaylla Tanskassa. Maksupalvelun tarjoaja ottaa koko summan ostajalta. Tällä hetkellä ostajan rahoja siirretään maksupalvelun tarjoajalle.

Maksupalvelun tarjoajan mukaan myyjä saattaa nähdä nämä rahat maksupalvelun tarjoajan tilillä – sekä vastaanotetut määrät että vähennetyt palkkiot. Maksupalvelujen tarjoajat ottavat usein provision jokaisesta tapahtumasta, ja joissakin tapauksissa heillä voi olla myös kiinteämääräinen maksu.
  
Maksupalvelun tarjoajan mukaan myyjä joko käynnistää rahan siirron pankkitililleen (maksu) manuaalisesti tai että se tapahtuu automaattisesti tietyn ajan välein - kerran päivässä, kerran kuukaudessa, ja niin edelleen.
  
Pankista riippuen myyjä näkee tämän saapuvan tapahtuman pankkitilillään verkkopankin kautta tai tiliotteelta.

Maksutapahtumia käsitellään useilla eri tavoilla [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Vaihtoehto 1: Täsmäytä saapuvat siirrot pankkitiliin alkuperäisten laskujen mukaan
  
Myyjä tuo myyntitilauksen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan ja kirjaa toimituksen ja laskun.

Tulos: järjestelmä luo **asiakastapahtumamerkinnän**, jonka tyyppi on *lasku* koko summalle, **Avoin**-kentän arvo on kyllä. **Jäljellä olevan summa** on sama kuin laskutettu summa.

Myyjä tuo pankin tiliotteen käyttäen maksujen täsmäytyskirjauskansiota.

Ongelmat:

1. Voi olla vaikeaa, jos on olemassa useita laskuja (ja hyvityslaskuja), mutta yksi kertasuoritus maksupalvelun tarjoajalta.
2. Summa ei yleensä täsmää komission vuoksi. Maksutoleranssin tai/ja maksualennuksen avulla voit käsitellä maksuja.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Vaihtoehto 2: Täsmäytä pankkitilille saapuvat siirrot maksupalvelun tarjoajan rahaa edustavan välitilin kanssa
  
Myyjä tuo myyntitilauksen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan ja kirjaa toimituksen ja laskun.
  
Tulos: järjestelmä luo asiakastapahtumamerkinnän, jonka tyyppi on **Lasku** koko summalle, ja **Avoin**-kentän arvo on kyllä. **Jäljellä olevan summa** on sama kuin laskutettu summa.

Koska myyntitilauksella on kuitenkin maksutavan koodi, jossa **vastatilin tyyppi**- ja **vastatilin nro** -kentät on täytetty, järjestelmä luo automaattisesti toisen asiakastapahtuman, jonka tyyppi on **maksu**, ja kohdistaa sen aiemmin luotuun asiakastapahtumaan.

>[!NOTE]
> Järjestelmä täyttää maksutavan koodi -kentän maksutavan yhdistämismäärityksen perusteella. Lisätietoja on kohdassa [Maksutavan yhdistäminen](#payment-method-mapping).
  
Voit määrittää maksutapojen vastatilit kahdella tavalla:

* **Vastatilin tyyppi** määritetty *pankkina*, ja **vastatili nro** syöttää pankkitilin, joka edustaa tiliäsi maksupalveluntarjoajalla.
* **Vastatilin tyyppi** määritetty *KP-tilinä*, ja **vastatili nro** syöttää pankkitilin, joka edustaa KP-tiliäsi maksupalveluntarjoajalla.

On järkevää käyttää pankkitiliä, jos maksupalveluntarjoaja vie jonkinlaisen tiliotteen, jonka voi tuoda maksun täsmäytyspäiväkirjaan.

Myyjä tuo pankin tiliotteen käyttäen maksujen täsmäytyskirjauskansiota. Saapuva maksu voidaan käsitellä:

* siirtona toisesta pankista. Jos siirto kestää muutaman päivän tai edellyttää valuutan vaihtoa, haluat ehkä käyttää väliaikaista KP-tiliä.
* erona KP-tiliin, joka edustaa tiliäsi maksupalveluntarjoajalla.
  
Maksupalvelun tarjoajan tiliä edustavan KP- tai pankkitilin jäljellä oleva saldo voidaan kuitata nimellä "maksut/palkkiot"

Ongelmat:

1. Voit luoda useampia KP- tai pankkitunnuksia, jos käsittelet useaa maksupalvelun tarjoajaa. Myyntitilaukset [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa tukevat kuitenkin vain yhtä maksutapakoodia, mikä vaikeuttaa tapausten käsittelyä, kun ostaja käyttää useita tilauksen maksutapoja.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
