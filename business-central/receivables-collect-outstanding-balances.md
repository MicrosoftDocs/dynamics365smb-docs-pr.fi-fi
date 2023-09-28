---
title: Avointen saldojen perintä
description: 'Tutustu siihen, miten voit muistuttaa asiakkaista erääntyneistä maksuista. Lähetä asiakastiliote, muistutus tai viivästyskululasku.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 02/09/2022
ms.author: bholtorf
---
# Avointen saldojen perintä

Myyntisaamisten hallintaan kuuluu sen tarkistaminen, onko erääntyneet summat maksettu ajoissa. Jos asiakkailla on erääntyneitä maksuja, voit aloittaa lähettämällä heille **Asiakkaan tiliote** -raportin muistutuksena. Vaihtoehtoisesti voit lähettää muistutuksia.

Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista. Niiden avulla voit myös laskea viivästyskuluja, kuten korkoja tai lisämaksuja, ja sisällyttää ne muistutukseen. Käytä viivästyskululaskuja, jos haluat veloittaa asiakkailta korkoja tai maksuja muistuttamatta erääntyneistä summista.

## Tiliotteet

Asiakaskortissa voit luoda ilmoituksen asiakkaan kanssa tapahtuville tapahtumille. Tämän jälkeen lähetät asiakkaalle luodun PDF-tiedoston. Vaihtoehtoisesti **asiakastiliotteen** avulla voit lähettää asiakkaille yleiskatsauksen liiketoiminnasta kanssasi. Asiakastiliotteen voi lähettää Exceliin jatkokäsittelyä varten.  

### Asiakkaan tilioteraportin lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaan tiliote** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Tulostusvaihtoehdot**-kohdassa, miten raportti lähetetään asiakkaalle.

> [!NOTE]
> Jos käytössä on useita valuuttoja, asiakkaan tiliotteen raportti tulostetaan aina asiakkaan valuuttana. Tiliotteen päivämääränä ja erääntymispäivämääränä, jos erääntyminen otetaan huomioon, käytetään tiliotteen kauden viimeistä päivämäärää.

## Muistutukset

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## Viivästyskulut

Jos asiakas ei suorita maksua eräpäivään mennessä, voit antaa ohjelman laskea viivästyskulut automaattisesti ja lisätä ne asiakkaan tilin erääntyneisiin summiin. Voi antaa asiakkaille tiedon lisätyistä kuluista lähettämällä viivästyskululaskuja.  

> [!NOTE]  
> Käyttämällä viivästyskululaskuja voit laskea korot ja viivästyskulut sekä antaa niistä tiedon asiakkaille muistuttamatta erääntyneistä maksuista. Vaihtoehtoisesti voit laskea erääntyneiden maksujen koron muistutusten luomisen yhteydessä.  

Ennen viivästyskululaskujen luomista sinun täytyy määrittää ehdot. Lisätietoja on ohjeaiheessa [Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md).  

Voit luoda yksittäiselle asiakkaalle viivästyskululaskun manuaalisesti ja täyttää rivit automaattisesti. Vaihtoehtoisesti voit luoda **Luo viivästyskululasku** -toiminnon avulla viivästyskululaskut kaikille asiakkaille tai valituille asiakkaille, joilla on erääntyneitä saldoja.  

Viivästyskululaskujen luomisen jälkeen voit muokata niitä. Kunkin viivästyskululaskun alussa ja lopussa näkyvä teksti määräytyy viivästyskuluehtojen mukaan, ja tekstin voi nähdä rivien **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä lisäkulun teksti** -toiminnon käyttämistä.  

Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut – yleensä sähköpostina.

### Viivästyskululaskujen luominen manuaalisesti

Viivästyskululasku on samanlainen kuin tavallinen lasku. Voit täyttää otsikon manuaalisesti ja antaa ohjelman täyttää rivit, tai voit antaa ohjelman luoda viivästyskululaskut kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.  
3. Valitse **Ehdota lisäkululaskurivejä** -toiminto.
4. Määritä suodatin **Ehdota lisäkululaskurivejä** -sivun **Asiakastapahtuma**-pikavälilehdessä, jos haluat luoda viivästyskululaskuja vain tietyille tapahtumille.

    > [!NOTE]
    > Vaikka ne on luetteloitu, **Maksun** ja **Hyvityslaskun** valitseminen **Asiakirjatyyppi**-suodattimiksi ei vaikuta siihen, koska **Ehdota viivästyskululaskun rivejä** -toiminto käsittelee vain positiivisia määriä.
5.  Aloita eräajo valitsemalla **OK**.  

### Viivästyskululaskutekstien päivitys  
Joskus voit haluta muuttaa viivästyskuluehtoihin määrittämiäsi alku- ja lopputekstejä. Jos teet tämän silloin, kun olet luonut viivästyskululaskut – mutta et vielä lähettänyt niitä, voit antaa ohjelman päivittää muutetut tekstit laskuihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululasku** ja valitse sitten vastaava linkki.  
2. Avaa viivästyskululaskun, jonka tekstiä haluat muuttaa, ja valitse sitten **Päivitä lisäkulun teksti** -toiminto.
3. Voit määrittää **Päivitä lisäkulun teksti** -sivulla suodattimen, jos haluat päivittää useita laskuja.
4. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.  

### Viivästyskululaskujen lähettäminen
Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut.

Kun muistutus lähetetään, tapahtumat kirjataan **Viivästyskuluehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Viivästyskuluehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumat**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi viivästyskululaskun lähettämisen seurauksena voi olla ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululaskut** ja valitse sitten vastaava linkki.
2. Valitse ensin soveltuva lasku ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä viivästyskululaskut** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Viivästyskululasku on joko tulostettu tai lähetetty määritettyyn sähköpostiin PDF-liitteenä.

### Lähetetyn viivästyskululaskun peruuttaminen
Jos viivästyskululaskut lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.
1. Valitse **Lähetetyt viivästyskululaskut** -sivulla vähintään yhden peruutettavan viivästyskululaskun rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt viivästyskululaskut** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

### Muistutus-/Viivästyskulutapahtumien katsominen  
Kun lähetät muistutuksen, muistutustapahtuma luodaan **Muistutus-/viivästyskulutap.**-sivulle kullekin asiakastapahtuman sisältävälle muistutusriville. Voit sitten hakea tietyn asiakkaan muistutustapahtumien yleiskuvauksen.    
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Tapahtumakirjaukset**-toiminto.
3. Valitse **Asiakastapahtumat**-sivulla tapahtumarivi, jonka muistutukset haluat nähdä, ja valitse sitten **Muistutus-/viivästyskulutapah.**-toiminto.

## Useita korkoprosentteja

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]Lisätietoja on kohdassa [Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md).  

## Katso myös

[Muistutusehtojen ja -tasojen määrittäminen.](finance-setup-reminders.md)  
[Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
