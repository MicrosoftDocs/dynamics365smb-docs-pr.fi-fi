---
title: 'Vaihekuvaus: Myyntikampanjan suorittaminen'
description: 'Tässä vaihekuvauksessa on yksityiskohtainen yleiskuvaus kaikista tehtävistä, jotka liittyvät myyntikampanjan toteuttamiseen Business Centralissa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-conducting-a-sales-campaign"></a><a name="walkthrough-conducting-a-sales-campaign"></a><a name="walkthrough-conducting-a-sales-campaign"></a>Vaihekuvaus: Myyntikampanjan suorittaminen

Kampanja voi olla mikä tahansa toimi, jossa on mukana useita kontakteja. Kampanjan määrittämisen tärkeä osa liittyy kampanjan kohderyhmän valitsemiseen. Tätä tarkoitusta varten [!INCLUDE[prod_short](includes/prod_short.md)]:ssa luodaan segmentti tai yhteystietoryhmä suodattimien avulla.  

 Näitä toimintoja voi käyttää Myynti ja markkinointi -moduulissa, kun haluat suunnitella markkinointitoimenpiteet huolellisesti ja hallita vuorovaikutusta, jonka toisena osapuolena ovat kontaktit ja asiakkaat. Voit luoda kampanjoita ja määrittää kontaktien segmenttejä niin postituksia varten kuin muitakin sellaisia vuorovaikutustilanteita varten, joissa toinen osapuoli on kontakti tai mahdollinen asiakas.  

 Kampanja- ja Segmentti-toiminnoilla ja niiden automaattisten prosessien avulla voit suunnitella, järjestää ja seurata markkinointitoimenpiteitä. Tällä tavoin uusien asiakkaiden saamisen ja aiempien asiakkaiden säilymisen mahdollisuudet paranevat.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

 Tässä vaihekuvauksessa havainnollistetaan messutapahtuman seurantatoimia sekä jatkokampanjan kohdistamista mahdollisiin asiakkaisiin (kontakteihin).  

 Vaihekuvauksessa esitellään Myynti ja markkinointi -osaston kampanjoiden- ja segmenttienhallintatoiminto. Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- Tietojen valmisteleminen.
- kampanjan määrittäminen  
- kohderyhmän valitseminen  
- tietojen louhinta  
- kirjeiden lähettäminen kontakteille  
- kampanjareaktioiden rekisteröinti.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Roolit

 Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- markkinointi- tai myyntipäällikkö  
- markkinointityöntekijä.  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Vaatimukset

 Asenna [!INCLUDE[prod_short](includes/prod_short.md)] ennen tämän vaihekuvauksen tehtävien suorittamista:  

## <a name="story"></a><a name="story"></a><a name="story"></a>Taustatietoja

 CRONUS:n myyntiosaston markkinointipäällikkö vastaa kampanjoiden suunnittelemisesta ja toteuttamisesta. Markkinointipäällikkö tekee myös päätöksiä messuista, joihin yhtiö osallistuu, sekä arvioi kampanjan edistymistä.  

 Markkinointiosaston markkinointityöntekijä huolehtii markkinointiaineiston tuottamisesta, jakamisesta ja sijoittamisesta.  

 Yhtiö on juuri julkistanut uuden tuotteen, joka on nimeltään Rome Guest Chair. Tuotetta on hiljattain esitelty Office Futurus -messuilla. Monet asiakkaat olivat erittäin kiinnostuneita tuotteesta, ja myyntiä edistettiin myymällä Rome Guest Chair -tuotetta asiakkaille kampanjan aikana erityiseen kampanjahintaan.  

 Mahdollisten asiakkaiden lisääminen kontakteiksi järjestelmään kuuluu markkinointityöntekijän messujen jälkeisiin työtehtäviin.  

 Markkinointipäällikkö järjestää kampanjan, luo segmentin, joka sisältää kaikki uudet kontaktit, ja valitsee sitten kampanjan kohderyhmän louhimalla kontaktitietoja.  

 Työntekijä auttaa lähettämään kiitoskirjeitä kontakteille, jotka jättivät korttinsa henkilökunnalle messujen aikana. Lopuksi päällikkö kirjaa kaikki mahdollisilta asiakkailta saadut vastaukset.  

## <a name="setting-up-a-campaign"></a><a name="setting-up-a-campaign"></a><a name="setting-up-a-campaign"></a>Kampanjan määrittäminen

 Kun työntekijä on lisännyt messuilla saatujen käyntikorttien tiedot, markkinointipäällikkö määrittää kampanjan kortin kampanjaan liittyvien toimien hallintaa varten.  

### <a name="to-set-up-a-campaign"></a><a name="to-set-up-a-campaign"></a><a name="to-set-up-a-campaign"></a>Kampanjan määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kampanjat** ja valitse sitten vastaava linkki.  
2. Luo uusi kampanja valitsemalla **Uusi**-toiminto. Paina kampanjakortissa <kbd>Enter</kbd>-näppäintä, jos haluat lisätä kampanjanumeron automaattisesti.  
3. Lisää kampanjan kuvaus **Kuvaus**-kenttään. Kuvaus voi olla esimerkiksi **Office Futurus -messut**.  
4. Valitse **Tilakoodi**-kenttä ja valitse tilakoodi "1-PLAN". 
5. Täytä kampanjan **Aloituspvm**- ja **Lopetuspvm**-kenttien tiedot asiaankuuluvalla tavalla.  

## <a name="selecting-the-target-audience"></a><a name="selecting-the-target-audience"></a><a name="selecting-the-target-audience"></a>Kohderyhmän valitseminen

 Luomalla segmentin markkinointipäällikkö valitsee kontaktit, joiden kanssa hän haluaa olla vuorovaikutuksessa.  
 
 Kun luot segmentin, voit valita eri kriteerien avulla ne yhteystiedot, joiden on oltava segmentin kohteita. Voit valita esimerkiksi yhteyshenkilöitä, jotka työskentelevät asiakkaan toimipaikassa tai mahdollisen asiakkaan toimipaikassa tai henkilöitä, jotka vastaavat yrityksensä ostoista. Käytä suodattimia lisätäksesi kontakteja sinun tarkoituksiisi parhaiten sopivien ehtojen mukaan. Kontakteja lisätään suodatinten avulla esimerkiksi kontaktihenkilön vastuualueen tai kontaktiyrityksen liikesuhteen tai toimialan perusteella. Tässä vaihekuvauksessa valitsemme **Vastuualue**-suodattimen valituille yhteyshenkilöille.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a><a name="to-create-a-segment-with-the-relevant-contacts"></a><a name="to-create-a-segment-with-the-relevant-contacts"></a>Asianmukaiset kontaktit sisältävän segmentin luominen

1. Valitse ensin **Navigoi**-toiminto ja sitten **Segmentit**.  
2. Luo uusi segmentti valitsemalla **Uusi**-toiminto. Valitse segmentin kortissa **Enter** jos haluat, että segmenttinumero lisätään automaattisesti.  
3. Kirjoita **Yleinen**-pikavälilehden **Kuvaus**-kenttään esimerkiksi *Office Futurus -messujen kävijät*.
4. Valitse **Lisää kontakteja** -toiminto avataksesi **Lisää kontakteja** -suodattimen.  
5. Vieritä alaspäin **Kontaktin tehtäväalue** -pikavälilehteen, valitse **Osto**-suodatin **Tehtävän vastuualuekoodi**ksi ja valitse **OK**-painike.  

**Segmentti**-sivulla on nyt luettelo lisäämääsi suodattimeen perustuvista kontakteista. **Yleiset**-pikavälilehden **Rivien lukumäärä** -kentässä näkyy niiden kontaktien määrä, otka täyttävät nämä ehdot.  

> [!NOTE]  
> Voit tallentaa segmentin kriteerin myöhempää käyttöä varten.

### <a name="to-save-your-segmentation-criteria"></a><a name="to-save-your-segmentation-criteria"></a><a name="to-save-your-segmentation-criteria"></a>Segmentointikriteerien tallentaminen

1. Valitse **Segmentti**-sivulla **Toiminnot**.
2. Valitse **Toiminnot**, sitten **Segmentti** ja valitse sitten **Tallenna kriteeri** -toiminto.  
3. Anna **Tallenna segmentin kriteeri** -sivulla segmentin koodi. Syötä **Kuvaus**-kenttään segmentointikriteerien kuvaus.
4. Valitse **OK**-painike.  

## <a name="mining-the-data"></a><a name="mining-the-data"></a><a name="mining-the-data"></a>Tietojen louhinta

 Markkinointipäällikkö tarkastelee segmentoitua kontaktiluetteloa lähemmin ja havaitsee, että luettelo on aivan liian laaja. Päällikkö päättääkin pienentää luetteloa sen mukaan, mitkä ovat todellisia mahdollisia asiakkaita, jotta painopiste on varmasti oikeassa kohderyhmässä. Tätä tietojen uudelleenmäärittämistä ja karsimista kutsutaan myös tietojen louhinnaksi.  

### <a name="to-remove-contacts-from-the-segment"></a><a name="to-remove-contacts-from-the-segment"></a><a name="to-remove-contacts-from-the-segment"></a>Kontaktien poistaminen segmentistä

1. Valitse **Segmentti**-sivulla **Toiminnot**.
2. Valitse alla olevassa valikkopalkissa **Toiminnot**, valitse **Yhteystiedot** ja valitse sitten **Vähennä kontakteja**.  

  Tämä avaa **Poista kontaktit – Vähennä** -dialogin.  
4. Valitse **Kontakti liikesuhde** -pikavälilehdessä **CUST** -suodatin **Liikesuhteen koodi**iksi ja valitse **OK**-painike..

 Karsittu kontaktien luettelo näkyy nyt **Segmentti**-sivulla. **Rivien lukumäärä** -kentässä näkyy niiden kontaktien määrä, jotka ovat nyt näiden kriteerien mukaisia.  

 > [!NOTE]  
 > Jos kontaktien ryhmän poistaminen täytyy syystä tai toisesta peruuttaa, voit käyttää **Mene takaisin** -toimintoa. Et toisin sanoen voi kumota viimeistä segmentointia.  

### <a name="to-bring-back-the-removed-contacts"></a><a name="to-bring-back-the-removed-contacts"></a><a name="to-bring-back-the-removed-contacts"></a>Poistettujen yhteystietojen palauttaminen

1. Valitse **Segmentti**-sivulla **Segmentti**-toiminto.
2. Valitse **Mene takaisin**-toiminto.

Yhteystiedot, jotka olet juuri poistanut lisätään takaisin yhteystietojen luetteloon.

## <a name="linking-a-segment-to-a-campaign"></a><a name="linking-a-segment-to-a-campaign"></a><a name="linking-a-segment-to-a-campaign"></a>Segmentin yhdistäminen kampanjaan

Markkinointipäällikkö päättää, että karsittu luettelo on kampanjan lopullinen kontaktiluettelo. Näin ollen he yhdistävät tämän segmentin FUTURUS-messut-kampanjaan.  

### <a name="to-link-a-segment-to-the-campaign"></a><a name="to-link-a-segment-to-the-campaign"></a><a name="to-link-a-segment-to-the-campaign"></a>Segmentin yhdistäminen kampanjaan

1. Valitse kampanja, johon segmentti on tarkoitus yhdistää, valitsemalla **Segmentti**-sivun **Kampanja**-pikavälilehdessä **Kampanjan Nro**-kenttä. Kampanja voi olla esimerkiksi **CP0001**.
2. Valitse **Kyllä**.  
3. Koska tämä segmentti on kampanjan kohde, valitse **Kampanjan kohde** -valintaruutu ja valitse **Kyllä**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a><a name="sending-letters-and-email-messages-to-contacts"></a><a name="sending-letters-and-email-messages-to-contacts"></a>Kirjeet ja sähköpostiviestit lähetetään yhteystiedoille

 Työntekijä auttaa markkinointipäällikköä lähettämään mahdollisille asiakkaille kirjeitä, joissa heitä kiitetään messukäynnistä.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a><a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a><a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Lähetä kirje yhteyshenkilölle segmentin avulla

> [!NOTE]  
> Tässä menettelyssä on liitettävä Word-asiakirja. Voit lisätä liitteitä millä tahansa kielellä.

> [!NOTE]  
> Napsauta tarvittaessa **Muokkaa kynä** -kuvaketta ja avaa sivu muokkaustilassa.

1. Avaa **FUTURUS-messujen kävijät** -segmentin **Segmentti**-kortti.  
2. Valitse **Vuorovaikutus** -pikavälilehden **Vuorovaikutusmallin koodi** -kentässä liikekirjeiden mallikoodi **LIIKET** ja valitse **Kyllä**.
3. Avaa **Segmentin vuorovaikutuskielet** -sivu valitsemalla **Kielikoodi (oletus)** -kenttä. Valitse **Kielikoodi** ja sitten **OK**-painike.
4. Varmista, että **Yhteydenpidon tyyppi (oletus)** on asetuksessa **Paperituloste**.
5. Valitse **Liite**-kentässä **Ellipsi**-ruutu. Näyttöön tulee valintaikkuna Tuo liite.
    1. Valitse tiedostosi painikkeesta **Valitse**.
    1. Etsi tiedosto ja valitse **Avaa** -painike liittääksesi sen.
6. Kirjoita **Aihe (oletus)** -kenttään esimerkiksi **Kiitos messukäynnistä**. Poistu kentästä <kbd>Sarkain</kbd>-näppäimellä ja valitse **Kyllä**.
7. Liu'uta **Lähetä Word-asiakirjoja liitteinä** päälle ja valitse **Kyllä**-painike.
8. Valitse **Loki**-toiminto. Lokin segmentin ponnahdusikkunassa ota käyttöön: **Luo seurantasegmentti**
9. Valitse **OK**-painike, niin **Lokisegmentin eräajo** käynnistyy.  

Liitteet lähetetään. Kun prosessi on valmis, valitse **OK** -painike viestille, joka ilmoittaa, että segmentti on kirjattu lokiin.  

 Kirjeet tulostetaan automaattisesti ja segmentti kirjataan lokiin. Koska segmentti on kirjattu lokiin, ei ole enää segmenttien luettelossa, vaan siirretty luetteloon lokiin kirjatuista segmenteistä. Luettelon nähdäksesi valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lokiin kirjatut segmentit** ja valitse sitten vastaava linkki.  

Kun segmentti kirjataan lokiin, jokainen lähetetty kirje tallennetaan vuorovaikutuksena, jossa voit tarkastella lokia.  

Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vuorovaikutuslokin tapahtumat** ja valitse sitten vastaava linkki. Jokaiselle lähetetylle kirjeelle on olemassa merkintä.  

### <a name="to-send-an-email-message-to-a-contact"></a><a name="to-send-an-email-message-to-a-contact"></a><a name="to-send-an-email-message-to-a-contact"></a>Lähetä sähköpostiviesti yhteyshenkilölle

1. Valitse **Vuorovaikutus**-pikavälilehden **Vuorovaikutusmallin koodi** -kentässä Liikekirje (**LIIKET**) -malli.  
2. Kirjoita **Aihe (oletus)** -kenttään esimerkiksi **Kiitos messukäynnistä**.  
3. Valitse **Yhteydenpidon tyyppi** -kentässä **Sähköposti**.  
4. Määrittele kieliasetukset ja liitä Word-asiakirja edellisten ohjeiden mukaisesti.  
5. Valitse **Loki**-toiminto. **Lokin segmentti** -sivu avautuu.  
6. Liitteet lähetetään sähköpostitse, kun valitset **Lähetä liitteitä** -valintaruudun.  
7. Valitse **Luo seurantasegmentti** -valintaruutu.  
8. Valitse **OK**-painike.  

 Kirjeet lähetetään automaattisesti sähköpostilla ja segmentti kirjataan lokiin. Koska segmentti on kirjattu lokiin, ei ole enää segmenttien luettelossa, vaan tallennettu luetteloon lokiin kirjatuista segmenteistä. Luettelon nähdäksesi valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lokiin kirjatut segmentit** ja valitse sitten vastaava linkki.  

## <a name="registering-campaign-responses"></a><a name="registering-campaign-responses"></a><a name="registering-campaign-responses"></a>Kampanjareaktioiden rekisteröiminen

 Mahdolliset asiakkaat vastaavat kirjeeseen seuraavien kahden viikon aikana. Markkinointipäällikkö haluaa pitää kirjaa vastauksista ja kirjata nämä vuorovaikutukset ohjelmaan.  

 Määritä tätä tarkoitusta varten segmentti kontakteille, jotka ovat vastanneet kirjeeseen.  

### <a name="to-register-campaign-responses"></a><a name="to-register-campaign-responses"></a><a name="to-register-campaign-responses"></a>Kampanjareaktioiden rekisteröiminen

1. Valitse **Segmentti**-sivun **Vuorovaikutus**-pikavälilehdessä **Vuorovaikutusmallin koodi** -kenttä.  

 Kampanjareaktioiden tallentamista varten ei ole vuorovaikutusmallia. Luo siksi uusi työtuntimalli.  

2. Valitse avattavasta luettelosta **Vuorovaikutusmallit** toiminto **Uusi**.  
3. Lisää **Koodi**-kenttään **REAKT.** ja **Kuvaus**-kenttään **Kampanjareaktiot**.  
4. Valitse **OK**-painike.
5. Valitse **Kyllä**, kun haluat vahvistaa, että haluat kohdistaa tämän vuorovaikutusmallikoodin kaikkiin segmenttiriveihin.
6. Valitse **Kampanja**-pikavälilehden **Kampanjapalaute**-kenttä. Valitse **Kyllä** vahvistaaksesi sanoman *Olet muokannut kampanjapalautetta*.  
7. Valitse **Segmentti**-sivulla **Loki**-toiminto.  
8. Tyhjennä **Lokin segmentti** -sivulla **Lähetä liitteet** -valintaruutu. Valitse sitten **OK**-painike vahvistaaksesi sanoman siitä, että segmentti on kirjattu lokiin.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös
[Liikesuhteiden hallinta](marketing-relationship-management.md)  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
