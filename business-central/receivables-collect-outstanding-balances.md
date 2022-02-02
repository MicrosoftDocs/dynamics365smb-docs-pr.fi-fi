---
title: Avointen saldojen perintä
description: Lue, miten asiakkaalle lähetetään muistutus erääntyvästä maksusta ja miten maksuun lisätään myöhästymismaksu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c3e4bc2b75133b0a46d3d5746841d6caf76589c
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971650"
---
# <a name="collect-outstanding-balances"></a>Avointen saldojen perintä

Myyntisaamisten hallintaan kuuluu sen tarkistaminen, onko erääntyneet summat maksettu ajoissa. Jos asiakkailla on erääntyneitä maksuja, voit aloittaa lähettämällä heille **Asiakkaan tiliote** -raportin muistutuksena. Vaihtoehtoisesti voit lähettää muistutuksia.

Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista. Niiden avulla voit myös laskea viivästyskuluja, kuten korkoja tai lisämaksuja, ja sisällyttää ne muistutukseen. Käytä viivästyskululaskuja, jos haluat veloittaa asiakkailta korkoja tai maksuja muistuttamatta erääntyneistä summista.

## <a name="statements"></a>Tiliotteet

Asiakaskortissa voit luoda ilmoituksen asiakkaan kanssa tapahtuville tapahtumille. Tämän jälkeen lähetät asiakkaalle luodun PDF-tiedoston. Vaihtoehtoisesti **asiakastiliotteen** avulla voit lähettää asiakkaille yleiskatsauksen liiketoiminnasta kanssasi. Asiakastiliotteen voi lähettää Exceliin jatkokäsittelyä varten.  

### <a name="to-send-the-customer-statement-report"></a>Asiakkaan tilioteraportin lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaan tiliote** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Tulostusvaihtoehdot**-kohdassa, miten raportti lähetetään asiakkaalle.

> [!NOTE]
> Jos käytössä on useita valuuttoja, asiakkaan tiliotteen raportti tulostetaan aina asiakkaan valuuttana. Tiliotteen päivämääränä ja erääntymispäivämääränä, jos erääntyminen otetaan huomioon, käytetään tiliotteen kauden viimeistä päivämäärää.

## <a name="reminders"></a>Muistutukset

Ennen kuin voit luoda muistutuksia, sinun on määritettävä muistutusehdot ja määritettävä ne asiakkaille. Lisätietoja on ohjeaiheessa [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] – **Viivästyskuluehdot-sivu määrittää**, lasketaanko muistutukseen korot.  

Voit ajaa **Luo muistutukset** -eräajon säännöllisin väliajoin ja luoda näin muistutukset kaikille asiakkaille, joilla on erääntyneitä saldoja, tai voit luoda muistutuksen tietylle asiakkaalle manuaalisesti ja antaa ohjelman laskea ja täyttää sen rivit automaattisesti.  

Muistutusten luomisen jälkeen voit muokata niitä. Kunkin muistutuksen alussa ja lopussa näkyvä teksti määräytyy muistutustason ehtojen mukaan, ja sen voi nähdä **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä muistutuksen teksti** -toiminnon käyttämistä.  

Asiakastapahtuma, jolla on **Estossa**-kenttä valittuna, ei aiheuta muistutuksen luomista. Jos muistutus kuitenkin luodaan toisen tapahtuman perusteella, pidossa olevaksi merkitty erääntynyt tapahtuma sisällytetään muistutukseen. Näiden tapahtumien riveille ei lasketa korkoa.

Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset – yleensä sähköpostina.

### <a name="to-create-a-reminder-automatically"></a>Muistutusten luominen automaattisesti

Muistutus on vastaava kuin lasku. Kun luot muistutuksen, muistutuksen otsikko ja vähintään yksi muistutusrivi on oltava lisättynä. Voit luoda toiminnolla muistutuksia kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse **Muistutus**-sivulla **Luo muistutuksia** -toiminto.
3. Täytä **Luo muistutukset** -sivulla kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
4. Valitse **OK**-painike.

### <a name="to-create-a-reminder-manually"></a>Muistutusten luominen manuaalisesti

Voit täyttää **Muistutus**-sivulla **Yleiset**-pikavälilehden tiedot manuaalisesti, jonka jälkeen rivit täytetään automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Valitse **Ehdota muistutusrivejä** -toiminto.
5. Täytä **Ehdota muistutusrivejä** -eräajossa kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
6. Valitse **Sisällytä pidossa olevat tapahtumat** -valintaruutu, jos haluat muistutusten sisältävän erääntyneet, pidossa olevat avoimet tapahtumat.
7. Valitse **Vain tapahtumat, joissa erääntyneitä määriä** -valintaruutu, jos haluat muistutusten sisältävän vain erääntyneet avoimet tapahtumat. Vain laskut ja maksut näytetään, koska nämä ovat tapahtumia, joista asiakkaiden maksut voivat olla myöhässä.

    > [!Important]
    > Pidossa olevat avoimet tapahtumat lisätään riippumatta **Vain tapahtumat, joissa on erääntyneitä summia** -asetuksen tilasta.

8. Valitse **OK**-painike.

### <a name="to-replace-reminder-texts"></a>Muistutustekstien vaihtaminen

On monta tapaa määrittää teksti, joka näkyy tulostetussa muistutuksessa. Joskus voit haluta korvata nykyiselle luokalle määritetyt alku- ja lopputekstit eri luokkien teksteillä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Avaa sopiva muistutus ja valitse sitten **Päivitä muistutusteksti** -toiminto.
3. Anna **Päivitä muistutusteksti** -sivun **Muistutustaso**-kentässä tarvittava taso.
4. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.

### <a name="to-issue-a-reminder"></a>Muistutuksen lähettäminen

Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset.

Kun lähetät muistutuksen, tiedot siirretään erilliseen lähetettyjen muistutusten sivulle. Samalla muistutuksen tapahtumat kirjataan. Jos muistutukseen on laskettu korkoja tai lisämaksuja, tapahtumat kirjataan asiakastapahtumiin ja pääkirjanpitoon.

Kun muistutus lähetetään, tapahtumat kirjataan **Muistutusehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Muistutusehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumamerkinnät**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi muistutuksen lähettämisestä voi seurata ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten vastaava linkki.
2. Valitse ensin soveltuva muistutus ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä muistutukset** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Muistutus on joko tulostettu lähettäväksi määritettyyn sähköpostiin PDF-liitteenä.

### <a name="to-cancel-an-issued-reminder"></a>Lähetetyn muistutuksen peruuttaminen

Jos muistutukset lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.

1. Valitse **Lähetetyt muistutukset** -sivulla vähintään yhden peruutettavan lähetetyn muistutuksen rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt muistutukset** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

## <a name="finance-charges"></a>Viivästyskulut

Jos asiakas ei suorita maksua eräpäivään mennessä, voit antaa ohjelman laskea viivästyskulut automaattisesti ja lisätä ne asiakkaan tilin erääntyneisiin summiin. Voi antaa asiakkaille tiedon lisätyistä kuluista lähettämällä viivästyskululaskuja.  

> [!NOTE]  
> Käyttämällä viivästyskululaskuja voit laskea korot ja viivästyskulut sekä antaa niistä tiedon asiakkaille muistuttamatta erääntyneistä maksuista. Vaihtoehtoisesti voit laskea erääntyneiden maksujen koron muistutusten luomisen yhteydessä.  

Ennen viivästyskululaskujen luomista sinun täytyy määrittää ehdot. Lisätietoja on ohjeaiheessa [Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md).  

Voit luoda yksittäiselle asiakkaalle viivästyskululaskun manuaalisesti ja täyttää rivit automaattisesti. Vaihtoehtoisesti voit luoda **Luo viivästyskululasku** -toiminnon avulla viivästyskululaskut kaikille asiakkaille tai valituille asiakkaille, joilla on erääntyneitä saldoja.  

Viivästyskululaskujen luomisen jälkeen voit muokata niitä. Kunkin viivästyskululaskun alussa ja lopussa näkyvä teksti määräytyy viivästyskuluehtojen mukaan, ja tekstin voi nähdä rivien **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä lisäkulun teksti** -toiminnon käyttämistä.  

Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut – yleensä sähköpostina.

### <a name="to-create-a-finance-charge-memo-manually"></a>Viivästyskululaskujen luominen manuaalisesti

Viivästyskululasku on samanlainen kuin tavallinen lasku. Voit täyttää otsikon manuaalisesti ja antaa ohjelman täyttää rivit, tai voit antaa ohjelman luoda viivästyskululaskut kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.  
3. Valitse **Ehdota lisäkululaskurivejä** -toiminto.
4. Määritä suodatin **Ehdota lisäkululaskurivejä** -sivun **Asiakastapahtuma**-pikavälilehdessä, jos haluat luoda viivästyskululaskuja vain tietyille tapahtumille.

    > [!NOTE]
    > Vaikka ne on luetteloitu, **Maksun** ja **Hyvityslaskun** valitseminen **Asiakirjatyyppi**-suodattimiksi ei vaikuta siihen, koska **Ehdota viivästyskululaskun rivejä** -toiminto käsittelee vain positiivisia määriä.
5.  Aloita eräajo valitsemalla **OK**.  

### <a name="to-update-finance-charge-memo-texts"></a>Viivästyskululaskutekstien päivitys  
Joskus voit haluta muuttaa viivästyskuluehtoihin määrittämiäsi alku- ja lopputekstejä. Jos teet tämän silloin, kun olet luonut viivästyskululaskut – mutta et vielä lähettänyt niitä, voit antaa ohjelman päivittää muutetut tekstit laskuihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululasku** ja valitse sitten vastaava linkki.  
2. Avaa viivästyskululaskun, jonka tekstiä haluat muuttaa, ja valitse sitten **Päivitä lisäkulun teksti** -toiminto.
3. Voit määrittää **Päivitä lisäkulun teksti** -sivulla suodattimen, jos haluat päivittää useita laskuja.
4. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.  

### <a name="to-issue-finance-charge-memos"></a>Viivästyskululaskujen lähettäminen
Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut.

Kun muistutus lähetetään, tapahtumat kirjataan **Viivästyskuluehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Viivästyskuluehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumat**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi viivästyskululaskun lähettämisen seurauksena voi olla ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskululaskut** ja valitse sitten vastaava linkki.
2. Valitse ensin soveltuva lasku ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä viivästyskululaskut** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Viivästyskululasku on joko tulostettu tai lähetetty määritettyyn sähköpostiin PDF-liitteenä.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Lähetetyn viivästyskululaskun peruuttaminen
Jos viivästyskululaskut lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.
1. Valitse **Lähetetyt viivästyskululaskut** -sivulla vähintään yhden peruutettavan viivästyskululaskun rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt viivästyskululaskut** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Muistutus-/Viivästyskulutapahtumien katsominen  
Kun lähetät muistutuksen, muistutustapahtuma luodaan **Muistutus-/viivästyskulutap.**-sivulle kullekin asiakastapahtuman sisältävälle muistutusriville. Voit sitten hakea tietyn asiakkaan muistutustapahtumien yleiskuvauksen.    
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Tapahtumakirjaukset**-toiminto.
3. Valitse **Asiakastapahtumat**-sivulla tapahtumarivi, jonka muistutukset haluat nähdä, ja valitse sitten **Muistutus-/viivästyskulutapah.**-toiminto.

## <a name="multiple-interest-rates"></a>Useita korkoprosentteja

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]Lisätietoja on kohdassa [Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md)  
[Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]