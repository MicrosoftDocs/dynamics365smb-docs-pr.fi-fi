---
author: brentholtorf
ms.topic: include
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista. Niiden avulla voit myös laskea viivästyskuluja, kuten korkoja tai lisämaksuja, ja sisällyttää ne muistutukseen.

> [!TIP]
> Vaikka tässä artikkelissa olevat tiedot ovat oikeita, siinä kuvaillaan lähinnä manuaalista prosessia. [!INCLUDE [prod_short](prod_short.md)]issa on työkaluja, joilla voidaan automatisoida muistutusten luonti-, julkaisu- ja lähetysprosessit. Näiden vaiheiden automatisointi voi säästää merkittävästi perintään käytettyä aikaa. Lisätietoja on kohdassa [Perinnän muistutusten automatisointi](../finance-automate-reminders.md).

Ennen kuin voit luoda muistutuksia, sinun on määritettävä muistutusehdot ja määritettävä ne asiakkaille. Lisätietoja on ohjeaiheessa [Muistutusehtojen ja -tasojen määrittäminen](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] – **Viivästyskuluehdot-sivu määrittää**, lasketaanko muistutukseen korot.  

Voit ajaa **Luo muistutukset** -eräajon säännöllisin väliajoin ja luoda näin muistutukset kaikille asiakkaille, joilla on erääntyneitä saldoja, tai voit luoda muistutuksen tietylle asiakkaalle manuaalisesti ja antaa ohjelman laskea ja täyttää sen rivit automaattisesti.  

Muistutusten luomisen jälkeen voit muokata niitä. Kunkin muistutuksen alussa ja lopussa näkyvä teksti määräytyy muistutustason ehtojen mukaan, ja sen voi nähdä **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä muistutuksen teksti** -toiminnon käyttämistä.  

Asiakastapahtuma, jolla on **Estossa**-kenttä valittuna, ei aiheuta muistutuksen luomista. Jos muistutus kuitenkin luodaan toisen tapahtuman perusteella, pidossa olevaksi merkitty erääntynyt tapahtuma sisällytetään muistutukseen. Näiden tapahtumien riveille ei lasketa korkoa.

Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset – yleensä sähköpostina.

### Muistutusten luominen automaattisesti

Muistutus on vastaava kuin lasku. Kun luot muistutuksen, muistutuksen otsikko ja vähintään yksi muistutusrivi on oltava lisättynä. Voit luoda toiminnolla muistutuksia kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 0.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse **Muistutus**-sivulla **Luo muistutuksia** -toiminto.
3. Täytä **Luo muistutukset** -sivulla kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
4. Valitse **OK**-painike.

### Muistutusten luominen manuaalisesti

Voit täyttää **Muistutus**-sivulla **Yleiset**-pikavälilehden tiedot manuaalisesti, jonka jälkeen rivit täytetään automaattisesti.

1. Valitse ![Lamppu, joka avaa uudelleen Kerro-ominaisuuden 2.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Valitse **Ehdota muistutusrivejä** -toiminto.
5. Täytä **Ehdota muistutusrivejä** -eräajossa kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
6. Valitse **Sisällytä pidossa olevat tapahtumat** -valintaruutu, jos haluat muistutusten sisältävän erääntyneet, pidossa olevat avoimet tapahtumat.
7. Valitse **Vain tapahtumat, joissa erääntyneitä määriä** -valintaruutu, jos haluat muistutusten sisältävän vain erääntyneet avoimet tapahtumat. Vain laskut ja maksut näytetään, koska nämä ovat tapahtumia, joista asiakkaiden maksut voivat olla myöhässä.

    > [!Important]
    > Pidossa olevat avoimet tapahtumat lisätään riippumatta **Vain tapahtumat, joissa on erääntyneitä summia** -asetuksen tilasta.

8. Valitse **OK**-painike.

### Muistutustekstien vaihtaminen

On monta tapaa määrittää teksti, joka näkyy tulostetussa muistutuksessa. Joskus voit haluta korvata nykyiselle luokalle määritetyt alku- ja lopputekstit eri luokkien teksteillä.

1. Valitse ![Lamppu, joka avaa vielä uudelleen Kerro-ominaisuuden 3.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Avaa sopiva muistutus ja valitse sitten **Päivitä muistutusteksti** -toiminto.
3. Anna **Päivitä muistutusteksti** -sivun **Muistutustaso**-kentässä tarvittava taso.
4. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.

### Muistutuksen lähettäminen

Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset.

Kun lähetät muistutuksen, tiedot siirretään erilliseen lähetettyjen muistutusten sivulle. Samalla muistutuksen tapahtumat kirjataan. Jos muistutukseen on laskettu korkoja tai lisämaksuja, tapahtumat kirjataan asiakastapahtumiin ja pääkirjanpitoon.

Kun muistutus lähetetään, tapahtumat kirjataan **Muistutusehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Muistutusehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumamerkinnät**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi muistutuksen lähettämisestä voi seurata ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa myös tässä Kerro-ominaisuuden 4.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse ensin soveltuva muistutus ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä muistutukset** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Muistutus on joko tulostettu lähettäväksi määritettyyn sähköpostiin PDF-liitteenä.

### Lähetetyn muistutuksen peruuttaminen

Jos muistutukset lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.

1. Valitse **Lähetetyt muistutukset** -sivulla vähintään yhden peruutettavan lähetetyn muistutuksen rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt muistutukset** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.


