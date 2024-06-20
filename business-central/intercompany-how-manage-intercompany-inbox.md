---
title: Konsernin Saapuneet- ja Lähtevät-kansion hallinta
description: 'Kumppaneilta vastaanotetut konsernitapahtumat näkyvät konsernin Saapuneet-kansiossa, jossa voit käsitellä niitä manuaalisesti tai automaattisesti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# Konsernin Saapuneet- ja Lähtevät-kansion hallinta

Kumppaneilta saamasi konsernin tapahtumat näkyvät **Konsernin Saapuneet** -sivulla. Jos haluat tietää, miten saapuvia konsernin tapahtumia käsitellään, siirry [Saapuvien konsernitapahtumien käsitteleminen](#process-incoming-intercompany-transactions) -kohtaan. Kumppaneille lähettämät konsernin tapahtumat näkyvät **Konsernin Lähtevät** -sivulla. Jos haluat tietää, miten lähteviä konsernin tapahtumia käsitellään, siirry [ Lähtevien konsernitapahtumien käsitteleminen](#to-process-outgoing-intercompany-transactions) -kohtaan.

Konsernin sisäisten asetusten mukaan jotkin tapahtumat kuitenkin käsitellään automaattisesti. Voit määrittää lähdeyrityksen ja kumppaniyritykset luomaan automaattisesti asiakirjoja ja päiväkirjoja, jotka vastaavat tapahtumia, joita kumppanit lähettävät konsernin yleisen päiväkirjan kautta. Saat lisätietoja konsernin päiväkirjojen käyttämisestä valitsemalla [Voit täyttää ja kirjata konsernin päiväkirjan seuraavasti](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## Saapuneet-kansion järjestäminen  

Saapuneet-sivun yläosassa näkyvien suodatinkenttien avulla voit määrittää, mitkä tapahtumat näkyvät sivulla. Jos esimerkiksi haluat tarkastella vain tietyn kumppanin luomia tapahtumia, voit käyttää **Tapahtuman lähde**- ja **Konsernikumppanin koodi** -suodattimia.  

### Tapahtuman lähde  

Tapahtumalle tehtävissä olevat toimet määräytyvät sen mukaan, onko tapahtuma  

* konsernikumppanin luoma  
* konsernikumppanin hylkäämä ja palauttama.  

Voit suodattaa **Näytä tapahtuman lähde** -kentän avulla **Konsernin Saapuneet-kansion tapahtumat** -sivua siten, että vain yksi näistä tapahtumatyypeistä näkyy sivulla. Voit käyttää suodatusperusteena myös konsernikumppania tai **Rivitoiminto**-kentän sisältöä.  

#### Konsernikumppanin luoma  

 Kumppanin luoman uuden tapahtuman vastaanottaja voi

* hyväksyä tapahtuman  
* hylätä tapahtuman (palauttaa tapahtuman kumppanille)  
* peruuttaa tapahtuman (poistaa tapahtuman palauttamatta sitä kumppanille)  

#### Konsernikumppanin palauttama  

Jos konsernikumppani hylkää tapahtuman, peruuta tapahtuma Saapuneet-kansiossa. Tämän jälkeen sinun täytyy luoda korjausrivejä tai peruuttaa päiväkirja tai asiakirja omassa yrityksessä.  

## Saapuneet-kansion tapahtumien luominen uudelleen  

Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

## Konsernin tapahtumien jaksokohtaisen yleiskuvauksen tarkasteleminen  

Voit tarkastella kaikkien sellaisten tapahtumien yleiskuvausta, jotka olet lähettänyt ja vastaanottanut tietyn jakson aikana. **Konsernin tapahtumat** -raportissa mainitaan kaikki konsernin KP-tapahtumat, asiakastapahtumat ja toimittajatapahtumat.

> [!NOTE]  
> Jos konsernikumppanit ovat samassa tietokannassa, kumppanit voivat automaattisesti hyväksyä tapahtumia. Siirry suoraan **Konsernin Saapuneet-kansion käsitellyt tapahtumat** ja **Konsernin Lähtevät-kansion käsitellyt tapahtumat** -sivuille. Saat lisätietoja tapahtumien automaattisesta hyväksymisestä valitsemalla [Hyväksy tapahtumia automaattisesti konsernikumppaneilta](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Ota synkronointikumppania varten käyttöön **Konsernin asetukset** -sivulla **Tapahtumien automaattinen lähetys** -vaihto.
> * Ota kumppaniyrityksiä varten käyttöön **Konsernikumppani** -sivulla **Tapahtumien automaattinen hyväksyntä** -vaihto.  

## Konsernitapahtumien tuominen tiedostosta

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Jos konsernikumppani ja oma yritys ovat eri tietokannoissa, voit vastaanottaa konsernin tapahtumia kyseiseltä kumppanilta .xml-tiedostona. Tapahtumat täytyy tämän jälkeen tuoda Saapuneet-kansioon.  

1. Tallenna tiedosto sijaintiin, jonka olet määrittänyt **Konsernin Saapuneet-kansion tiedot** -kentässä konsernitapahtumien asettamisen aikana.  
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.
3. Valitse **Konsernin Saapuneet-kansion tapahtumat** -sivulla **Tuo tapahtumatiedosto** -toiminto.  
4. Valitse avautuvalla sivulla tapahtumat sisältävä .xml-tiedosto ja valitse **Avaa**.  

Tapahtumat tuodaan Saapuneet-kansioon. Niitä voi nyt käsitellä.

## Saapuvien konsernitapahtumien käsitteleminen  

Konsernikumppanien sinulle lähettämät konsernin tapahtumat tulevat konsernin Saapuneet-kansioon. Jokainen Saapuneet-kansion tapahtuma täytyy arvioida ja käsitellä erikseen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.  
2. Käsittele rivi valitsemalla **Konsernin Saapuneet-kansion tapahtumat** -sivulla ensin rivi ja sitten toiminto, kuten **Hyväksy**.
3. Täytä **Tot. kons. Saap.-kansion toim.** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **OK**-painike.  

Yrityksessäsi luodaan asiakirja- tai päiväkirjarivejä hyväksymillesi riveille. Avaa kukin asiakirja tai päiväkirja, tee tarvittavat muutokset ja kirjaa ne.  

Rivit, jotka hylkäät ja palautat kumppanille, siirtyvät konsernin Lähtevät-kansioon, jossa voit lähettää ne kumppanille.

Riveille, jotka kumppani hylkäsi ja palautti sinulle, on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.

## Lähtevien konsernitapahtumien käsitteleminen  

Kun kirjaat konsernin päiväkirjan tai asiakirjan tai lähetät konsernin tilausvahvistuksen, tapahtumat siirtyvät konsernin Lähtevät-kansioon. Kun haluat lähettää ne konsernikumppaneille, avaa Lähtevät-kansio ja käsittele ne.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Lähtevät-kansion tapahtumat** ja valitse sitten vastaava linkki.  
2. Käsittele rivi valitsemalla **Konsernin Lähtevät-kansion tapahtumat** -sivulla ensin rivi ja sitten toiminto, kuten **Palaa Saapuneet-kansioon**.

Käytä **Lähetä konsernikumppanille** -toimintoa, kun haluat lähettää rivejä asianomaisen kumppanin Saapuneet-kansioon.

**Palaa Saapuneet-kansioon** -toiminnolla rivit siirretään Saapuneet-kansioon, jossa voit sitten hyväksyä ne. Omaan yritykseen luoda sitten vastaavat asiakirja- tai päiväkirjarivit.  

Jos käytät **Peruuta**-toimintoa, on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.  

## Konsernin Saapuneet-kansion tapahtumien luominen uudelleen  

Haluat ehkä luoda tapahtuman uudelleen Saapuneet- tai Lähtevät-kansioon. Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

Seuraavissa ohjeissa neuvotaan, kuinka Saapuneet-kansion tapahtumia voi luoda uudelleen. Samoja ohjeita voi kuitenkin soveltaa myös Lähtevät-kansioon.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käsitellyt konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.  
2. Valitse **Käsitellyt konsernin Saapuneet-kansion tapahtumat** -sivulla rivi, jossa on Saapuneet-kansioon uudelleen luotava tapahtuma. Valitse sitten **Luo Saapuneet-kansion tapahtuma uudelleen** -toiminto.  

## Katso myös

[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
