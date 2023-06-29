---
title: Vianmääritys ja dimensioiden korjaaminen
description: 'Lisätietoja tavallisten dimensiovirheiden vianmäärityksestä ja dimensioiden korjaamisesta sen jälkeen, kun niitä on käytetty kirjatuissa tapahtumissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 09/27/2021
ms.author: bholtorf
---

# <a name="troubleshooting-and-correcting-dimensions"></a><a name="troubleshooting-and-correcting-dimensions"></a>Vianmääritys ja dimensioiden korjaaminen

Talousraportointi ja analyysinäkymät perustuvat usein dimensioiden tietoihin. Käytettävissä olevista turvatoimista huolimatta tapahtuu joskus vahinkoja, jotka johtavat epätarkkuuksiin. Tässä ohjeaiheessa kuvataan joitakin tyypillisiä virheitä ja kerrotaan, miten kirjattujen tapahtumien dimensiomääritykset korjataan talousraporttien saattamiseksi ajan tasalle.

## <a name="troubleshooting-dimensions-errors"></a><a name="troubleshooting-dimensions-errors"></a>Dimensiovirheiden vianmääritys

Kun kirjaat dimensioita sisältäviä asiakirja- ja päiväkirjarivejä, erilaisia virheitä voi esiintyä. Yleensä nämä virheet liittyvät kuitenkin dimension virheelliseen määrittämiseen tai määrittelyyn.

> [!NOTE]
> Seuraavassa mahdollisten virhesanomien luettelossa, *%X*-koodit ovat tietomuuttujien paikkamerkkejä, jonka varsinainen sanoma sisältää tilannekohtaisen käyttöliittymän mukaan. Esimerkiksi *%1 %2 on estetty.* voisi näkyä käyttöliittymässä muodossa Dimensiokoodialue on estetty.  

|Ongelma|Virhesanoma|Mahdollinen ratkaisu|
|-----|-------------|-----------------|
|Estetty dimensio|%1 %2 on estetty.|-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on estetty dimensio, ja poista sen esto.<br />-Poista estetyn dimension dimensiojoukon rivi.|
|Poistettu dimensio|%1 %2 ei löydy.|-Palauta puuttuva dimensio.<br />-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on puuttuva dimensio, ja lisää se.<br />-Poista puuttuvan dimension dimensiojoukon rivi.|
|Estetty dimensioarvo|%1 %2 - %3 on estetty.|-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on estetty dimensioarvo, ja poista sen esto.<br />-Poista estetyn dimensioarvon dimensiojoukon rivi.|
|Poistettu dimensioarvo|    Kohteen %2 %1 puuttuu.|-Palauta puuttuva dimensioarvo.<br />-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on puuttuva dimensioarvo, ja lisää se.<br />-Poista puuttuvan dimensioarvon dimensiojoukon rivi.|
|Ei-sallittu dimensioarvo.|Kohteen %1 %2 - %3 dimensioarvon tyyppi ei saa olla %4.|-Muuta **Dimensioarvot**-sivun **Dimension arvotyyppi** -kentän arvoksi **Vakio** tai **Alkusumma**.<br />-Poista estetyn dimensioarvon dimensiojoukon rivi.|
|Estetty dimensioyhdistelmä|Dimensioita %1 ja %2 ei voida käyttää yhtäaikaisesti.|-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on estetty dimensioyhdistelmä, ja poista sen esto.<br />-Muokkaa yhtä dimensioyhdistelmän ristiriitaista käyttöoikeuksien joukon riviä.|
|Estetty dimensioarvoyhdistelmä|Dimensioiden yhdistelmiä %1 - %2 ja %3 - %4 ei voida käyttää yhtäaikaisesti.|-Etsi kirjaamattomia asiakirjoja, jotka sisältävät dimensiojoukon, jossa on estetty dimensioarvoyhdistelmä, ja poista sen esto.<br />-Muokkaa yhtä dimensioarvoyhdistelmän ristiriitaista käyttöoikeuksien joukon riviä.|
|Oletusdimension tyhjä dimensioarvon koodi, jossa **Arvon kirjaaminen** -kentässä on **Koodi pakollinen**|-Valitse yksi %1 kohteelle %2 %3.<br />-Valitse yksi %1 kohteelle %2 %3 kohteelle %4 %5.|-Muuta **Arvon kirjaaminen** -kenttä **Oletusdimensio**-sivulla.<br />-Anna jokin muu kuin tyhjä dimensioarvo dimensiojoukon ristiriitaiselle dimensiolle.|
|Oletusdimension väärä dimensioarvon koodi, jossa **Arvon kirjaaminen** -kentässä on **Sama koodi**|-Valitse %1 %2 kohteelle %3 %4.<br />-Valitse %1 %2 kohteen %3 %4 kohteelle %5 %6|-Muuta **Arvon kirjaaminen** -kenttä **Oletusdimensio**-sivulla.<br />-Anna pakollinen dimensioarvo dimensiojoukon ristiriitaiselle dimensiolle.|
|Tyhjän oletusdimension muu kuin tyhjä dimensioarvon koodi, jossa **Arvon kirjaaminen** -kentässä on **Sama koodi**|-%1 %2 tulee olla tyhjä.<br />-%1 %2 on oltava tyhjä kohteille %3 %4.|-Muuta **Arvon kirjaaminen** -kenttä **Oletusdimensio**-sivulla.<br />-Anna tyhjä dimensioarvon koodi dimensiojoukon ristiriitaiselle dimensiolle.|
|Oletusdimension odottamaton dimensioarvo jossa **Arvon kirjaaminen** -kentässä on **Ei koodia**|-%1 %2 ei tule mainita.<br />-%1 %2 ei tule mainita kohteille %3 %4|-Muuta **Arvon kirjaaminen** -kenttä **Oletusdimensio**-sivulla.<br />-Poista ristiriitainen rivi dimensioyhdistelmästä.|
|Dimension korjausta ei suoriteta loppuun oikein.||-Palauta korjaus luonnostilaan valitsemalla **Palauta**. Muutokset nollataan ja korjaus voidaan suorittaa uudelleen.|

## <a name="changing-dimension-assignments-after-posting"></a><a name="changing-dimension-assignments-after-posting"></a>Dimensiomääritysten muuttaminen kirjauksen jälkeen

Jos huomataan, että kirjatuissa kirjanpitotapahtumissa on käytetty virheellistä dimensiota, dimension arvot voidaan korjata ja analyysinäkymät päivittää. Tällä tavoin talousraportit ja analyysit pysyvät tarkkoina.

> [!IMPORTANT]
> Dimensioiden korjaamisen ominaisuuksien tavoite on saattaa talousraportointi ajan tasalle. Dimensioiden korjaukset koskevat vain KP-tapahtumia. Ne eivät muuta saman tapahtuman muiden kirjanpitojen tapahtumiin määritettyjä dimensioita. Pääkirjanpitoon ja alikirjanpitoon liitettyjen dimensioiden välillä siis on ristiriita.

### <a name="setting-up-dimension-corrections"></a><a name="setting-up-dimension-corrections"></a>Dimension korjausten määrittäminen

Dimension korjauksia määritettäessä on otettava huomioon kaksi seikkaa:

* Ovatko jotkin dimensiot sellaisia, joita muuttamista ei haluta sallia? Määritä **Dimension korjauksen asetukset** -sivulla dimensiot, joissa haluat estää muutokset.
* Kuka saa muuttaa dimensioita? Käyttäjät, jolle on määritetty **D365 DIMENSIOIDEN KORJAUS** -oikeus, voivat tehdä muutoksia. Näillä oikeuksilla voidaan luoda dimension korjauksia, suorittaa niitä ja kumota ne tarvittaessa. Niillä voidaan myös määrittää estetyt dimensiot. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a><a name="correcting-a-dimension"></a>Dimension korjaaminen

Voit valita manuaalisesti vähintään yhden kirjanpitotapahtuman tai voit valita tapahtumajoukon suodattamia käyttämällä. Voit tarvittaessa myös lisätä tai poistaa dimensioita. 

1. Voit aloittaa dimension korjauksen jollakin seuraavista sivuista:

    * Valitse **KP-rekisteri**-sivulla ensin rekisteri ja sitten **Korjaa dimensiot** -toiminto. Valitun rekisterin tapahtumien korjaus käynnistyy.
    * Valitse **Kirjanpitotapahtumat**-sivulla **Dimension korjaus** -toiminto. 

2. Kirjoita **Kuvaus**-kenttään muutosta koskevia tietoja. Nämä tiedot auttavat myöhemmin muita käyttäjiä hahmottamaan, mitä on tehty.
3. Valitse **Valitut kirjanpitotapahtumat** -pikavälilehdessä soveltuvat tapahtumat.

    > [!IMPORTANT]
    > Kun valintaa muutetaan, **Dimension korjauksen asetukset** -pikavälilehden arvot nollataan. Tämän vuoksi tapahtumat on valittava aina ennen dimensioarvojen muutosten määrittämistä.

   Asetukset kuvaillaan seuraavassa taulukossa.

   |Asetus  |Kuvaus  |
   |---------|---------|
   |Lisää liittyvät tapahtumat     |Lisää KP-tapahtumat, jotka ovat samassa KP-rekisterissä.|   
   |Lisää suodattimen mukaan     |Käytä suodatusehtoja KP-tapahtumia lisättäessä.|
   |Manuaalinen valinta     |Valitse tietyt KP-tapahtumat.         |
   |Lisää dimensioittain     |Suodata KP-tapahtumia dimensioiden perusteella.         |
   |Poista tapahtumat     |Poista KP-tapahtumien valinta.         |
   |Hallitse valintaehtoja     |Seuraa valintaprosessia ja kumoa valinnat tarvittaessa.         |

4. Valitse **Dimension korjauksen muutokset** -pikavälilehdessä dimensio, jonka haluat muuttaa **Dimension koodi** -kenttää, uusi **Uusi dimension arvokoodi** -kentän arvo.
5. Korjauksen voi vahvistaa valitsemalla **Vahvista dimension muutokset**. Lisätietoja on kohdassa [Dimension korjausten vahvistaminen](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Valitse **Suorita**.

### <a name="validating-dimension-corrections"></a><a name="validating-dimension-corrections"></a>Dimension korjausten vahvistaminen

Korjaus kannattaa vahvistaa, ennen kuin se suoritetaan. Vahvistus tarkistaa KP-tilille kirjattavien arvojen rajoitukset ja dimensioiden rajoitukset sekä mahdollisesti estetyt dimension arvot. Vahvistuksen aikana korjauksen tilaksi on määritetty **Keskeneräinen vahvistus**. Kun korjaus on vahvistettu, tulos näytetään **Vahvistuksen tila** -kentässä. Jos virheitä löytyi, niihin voi perehtyä **Näytä virheet** -toiminnolla. Kun virhe on korjattu, käytä **Avaa uudelleen** -toimintoa korjauksen suorittamiseen tai uuden vahvistukseen.

Voit suorittaa korjauksen joko heti tai aikatauluttaa sen suorittavaksi myöhemmin. Jos korjauksia suoritetaan suuressa tietojoukossa, se kannattaa aikatauluttaa suoritettavaksi työajan ulkopuolella. Lisätietoja on kohdassa [Suurten tietojoukkojen dimension korjaukset](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a><a name="undoing-a-correction"></a>Korjauksen kumoaminen

Jos pidä dimension korjauksen tuloksesta, voit palauttaa aiemman arvon käyttämällä **Kumoa**-toimintoa. Kuitenkin vain viimeisin korjaus voidaan kumota. Voit vahvistaa ennen korjauksen kumoamista, mitkä muutokset kumoaminen tekee. Tämä on kätevää, jos esimerkiksi dimension rajoitukset ovat muuttuneet korjauksen jälkeen.

Jos kumoamistoiminto ei ole käytettävissä, koska korjauksia on tehty useita, samojen tapahtumien uusi korjaus voidaan aloittaa käyttämällä **Kopioi luonnokseen** -toimintoa.

### <a name="dimension-corrections-on-large-data-sets"></a><a name="dimension-corrections-on-large-data-sets"></a>Suurten tietojoukkojen dimension korjaukset

Suuria tapahtumajoukkoja, joissa on esimerkiksi yli 10 000 tapahtumaa, korjattaessa on syytä olla varovainen. Mikäli se on mahdollista, korjaukset kannattaa suorittaa pienemmiksi suodatetuissa tietojoukoissa. Lisäksi korjaukset kannattaa suorittaa normaalin työajan ulkopuolella. 

### <a name="use-analysis-views-with-dimension-corrections"></a><a name="use-analysis-views-with-dimension-corrections"></a>Analyysinäkymien käyttäminen dimension korjausten kanssa

Jos **Päivitä kirjattaessa** on otettu käyttöön analyysinäkymässä, [!INCLUDE[prod_short](includes/prod_short.md)] näkee, mitkä asiakirjat ja päiväkirjat on kirjattu. Myös näkymät voidaan päivittää, kun tämä asetus on otettu käyttöön dimension korjaustuloksissa. Asetus otetaan käyttöön **Päivitä analyysinäkymät**-vaihtopainikkeella. Analyysinäkymien päivittäminen voi vaikuttaa suorituskykyyn, etenkin jos kyse on suurista tietojoukoista, joten vain pienien tietojoukkojen analyysinäkymien päivittämistä suositellaan.  

### <a name="viewing-historical-dimension-corrections"></a><a name="viewing-historical-dimension-corrections"></a>Historiallisten dimension korjausten näyttäminen

Jos kirjapitotapahtuma on korjattu, muutosta voi tarkastella **Dimension korjaushistoria** -toiminnolla.

### <a name="handling-incomplete-corrections"></a><a name="handling-incomplete-corrections"></a>Keskeneräisten korjausten käsitteleminen

Jos korjaus on keskeneräinen, korjauskortissa näkyy varoitus. Korjauksen voi siinä tapauksessa palauttaa luonnostilaan ja muutokset kumota **Palauta**-toiminnolla. Korjauksen voi suorittaa sitten uudelleen.

> [!NOTE]
> Keskeneräisen korjauksen nollaaminen ei vaikuta analyysinäkymien päivityksiin, koska ne tehdään korjausprosessin lopussa.

### <a name="use-cost-accounting-with-corrected-gl-entries"></a><a name="use-cost-accounting-with-corrected-gl-entries"></a>Kustannuslaskennan käyttäminen korjatuissa KP-tapahtumissa

Dimensioiden korjauksen jälkeen kustannuslaskennan tiedot eivät ole synkronoituja. Kustannuslaskenta käyttää dimensioita koostamaan kustannuspaikkoja ja kustannuskohteita ja suorittamaan kustannusten kohdistamiset. KP-tapahtumien dimensioiden muuttaminen aiheuttaa todennäköisesti kustannuslaskentamallien uudelleensuorittamisen. Se, onko poistettava vain muutamia kustannusrekistereitä ja onko kohdistus suoritettava uudelleen vai onko kaikki poistettava ja kaikki mallit suoritettava uudelleen, perustuu tietoihin, jotka on päivitetty, ja siihen, miten kustannuslaskentaominaisuudet on määritetty. Sinun on manuaalisesti määritettävä, miten dimension korjaukset vaikuttavat kustannuslaskentaan ja missä päivityksiä tarvitaan. [!INCLUDE[prod_short](includes/prod_short.md)]issa ei ole tällä hetkellä tapaa tehdä tätä automaattisesti.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/dimensions-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Dimensioiden käyttäminen](finance-dimensions.md)  
[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
