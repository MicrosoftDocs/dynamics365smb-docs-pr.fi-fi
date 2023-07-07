---
title: Päivitä valuutanvaihtokurssit (sisältää videon)
description: 'Jos seuraat summia eri valuutoissa, voit antaa Business Centralin auttaa sinua säätämään FX-vaihtokursseja julkaistuille merkinnöille ulkoisen palvelun avulla.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen

Voit määrittää eri valuuttoja [!INCLUDE [prod_short](includes/prod_short.md)]issa esimerkiksi silloin, kun et tee kauppaa muussa valuutassa kuin paikallisessa valuutassa. Tämän jälkeen voit auttaa itseäsi seuraamaan valuutan vaihtokurssien muutoksia, kun hallitset valuuttoja manuaalisesti tai voit määrittää valuutan vaihtokurssipalvelun.

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

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen

Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä sovellukseen, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty.

**Muuta vaihtokursseja** -eräajon avulla voi muuttaa manuaalisesti kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia.  

> [!TIP]
> Voit käyttää palvelua vaihtokurssien päivittämiseen automaattisesti järjestelmässä. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Jos kirjattujen tapahtumien vaihtokursseja ei kuitenkaan silloin muuteta. Voit päivittää kirjattujen tapahtumien vaihtokurssit käyttämällä **Muuta vaihtokursseja** -erätyötä.

Voit esikatsella oikaisun vaikutusta kirjaukseen ennen kirjaamista valitsemalla **Esikatselu** **Muuta vaihtokursseja** -sivulla. Lisäksi voit määrittää, onko pääkirjanpidon kirjaus yksityiskohtainen (tapahtumakohtainen) vai yhteenveto (valuuttakohtainen) valitsemalla **Tee yhteenveto tapahtumista**. Voit myös määrittää, miten dimensioita käsitellään ei-realisoituneiden voittojen ja tappioiden kirjausten kohdalla valitsemalla jonkin **Siirrä dimensioarvot** -kentän seuraavista vaihtoehdoista:  

- **Lähdetapahtuma**: Ei-realisoituneiden voittojen ja tappioiden K/P-tapahtumien dimensioiden arvot siirretään oikaistusta tapahtumasta.
- **K/P-tilin mukaan**: Ei-realisoituneiden voittojen ja tappioiden K/P-tapahtumien dimensioiden arvot siirretään ei-realisoituneiden voittojen ja tappioiden K/P-tilien dimension asetusten lähdetapahtumasta.
- **Ei siirtoa**: Ei-realisoituneiden voittojen ja tappioiden K/P-tapahtumilla ei ole dimensioiden arvoja.

### <a name="effect-on-customers-and-vendors"></a>Vaikutus asiakkaisiin ja toimittajiin

Asiakkaan ja toimittajan tileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee yksittäisten valuuttasaldojen erot ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Ei-realisoit. val.voitt. tili** -kentässä tai **Ei-realisoit. val.voitt. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti ostoreskontran/myyntireskontran tilille pääkirjanpidossa.

Eräajo käsittelee kaikki avoimet asiakas- ja toimittajatapahtumat. Jos tapahtumassa on valuuttaero, eräajo luo uuden, eritellyn asiakas- tai toimittajatapahtuman, josta näkyy muutettu summa asiakas- tai toimittajatapahtumassa.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Asiakas- ja toimittajatapahtumien dimensiot

Muutostapahtumille on määritetty dimensiot asiakas-/toimittajatapahtumilta, ja muutokset on kirjattu dimensioarvojen kombinaatioiden mukaan.

### <a name="effect-on-bank-accounts"></a>Vaikutus pankkitileihin

Pankkitileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee eron jokaiselle tilille, jolla on valuuttakoodi ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Realisoitun. val.voitt. tili** -kentässä tai **Realisoit. val.tapp. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti niille KP:n pankkitileille, jotka on määritelty pankkitilien postitusryhmissä. Eräajo laskee yhden tapahtuman valuuttaa ja kirjausryhmää kohden.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiot pankkitilitapahtumilla

Muutostapahtumien pankkitilin KP-tilille ja voitto/tappio tileille määritetään oletusdimensiot.

### <a name="effect-on-gl-accounts"></a>Vaikutus KP-tileihin
Jos kirjaat lisäraportointivaluutan, voit eräajon avulla luoda uusia KP-tapahtumia PVA:n ja lisäraportointivaluutan välillä tapahtuvia kurssimuutoksia varten. Eräajo laskee jokaisen kirjanpitotapahtuman erotuksen ja muuttaa kirjanpitotapahtumaa sen mukaan, mitä **Vaihtokurssin muutos** -kentässä lukee kirjanpitotilin kohdalla.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensiot KP-tilin tapahtumille
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

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Valuutat Business Centralissa](finance-currencies.md)  
[Valuuttojen määrittäminen](finance-set-up-currencies.md)  
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
