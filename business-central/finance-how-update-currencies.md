---
title: Päivitä valuutanvaihtokurssit (sisältää videon)
description: 'Jos seuraat eri valuutoissa olevia summia, voit antaa Business Centralin auttaa sinua muuttamaan vaihtokursseja.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 09/07/2023
ms.author: bholtorf
---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen

Voit määrittää eri valuuttoja [!INCLUDE [prod_short](includes/prod_short.md)]issa esimerkiksi silloin, kun et tee kauppaa muussa valuutassa kuin paikallisessa valuutassa. Voit auttaa itseäsi seuraamaan valuutan vaihtokurssien muutoksia, kun hallitset valuuttoja manuaalisesti tai voit määrittää valuutan vaihtokurssipalvelun.

## <a name="currencies"></a>Valuutat

> [!TIP]  
> Jos etsit [!INCLUDE[prod_short](includes/prod_short.md)]issa reaaliajassa tietoa valuuttakurssien (FX) hinnoista tai historiallisista hinnoista, löydät sen nimityksellä valuutta. Tämän artikkelin lisäksi on artikkeli [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Valuuttakoodit määritetään **Valuutat**-luettelossa, mukaan lukien lisätiedot ja asetukset, jotka ovat välttämättömiä kunkin valuuttakoodin osalta. Lisätietoja on ohjeaiheessa [Valuutat](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Esimerkki saamisen valuuttatapahtumasta

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Vaihtokurssit

Vaihtokurssit ovat työkalu, jonka avulla lasketaan kunkin valuuttatapahtuman arvo paikallisessa valuutassa (PVA). **Vaihtokurssit**-sivulla on seuraavat kentät:

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Aloitustiedot**|Päivämäärä, jolloin valuuttakurssi on pantu toimeen|  
|**Valuutan koodi**|Tähän vaihtokurssiin liittyvä valuutan koodi|  
|**Suhteellinen valuuttakoodi**|Jos tämä valuutta on osa kolmenkeskistä valuuttalaskentaa, liittyvä valuuttakoodi voidaan määrittää tässä|  
|**Vaihtokurssisumma**|Vaihtokurssisumma on rivillä valitulle valuuttakoodille käytettävä kurssi. Normaalisti 1 tai 100|  
|**Suhteellinen vaihtokurssisumma**|Suhteellinen vaihtokurssisumma on rivillä valitulle suhteelliselle valuuttakoodille käytettävä kurssi.|  
|**Muutoksen vaihtokurssisumma**|Muutoksen vaihtokurssisumma on kurssi, jota käytetään valuuttakoodille, joka on valittuna rivillä **Muuta vaihtokursseja** -eräajoa varten|  
|**Suhteellinen vaihtokurssisumman muutos**|Suhteellinen vaihtokurssisumman muutos on kurssi, jota käytetään valuuttakoodille, joka on valittuna rivillä **Muuta vaihtokursseja** -eräajoa varten|  
|**Kiinteä vaihtokurssisumma**|Määrittää, voidaanko valuuttakurssia muuttaa laskuissa ja päiväkirjan riveillä.|  

Yleisesti arvoja **Vaihtokurssisumma**- ja **Suhteellinen vaihtokurssisumma** -kentissä käytetään oletusvaluuttakursseina kaikissa vastedes luotavissa myyntisaamisten ja ostovelkojen asiakirjoissa. Asiakirjalle määritetään valuuttakurssi tämänhetkisen käsittelypäivämäärän mukaan.  

> [!Note]
> Todellinen valuuttakurssi lasketaan tämän kaavan avulla:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Muutoksen vaihtokurssisummaa tai suhteellista vaihtokurssisumman muutosta käytetään kaikkein avoimien pankki-, saamis- ja ostovelkatransaktioiden päivittämiseen.  

> [!Note]
> Todellinen valuuttakurssi lasketaan tämän kaavan avulla:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Muutetaan vaihtokursseja

Koska vaihtokurssit vaihtelevat koko ajan, muita valuuttoja täytyy muuttaa jaksoittain. Jos et tee niin, ulkomaan valuutoista (tai muista) valuutoista muunnetut summat, jotka kirjattiin pääkirjanpitoon paikallisena valuuttana, voivat olla virheellisiä. Päivitä myös päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin syöttämistä.

**Muuta vaihtokursseja** -eräajon avulla voi muuttaa manuaalisesti kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Eräajo myös päivittää KP-tapahtumien lisäraportointivaluutan summat.  

> [!TIP]
> Voit käyttää palvelua vaihtokurssien päivittämiseen automaattisesti järjestelmässä. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Jos kirjattujen tapahtumien vaihtokursseja ei kuitenkaan silloin muuteta. Voit päivittää kirjattujen tapahtumien vaihtokurssit käyttämällä **Muuta vaihtokursseja** -erätyötä.

Voit myös määrittää, miten dimensioita käsitellään ei-realisoituneiden voittojen ja tappioiden kirjausten kohdalla valitsemalla jonkin **Dimension kirjaus** -kentän seuraavista vaihtoehdoista:  

* **Lähdetapahtumien dimensiot**: Siirrä ei-realisoituneiden voittojen ja tappioiden K/P-tapahtumien dimensioiden arvot oikaistusta tapahtumasta.  
* **Ei dimensioita**: Älä siirrä ei-realisoituneiden voittojen ja tappioiden dimensioarvoja K/P-tapahtumiin. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää edelleen oletusdimensioasetuksia, esimerkiksi **Koodi pakollinen**, **Sama koodi** tai **Ei koodia**. Jos lähdetapahtumamerkinnöillä on dimensioarvoja, muutos luo tapahtumia ilman dimensioarvoja.  
* **KP-tilin dimensiot**: Dimension arvojen siirtäminen ei-realisoituneiden voittojen ja tappioiden KP-tilin dimensioasetusten lähdetapahtumasta KP-tapahtumiin.

> [!NOTE]
> Jotta voit käyttää esikatseluominaisuutta, ota käyttöön **Ominaisuuspäivitys: Salli uuden laajennettavan vaihtokurssioikaisun (myös kirjauksen tarkistuksen) käyttö** -ominaisuus **[Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610)** -sivulla.

> [!IMPORTANT]
> Sveitsin paikallisten vaatimusten vuoksi emme suosittele, että otat käyttöön **Ominaisuuspäivitys: Salli uuden laajennettavan vaihtokurssioikaisun (myös kirjauksen tarkistuksen) käyttö** -ominaisuutta Sveitsin (CH) maaversiossa.

## <a name="preview-the-effect-of-an-adjustment"></a>Muutoksen vaikutuksen esikatselu

Voit esikatsella valuuttakurssin muutoksen vaikutusta kirjaukseen ennen varsinaista kirjausta valitsemalla **Esikatsele kirjausta** -toiminnon **Vaihtokurssien muutos** -raportin (Raportti 596) pyyntösivulla. Pyyntösivulla voit määrittää, mitä esiversioon sisällytetään:

* Yksityiskohtaisen kirjauksen hakeminen pääkirjanpitoon tapahtuman mukaan
* Tee yhteenveto kirjauksesta valuutoittain. Valitse vain **Muuta tapahtumakohtaisesti** -kenttä **Vaihtokurssien muutos** -raportista.

### <a name="effect-on-customers-and-vendors"></a>Vaikutus asiakkaisiin ja toimittajiin

Asiakkaan ja toimittajan tileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee yksittäisten valuuttasaldojen erot ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Ei-realisoit. val.voitt. tili** -kentässä tai **Ei-realisoit. val.voitt. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti ostoreskontran/myyntireskontran tilille pääkirjanpidossa.

Eräajo käsittelee kaikki avoimet asiakas- ja toimittajatapahtumat. Jos tapahtumassa on vaihtokurssiero, eräajo luo uuden yksityiskohtaisen asiakas- tai toimittajatapahtuman. Uusi tapahtuma kuvastaa muutettua summaa asiakas- tai toimittajatapahtumassa.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Asiakas- ja toimittajatapahtumien dimensiot

[!INCLUDE [prod_short](includes/prod_short.md)] määrittää dimensiot asiakas- tai toimittajatapahtumilta muutostapahtumiin, ja muutokset kirjataan dimensioarvojen kombinaatioiden mukaan.

### <a name="effect-on-bank-accounts"></a>Vaikutus pankkitileihin

Pankkitileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee eron jokaiselle tilille, jolla on valuuttakoodi ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Realisoitun. val.voitt. tili** -kentässä tai **Realisoit. val.tapp. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti niille KP:n pankkitileille, jotka on määritelty pankkitilien postitusryhmissä. Eräajo laskee yhden tapahtuman valuuttaa ja kirjausryhmää kohden.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiot pankkitilitapahtumilla

Muutostapahtumien pankkitilin KP-tilille ja voitto/tappio tileille määritetään oletusdimensiot.

### <a name="effect-on-gl-accounts"></a>Vaikutus KP-tileihin

Jos kirjaat toisen raportointivaluutan, voit eräajon avulla luoda uusia KP-tapahtumia paikallisen valuutan ja toisen raportointivaluutan välillä tapahtuvia kurssimuutoksia varten. Eräajo laskee jokaisen kirjanpitotapahtuman erotuksen ja muuttaa kirjanpitotapahtumaa sen mukaan, mitä **Vaihtokurssin muutos** -kentässä lukee kirjanpitotilin kohdalla.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensiot KP-tilin tapahtumille

Muutostapahtumille on määritetty niiden KP-tilien dimensiot, joille ne on kirjattu.

> [!Important]
> Syötä ennen eräajon käyttämistä vaihtokurssit, joita käytetään ulkomaisen valuutan saldoja muutettaessa. Se tehdään **Valuutan vaihtokurssit** -sivulla.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen

Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla. 

> [!NOTE]
> Useimmat vaihtokurssipalvelut sisältävät tietoja, jotka ovat yhteensopivia kohteen [!INCLUDE[prod_short](includes/prod_short.md)] tuontiprosessin kanssa. Joskus tiedot kuitenkin muotoillaan eri tavalla, ja sinun on mukautettava tuontiprosessia. Voit tehdä näin tiedonsiirtokehyksen avulla lisäämällä oman koodiyksikön. Tarvitset luultavasti kehittäjän apua. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Valuutanvaihdon kurssipalvelut** ja valitse liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Käytössä**-tilanvaihtonäppäin ottaaksesi palvelun käyttöön.

> [!NOTE]
> Seuraava video näyttää esimerkin siitä, miten voit muodostaa yhteyden valuutan vaihtokurssipalveluun. Esimerkissä käytetään Euroopan keskuspankkia. Segmentissä, joka kuvaa, miten kenttien yhdistämismääritykset tehdään, **Valuutan koodin pääsolmu** -kohdan **Lähde**-sarakkeen asetus palauttaa vain ensimmäisen löydetyn valuutan. Asetuksen on oltava `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten vastaava linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-also"></a>Katso myös

[Business Centralin valuutat](finance-currencies.md)  
[Valuuttojen määrittäminen](finance-set-up-currencies.md)  
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
