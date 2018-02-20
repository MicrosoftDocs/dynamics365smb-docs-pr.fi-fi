---
title: "Vaihekuvaus – Myyntikampanjan suorittaminen | Microsoft Docs"
description: "Kampanja voi olla mikä tahansa toimi, jossa on mukana useita kontakteja. Kampanjan määrittämisen tärkeä osa liittyy kampanjan kohderyhmän valitsemiseen. Sitä varten Finance and Operations, Business editionissa luodaan segmentti tai yhteystietoryhmä suodattimien avulla."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e933115531f9adb0296ad8983be00da480f11f25
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Vaihekuvaus: Myyntikampanjan suorittaminen
Kampanja voi olla mikä tahansa toimi, jossa on mukana useita kontakteja. Kampanjan määrittämisen tärkeä osa liittyy kampanjan kohderyhmän valitsemiseen. Tätä tarkoitusta varten [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa luodaan segmentti tai yhteystietoryhmä suodattimien avulla.  

 Näitä toimintoja voi käyttää Myynti ja markkinointi -moduulissa, kun haluat suunnitella markkinointitoimenpiteet huolellisesti ja hallita vuorovaikutusta, jonka toisena osapuolena ovat kontaktit ja asiakkaat. Voit luoda kampanjoita ja määrittää kontaktien segmenttejä niin postituksia varten kuin muitakin sellaisia vuorovaikutustilanteita varten, joissa toinen osapuoli on kontakti tai mahdollinen asiakas.  

 Kampanja- ja Segmentti-toiminnoilla ja niiden automaattisten prosessien avulla voit suunnitella, järjestää ja seurata markkinointitoimenpiteitä. Tällä tavoin uusien asiakkaiden saamisen ja aiempien asiakkaiden säilymisen mahdollisuudet paranevat.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa havainnollistetaan messutapahtuman seurantatoimia sekä jatkokampanjan kohdistamista mahdollisiin asiakkaisiin (kontakteihin).  

 Vaihekuvauksessa esitellään Myynti ja markkinointi -osaston kampanjoiden- ja segmenttienhallintatoiminto. Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   kampanjan määrittäminen  
-   kohderyhmän valitseminen  
-   tietojen louhinta  
-   kirjeiden lähettäminen kontakteille  
-   kampanjareaktioiden rekisteröinti.  

## <a name="roles"></a>Roolit  
 Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   markkinointi- tai myyntipäällikkö  
-   markkinointityöntekijä.  

## <a name="prerequisites"></a>Vaatimukset  
 Asenna [!INCLUDE[d365fin](includes/d365fin_md.md)] ennen tämän vaihekuvauksen tehtävien suorittamista:  

## <a name="story"></a>Taustatietoja  
 CRONUSIN myyntiosaston markkinointipäällikkö vastaa kampanjoiden suunnittelemisesta ja toteuttamisesta. Hän tekee myös päätöksiä messuista, joihin yhtiö osallistuu, sekä arvioi kampanjan edistymistä.  

 Markkinointiosaston markkinointityöntekijä huolehtii markkinointiaineiston tuottamisesta, jakamisesta ja sijoittamisesta.  

 Yhtiö on juuri julkistanut uuden tuotteen, joka on nimeltään Millennium Server. Tuotetta on hiljattain esitelty Computer Futurus -messuilla. Monet asiakkaat olivat erittäin kiinnostuneita tuotteesta, ja myyntiä edistettiin myymällä Millennium Server -tuotetta asiakkaille kampanjan aikana erityiseen kampanjahintaan.  

 Mahdollisten asiakkaiden lisääminen kontakteiksi järjestelmään kuuluu markkinointityöntekijän messujen jälkeisiin työtehtäviin.  

 Markkinointipäällikkö järjestää kampanjan, luo segmentin, joka sisältää kaikki uudet kontaktit, ja valitsee sitten kampanjan kohderyhmän louhimalla kontaktitietoja.  

 Työntekijä auttaa lähettämään kiitoskirjeitä kontakteille, jotka jättivät korttinsa henkilökunnalle messujen aikana. Lopuksi päällikkö kirjaa kaikki mahdollisilta asiakkailta saadut vastaukset.  

## <a name="setting-up-a-campaign"></a>Kampanjan määrittäminen  
 Kun työntekijä on lisännyt messuilla saatujen käyntikorttien tiedot, markkinointipäällikkö määrittää kampanjan kortin kampanjaan liittyvien toimien hallintaa varten.  

### <a name="to-set-up-a-campaign"></a>Kampanjan määrittäminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kampanjat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi kampanja valitsemalla **Uusi**-toiminto. Paina kampanjan kortissa Enter, jos haluat, että kampanjanumero lisätään automaattisesti.  
3.  Lisää kampanjan kuvaus **Kuvaus**-kenttään. Kuvaus voi olla esimerkiksi **FUTURUS-messut**.  
4.  Napsauta **Tilakoodi**-kenttää ja valitse tilakoodi näkyviin tulevassa **Kampanjan tila** -luettelossa.  
5.  Täytä kampanjan **Aloituspvm**- ja **Lopetuspvm**-kenttien tiedot asiaankuuluvalla tavalla.  

## <a name="selecting-the-target-audience"></a>Kohderyhmän valitseminen  
 Luomalla segmentin markkinointipäällikkö valitsee kontaktit, joiden kanssa hän haluaa olla vuorovaikutuksessa.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Asianmukaiset kontaktit sisältävän segmentin luominen  

1.  Valitse **Segmentit**-toiminto.  
2.  Luo uusi segmentti valitsemalla **Uusi**-toiminto. Paina segmentin kortissa Enter, jos haluat, että segmenttinumero lisätään automaattisesti.  
3.  Kirjoita **Yleinen**-pikavälilehden **Kuvaus**-kenttään esimerkiksi **FUTURUS-messujen kävijät**.  

     Kun olet lisännyt yleiset segmenttiä koskevat tiedot, valitse segmenttiin sisällytettävät kontaktit.  

     Kontaktien valinnassa voi käyttää erilaisia kriteereitä, esimerkiksi asiakkaan tai mahdollisen asiakkaan toimipaikassa työskenteleviä kontaktihenkilöitä, jotka vastaavat yrityksensä ostoista.  

     Käytä suodattimia lisätäksesi kontakteja sinun tarkoituksiisi parhaiten sopivien ehtojen mukaan. Kontakteja lisätään suodatinten avulla esimerkiksi kontaktihenkilön vastuualueen tai kontaktiyrityksen liikesuhteen tai toimialan perusteella. Valitse kontaktit tässä vaihekuvauksessa valitsemalla **Vastuualue**-suodatin.  

4.  Avaa **Lisää kontakteja** -suodatin valitsemalla **Segmentti**-ikkunassa **Lisää kontakteja**.  
5.  Valitse **Vastuualue**-pikavälilehdessä **Tehtävän vastuualuekoodi** -asetukseksi **Osto**-suodatin ja valitse **OK**.  

     **Segmentti**-ikkunassa on nyt luettelo lisäämääsi suodattimeen perustuvista kontakteista. **Yleiset**-pikavälilehden **Rivien lukumäärä** -kentässä näkyy niiden kontaktien määrä, otka täyttävät nämä ehdot.  

    > [!NOTE]  
    >  Voit tallentaa segmentin kriteerin myöhempää käyttöä varten.

    1.  Valitse **Segmentti**-ikkunassa ensin **Segmentti**-toiminto ja sitten **Tallenna kriteeri** -toiminto.  
    2.  Anna **Tallenna segmentin kriteeri** -ikkunassa segmentin koodi. Syötä **Kuvaus**-kenttään segmentointikriteerien kuvaus.
    3.  Valitse **OK**-painike.  

## <a name="mining-the-data"></a>Tietojen louhinta  
 Markkinointipäällikkö tarkastelee segmentoitua kontaktiluetteloa lähemmin ja havaitsee, että luettelo on aivan liian laaja. Hän päättääkin pienentää luetteloa sen mukaan, mitkä ovat todellisia mahdollisia asiakkaita, jotta painopiste on varmasti oikeassa kohderyhmässä. Tätä tietojen uudelleenmäärittämistä ja karsimista kutsutaan myös tietojen louhinnaksi.  

### <a name="to-remove-contacts-from-the-segment"></a>Kontaktien poistaminen segmentistä  

1.  Avaa **Poista kontaktit - Vähennä** -ikkuna valitsemalla **Segmentti**-ikkunassa ensin **Kontaktit**-toiminto ja sitten **Vähennä kontakteja** -toiminto.  
2.  Valitse **Liikesuhde**-pikavälilehdessä **Liikesuhteen koodi** -asetukseksi **MAHD.**-suodatin ja valitse **OK**.  

     Karsittu kontaktien luettelo näkyy nyt **Segmentti**-ikkunassa. **Rivien lukumäärä** -kentässä näkyy niiden kontaktien määrä, jotka ovat nyt näiden kriteerien mukaisia.  

    > [!NOTE]  
    >  Jos kontaktien ryhmän poistaminen täytyy syystä tai toisesta peruuttaa, voit käyttää **Mene takaisin** -toimintoa. Et toisin sanoen voi kumota viimeistä segmentointia.  
    >   
    >  Valitse **Segmentti**-ikkunassa ensin **Segmentti**-toiminto ja sitten **Takaisin**-toiminto.  
    >   
    >  Yhteystiedot, jotka olet juuri poistanut lisätään takaisin yhteystietojen luetteloon.  

## <a name="linking-a-segment-to-a-campaign"></a>Segmentin yhdistäminen kampanjaan  
 Markkinointipäällikkö päättää, että karsittu luettelo on kampanjan lopullinen kontaktiluettelo. Hän yhdistää tämän segmentin FUTURUS-messut-kampanjaan.  

### <a name="to-link-a-segment-to-the-campaign"></a>Segmentin yhdistäminen kampanjaan  

1.  Valitse kampanja, johon segmentti on tarkoitus yhdistää, napsauttamalla **Segmentti**-ikkunan **Kampanja**-pikavälilehdessä **Kampanjan Nro**-kenttää. Kampanja voi olla esimerkiksi **CP0001**.  
2.  Koska tämä segmentti on kampanjan kohde, valitse **Kampanjan kohde** -valintaruutu.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Kirjeet ja sähköpostiviestit lähetetään yhteystiedoille  
 Työntekijä auttaa markkinointipäällikköä lähettämään mahdollisille asiakkaille kirjeitä, joissa heitä kiitetään messukäynnistä.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Lähetä kirje yhteyshenkilölle segmentin avulla  

1.  Avaa **FUTURUS-messujen kävijät** -segmentin **Segmentti**-kortti.  
2.  Valitse **Vuorovaikutus**-pikavälilehden **Vuorovaikutusmallin koodi** -kentässä Liikekirje (**LIIKET**) -malli.  
3.  Kirjoita **Aihe (oletus)** -kenttään esimerkiksi **Kiitos messukäynnistä**.  

    > [!NOTE]  
    >  Tässä mallissa on useita liiteasiakirjoja, joista jokainen on kirjoitettu eri kielellä. Mukana ovat esimerkiksi englanti ja tanska.  

4.  Avaa **Segmentin vuorovaikutuskielet** -ikkuna napsauttamalla **Kielikoodi (oletus)** -kentän alanuolta. Valitse kielikoodi ja sitten **OK**-painike.  
5.  Voit näyttää asiakirjan valitulla kielellä. Valitse ensin **Liite**-toiminto ja sitten **Avaa**-toiminto.  

     Vastaa viestiin, jossa pyydetään lupaa käynnistää Word valitsemalla **Salli tämä käyttöliittymän istunto** -vaihtoehto.  

     Tämä avaa liitetyn Word-asiakirjan tarkasteltavaksi. Voit myös käyttää tämän mahdollisuuden muokata kirjettä. Kun olet valmis, sulje Word.  

6.  Lisää kirjeen aihe **Aihe**-kenttään mallia varten valitulla kielellä.  
7.  Valitse **Loki**-toiminto.
8.  Valitse **Lähetä liitteitä** -valintaruutu liitteiden tulostamiseksi.  

    1. Valitse **Luo seurantasegmentti** -valintaruutu.  
    2. Aloita **Lokisegmentti**-eräajo valitsemalla **OK**.  

9. Liitteet lähetetään. Kun prosessi on valmis, valitse **OK** -painike viestille, joka ilmoittaa, että segmentti on kirjattu lokiin.  

     Kirjeet tulostetaan automaattisesti ja segmentti kirjataan lokiin. Koska segmentti on kirjattu lokiin, ei ole enää segmenttien luettelossa, vaan siirretty luetteloon lokiin kirjatuista segmenteistä. Saat luettelon näkyviin valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoittamalla **Lokiin kirjatut segmentit** ja valitsemalla sitten aiheeseen liittyvän linkin.  

10. Kun segmentti kirjataan lokiin, jokainen lähetetty kirje tallennetaan vuorovaikutuksena, jossa voit tarkastella lokia.  

     Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vuorovaikutuslokin tapahtumat** ja valitse sitten aiheeseen liittyvä linkki. Jokaiselle lähetetylle kirjeelle on olemassa merkintä.  

### <a name="to-send-an-email-message-to-a-contact"></a>Lähetä sähköpostiviesti yhteyshenkilölle  

1.  Valitse **Vuorovaikutus**-pikavälilehden **Vuorovaikutusmallin koodi** -kentässä Liikekirje (**LIIKET**) -malli.  
2.  Kirjoita **Aihe (oletus)** -kenttään esimerkiksi **Kiitos messukäynnistä**.  
3.  Valitse **Yhteydenpidon tyyppi** -kentässä **Sähköposti**.  
4.  Määritä kieliasetukset, kuten edellä.  
5.  Valitse **Loki**-toiminto. **Lokin segmentti**-luetteloikkuna aukeaa.  
6.  Liitteet lähetetään sähköpostitse, kun valitset **Lähetä liitteitä** -valintaruudun.  
7.  Valitse **Luo seurantasegmentti** -valintaruutu.  
8.  Valitse **OK**-painike.  

     Kirjeet lähetetään automaattisesti sähköpostilla ja segmentti kirjataan lokiin. Koska segmentti on kirjattu lokiin, ei ole enää segmenttien luettelossa, vaan tallennettu luetteloon lokiin kirjatuista segmenteistä. Saat luettelon näkyviin valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoittamalla **Lokiin kirjatut segmentit** ja valitsemalla sitten aiheeseen liittyvän linkin.  

## <a name="registering-campaign-responses"></a>Kampanjareaktioiden rekisteröiminen  
 Mahdolliset asiakkaat vastaavat kirjeeseen seuraavien kahden viikon aikana. Markkinointipäällikkö haluaa pitää kirjaa vastauksista ja kirjata nämä vuorovaikutukset ohjelmaan.  

 Määritä tätä tarkoitusta varten segmentti kontakteille, jotka ovat vastanneet kirjeeseen.  

### <a name="to-register-campaign-responses"></a>Kampanjareaktioiden rekisteröiminen  

1.  Valitse **Segmentti**-ikkunan **Vuorovaikutus**-pikavälilehti.  
2.  Valitse **Vuorovaikutusmallin koodi** -kenttä.  

     Kampanjareaktioiden tallentamista varten ei ole vuorovaikutusmallia. Luo siksi uusi työtuntimalli.  

3.  Valitse **Vuorovaikutusmallit**-ikkunassa **Uusi**-toiminto.  
4.  Lisää **Koodi**-kenttään **REAKT.** ja **Kuvaus**-kenttään **Kampanjareaktiot**.  
5.  Valitse **OK**-painike.  
6.  Valitse tämä vuorovaikutusmalli **Vuorovaikutusmallin koodi** -kentässä ja vahvista sanoma, jossa kysytään, haluatko päivittää segmenttirivit samalla vuorovaikutusmallin koodilla.  

     Määritä nyt, että nämä kontaktit ovat vastanneet kampanjaan:  
7.  Täytä **Kampanja**-pikavälilehden **Kampanjanro**-kenttään kampanja.  
8.  Siirry pois **Kampanjanro**-kentästä ja vahvista sanoma, jossa kysytään, haluatko päivittää segmenttirivit samalla vuorovaikutusmallin koodilla.  
9. Valitse **Kampanjareaktio**-kenttä ja vahvista seuraava sanoma.  

     Kirjaa segmentti lokiin sen varmistamiseksi, että vuorovaikutukset tulevat kirjatuiksi:  
10. Valitse **Segmentti**-ikkunassa **Loki**-toiminto.  
11. Poista **Lokin segmentti** -ikkunan **Lähetä liitteet** -valintaruudun valinta, valitse **OK** ja vahvista näkyviin tuleva sanoma.  

     Kun segmentti on kirjattu lokiin, ohjelma luo kampanjalle automaattisesti tapahtuman **Kampanjan tapahtumat** -ikkunaan näiden toimien kirjaamista varten.  

## <a name="see-also"></a>Katso myös  
[Kontaktienhallinta](marketing-relationship-management.md)  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

