---
title: Asiakkaiden muistuttaminen tai sakottaminen erääntyneistä maksuista| Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten asiakkaalle lähetetään muistutus erääntyvästä maksusta ja miten maksuun lisätään myöhästymismaksu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ec17c59ebbc336cf6c4757be447ff7765098c816
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190681"
---
# <a name="collect-outstanding-balances"></a>Avointen saldojen perintä
Myyntisaamisten hallintaan kuuluu sen tarkistaminen, onko erääntyneet summat maksettu ajoissa. Jos asiakkailla on erääntyneitä maksuja, voit aloittaa lähettämällä heille asiakkaan tiliotteen raportin muistutuksena. Vaihtoehtoisesti voit lähettää muistutuksia.

Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista. Niiden avulla voit myös laskea viivästyskuluja, kuten korkoja tai lisämaksuja, ja sisällyttää ne muistutukseen. Käytä viivästyskululaskuja, jos haluat veloittaa asiakkailta korkoja tai maksuja muistuttamatta erääntyneistä summista.

## <a name="reminders"></a>Muistutukset
Ennen kuin voit luoda muistutuksia, sinun on määritettävä muistutusehdot ja määritettävä ne asiakkaille. Kullakin muistutusehdolla on ennalta määritetyt muistutustasot. Kukin muistutustaso sisältää muistutuksen lähettämisajankohtaa koskevat säännöt, esimerkiksi kuinka monta päivää laskun eräpäivän tai edellisen muistutuksen päivämäärän jälkeen muistutus lähetetään. **Viivästyskuluehdot**-sivu määrittää, lasketaanko muistutukseen korot.  

Voit ajaa **Luo muistutukset** -eräajon säännöllisin väliajoin ja luoda näin muistutukset kaikille asiakkaille, joilla on erääntyneitä saldoja, tai voit luoda muistutuksen tietylle asiakkaalle manuaalisesti ja antaa ohjelman laskea ja täyttää sen rivit automaattisesti.  

Muistutusten luomisen jälkeen voit muokata niitä. Kunkin muistutuksen alussa ja lopussa näkyvä teksti määräytyy muistutustason ehtojen mukaan, ja sen voi nähdä **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä muistutuksen teksti** -toiminnon käyttämistä.  

Asiakastapahtuma, jolla on **Estossa**-kenttä valittuna, ei aiheuta muistutuksen luomista. Jos muistutus kuitenkin luodaan toisen tapahtuman perusteella, pidossa olevaksi merkitty erääntynyt tapahtuma sisällytetään muistutukseen. Näiden tapahtumien riveille ei lasketa korkoa.

Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset – yleensä sähköpostina.

## <a name="finance-charges"></a>Viivästyskulut
Jos asiakas ei suorita maksua eräpäivään mennessä, voit antaa ohjelman laskea viivästyskulut automaattisesti ja lisätä ne asiakkaan tilin erääntyneisiin summiin. Voi antaa asiakkaille tiedon lisätyistä kuluista lähettämällä viivästyskululaskuja.  

> [!NOTE]  
> Käyttämällä viivästyskululaskuja voit laskea korot ja viivästyskulut sekä antaa niistä tiedon asiakkaille muistuttamatta erääntyneistä maksuista. Vaihtoehtoisesti voit laskea erääntyneiden maksujen koron muistutusten luomisen yhteydessä.  

Voit luoda yksittäiselle asiakkaalle viivästyskululaskun manuaalisesti ja täyttää rivit automaattisesti. Vaihtoehtoisesti voit luoda **Luo viivästyskululasku** -toiminnon avulla viivästyskululaskut kaikille asiakkaille tai valituille asiakkaille, joilla on erääntyneitä saldoja.  

Viivästyskululaskujen luomisen jälkeen voit muokata niitä. Kunkin viivästyskululaskun alussa ja lopussa näkyvä teksti määräytyy viivästyskuluehtojen mukaan, ja tekstin voi nähdä rivien **Kuvaus**-sarakkeessa. Jos laskettu summa on lisätty automaattisesti tekstin alkuun tai loppuun, tekstiä ei muuteta, jos poistat rivit. Tällöin tekstin muuttaminen edellyttää **Päivitä lisäkulun teksti** -toiminnon käyttämistä.  

Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut – yleensä sähköpostina.

## <a name="multiple-interest-rates"></a>Useita korkoprosentteja
Kun määrität viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan. Jos useita korkoprosentteja ei ole määritetty, korkoprosentti ja kausi määritetään **Viivästyskuluehdot**- ja **Muistutusehdot**-sivuilla laskennan koko kaudelle. Lisätietoja on kohdassa [Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Asiakkaan tilioteraportin lähettäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaan tiliote** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Tulostusvaihtoehdot**-kohdassa, miten raportti lähetetään asiakkaalle.

> [!NOTE]  
>   Jos käytössä on useita valuuttoja, asiakkaan tiliotteen raportti tulostetaan aina asiakkaan valuuttana. Tiliotteen päivämääränä ja erääntymispäivämääränä, jos erääntyminen otetaan huomioon, käytetään tiliotteen kauden viimeistä päivämäärää.

## <a name="to-set-up-reminder-terms"></a>Muistutusehtojen määrittäminen
Jos asiakkailla on erääntyneitä maksuja, sinun täytyy päättää, milloin ja miten heille lähetetään muistutus. Lisäksi saattaa olla tarpeen veloittaa heidän tileiltään korkoja tai maksuja. Muistutusehtoja voi määrittää kuinka monta tahansa. Voit määrittää kullekin muistutusehtojen koodille rajoittamattoman määrän muistutustasoja.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.  
3. Voit käyttää useita muistutusehtoyhdistelmä, kun määrität kullekin koodin.

## <a name="to-set-up-reminder-levels"></a>Muistutustasojen määrittäminen
Kun asiakkaalle luodaan ensimmäinen muistutus, ohjelma käyttää tason 1 asetuksia. Kun muistutus lähetetään, tason numero rekisteröidään muistutustapahtumiin, jotka luodaan ja linkitetään yksittäisiin asiakastapahtumiin. Jos asiakkaalle on tarpeen lähettää uusi muistutus, kaikki avoimiin asiakastapahtumiin linkitetyt muistutustapahtumat tarkistetaan suurimman tason numeron selvittämistä varten. Tämän jälkeen käytetään uutta muistutusta varten seuraavan tason numeron ehtoja.

Jos luot enemmän muistutuksia kuin mille olet määrittänyt tasoja, ohjelma käyttää ylimmän tason ehtoja. Luotavien muistutusten enimmäismäärä määräytyy muistutusehtojen **Muistutusten enimmäislukumäärä** -kentän mukaan.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
2. Valitse **Muistutusehdot**-sivulla rivi, jonka ehdoille haluat määrittää tasoja, ja valitse sitten **Tasot**-toiminto.  
3. Täytä tarvittavat kentät.  

    Kutakin muistutustasoa varten voit määrittää yksittäisiä ehtoja, joihin voi sisältyä lisämaksuja sekä paikallisena valuuttana että ulkomaan valuuttana. Kullekin **Muistutustasot**-sivun koodille voi määrittää useita ulkomaan valuutoissa olevia lisämaksuja.
4. Valitse **Valuutat**-toiminto.
5. Määritä **Muistutustason valuutat** -sivulla jokaiselle muistutustason koodille ja vastaavalle muistutustason numerolle valuutan koodi ja lisämaksu.

    > [!NOTE]  
    > Kun luot muistutuksia ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään muistutusten luontiin. Jos ulkomaan valuuttojen ehtoja ei ole määritetty, käytetään **Muistutustasot**-sivulla määritettyjä PVA:n muistutusehtoja ja ne muunnetaan soveltuvaan valuuttaan.

    Voit määrittää kutakin muistutustasoa varten tekstin, joka tulostetaan ennen muistutuksen merkintöjä (**Aloitusteksti**) tai niiden jälkeen (**Lopetusteksti**).

6. Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Muistutusteksti**-sivun tiedot.
7. Voit lisätä liittyviä arvoja automaattisesti muistutustekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.  

|Paikkamerkki|Arvo|  
|-----------------|-----------|  
|%1|Muistutuksen otsikon **Asiakirjan pvm** -kentän sisältö|  
|%2|Muistutuksen otsikon **Eräpäivä** -kentän sisältö|  
|%3|Viivästyskuluehtojen **Korko**-kentän sisältö|  
|%4|Muistutuksen otsikon **Jäljellä oleva summa** -kentän sisältö|  
|%5|Muistutuksen otsikon **Korkosumma**-kentän sisältö|  
|%6|Muistutuksen otsikon **Lisämaksu**-kentän sisältö|  
|%7|Muistutuksen kokonaissumma|  
|%8|Muistutuksen otsikon **Muistutustaso**-kentän sisältö|  
|%9|Muistutuksen otsikon **Valuutan koodi** -kentän sisältö|  
|%10|Muistutuksen otsikon **Kirjauspvm** -kentän sisältö|  
|%11|Yrityksen nimi|  
|%12|Muistutuksen otsikon **Lisämaksu riviä kohti** -kentän sisältö|  

Jos kirjoitat kenttään esimerkiksi **Velkasi on %9 %7, joka erääntyy %2**, muistutustekstiksi tulee **Velkasi on 1200,50 PVA, joka erääntyy 2.2.2014.**.

> [!NOTE]
> Eräpäivä lasketaan annetun päivämääräkaavan mukaan. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).

Kun olet määrittänyt muistutusehdot sekä lisätasot ja tekstin, määritä jokin koodeista kussakin asiakkaan kortissa. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Muistutusten luominen automaattisesti
Muistutus on vastaava kuin lasku. Kun luot muistutuksen, muistutuksen otsikko ja vähintään yksi muistutusrivi on oltava lisättynä. Voit luoda toiminnolla muistutuksia kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten liittyvä linkki.
2. Valitse **Muistutus**-sivulla **Luo muistutuksia** -toiminto.
3. Täytä **Luo muistutukset** -sivulla kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
4. Valitse **OK**-painike.

## <a name="to-create-a-reminder-manually"></a>Muistutusten luominen manuaalisesti
Voit täyttää **Muistutus**-sivulla **Yleiset**-pikavälilehden tiedot manuaalisesti, jonka jälkeen rivit täytetään automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Valitse **Ehdota muistutusrivejä** -toiminto.
5. Täytä **Ehdota muistutusrivejä** -eräajossa kentät, joilla määrität, miten muistutukset luodaan ja kenelle ne luodaan.
6. Valitse **Sisällytä pidossa olevat tapahtumat** -valintaruutu, jos haluat muistutusten sisältävän erääntyneet, pidossa olevat avoimet tapahtumat.

    > [!Important]
    > Pidossa olevat avoimet tapahtumat lisätään riippumatta Vain tapahtumat, joissa on erääntyneitä summia -asetuksen tilasta.

7. Valitse **OK**-painike.

## <a name="to-replace-reminder-texts"></a>Muistutustekstien vaihtaminen  
On monta tapaa määrittää teksti, joka näkyy tulostetussa muistutuksessa. Joskus voit haluta korvata nykyiselle luokalle määritetyt alku- ja lopputekstit eri luokkien teksteillä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten liittyvä linkki.
2. Avaa sopiva muistutus ja valitse sitten **Päivitä muistutusteksti** -toiminto.
3. Anna **Päivitä muistutusteksti** -sivun **Muistutustaso**-kentässä tarvittava taso.
3. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.

## <a name="to-issue-a-reminder"></a>Muistutuksen lähettäminen
Kun olet luonut muistutukset ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää muistutukset.

Kun lähetät muistutuksen, tiedot siirretään erilliseen lähetettyjen muistutusten sivulle. Samalla muistutuksen tapahtumat kirjataan. Jos muistutukseen on laskettu korkoja tai lisämaksuja, tapahtumat kirjataan asiakastapahtumiin ja pääkirjanpitoon.

Kun muistutus lähetetään, tapahtumat kirjataan **Muistutusehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Muistutusehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumat**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi muistutuksen lähettämisestä voi seurata ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutukset** ja valitse sitten liittyvä linkki.
2. Valitse ensin soveltuva muistutus ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä muistutukset** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Muistutus on joko tulostettu lähettäväksi määritettyyn sähköpostiin PDF-liitteenä.

### <a name="to-cancel-an-issued-reminder"></a>Lähetetyn muistutuksen peruuttaminen
Jos muistutukset lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.
1. Valitse **Lähetetyt muistutukset** -sivulla vähintään yhden peruutettavan lähetetyn muistutuksen rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt muistutukset** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

## <a name="to-set-up-finance-charge-terms"></a>Viivästyskuluehtojen määrittäminen
Jokaista viivästyskulun laskentaa kuvaamaan täytyy määrittää koodi. Tämä koodi voidaan sitten antaa asiakas- tai toimittajakortin **Viivästyskuluehtojen koodi** -kentässä.

Viivästyskulut voidaan laskea käyttämällä joko keskimääräinen päiväsaldo -menetelmää tai erääntyvä saldo -menetelmää.

* Erääntyvä saldo -menetelmä

    Viivästyskulu on yksinkertaisesti prosenttiosuus erääntyneestä summasta.  
    *Erääntyvä saldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(korkoprosentti / 100)*

*   Keskimääräinen päiväsaldo -menetelmä

    Maksun erääntymispäivien määrä otetaan huomioon:  
    *Keskimääräinen päiväsaldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(päiviä erääntynyt / korkojakso)* x *(korkoprosentti/100)*

Lisäksi jokainen Viivästyskuluehdot-taulukon koodi on linkitetty alitaulukkoon, Viivästyskuluteksti-taulukkoon. Jokaiselle viivästyskuluehtojen sarjalle voidaan määrittää alku- ja/tai lopputekstiä, joka sisällytetään viivästyskululaskuun.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskuluehdot** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.
3. Voit käyttää useita viivästyskuluehtoyhdistelmä, kun määrität kullekin koodin.

    Voit määrittää kullekin viivästyskuluehdolle yksittäisiä ehtoja, joihin voi sisältyä lisämaksuja sekä paikallisena valuuttana että ulkomaan valuuttana. Kullekin **Viivästyskuluehdot**-sivun koodille voi määrittää useita lisämaksuja ulkomaan valuuttana.
4. Valitse **Valuutat**-toiminto.
5. Määritä **Lisäkuluehtojen valuutat** -sivulla kullekin ehdolle valuutan koodi ja lisämaksu.

    > [!NOTE]  
    > Kun luot viivästyskuluja ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään viivästyskululaskujen luomiseen. Jos ulkomaan valuuttojen viivästyskuluehtoja ei ole määritetty, käytetään **Viivästyskuluehdot**-sivulla määritettyjä PVA:n viivästyskuluehtoja ja ne muunnetaan liittyvään valuuttaan.

    Voit määrittää jokaiselle viivästyskuluehdolle tekstiä, joka tulostetaan ennen viivästyskululaskun tapahtumia (**Aloitusteksti**) tai tapahtumien jälkeen (**Lopputeksti**).  
6. Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Viivästyskuluteksti**-sivun tiedot.
7. Voit lisätä liittyviä arvoja automaattisesti viivästyskulutekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.

|Paikkamerkki|Arvo|  
|-----------------|-----------|  
|%1|Viivästyskululaskun otsikon **Asiakirjan pvm** -kentän sisältö|  
|%2|Viivästyskululaskun otsikon **Eräpäivä**-kentän sisältö|  
|%3|Viivästyskuluehtojen **Korko**-kentän sisältö|  
|%4|Viivästyskululaskun otsikon **Jäljellä oleva summa** -kentän sisältö|  
|%5|Viivästyskululaskun otsikon **Korkosumma**-kentän sisältö|  
|%6|Viivästyskululaskun otsikon **Lisämaksu**-kentän sisältö|  
|%7|Muistutuksen kokonaissumma|  
|%8|Viivästyskululaskun otsikon **Valuutan koodi** -kentän sisältö|  
|%9|Viivästyskululaskun otsikon **Kirjauspvm**-kentän sisältö|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Viivästyskululaskujen luominen manuaalisesti  
Viivästyskululasku on samanlainen kuin tavallinen lasku. Voit täyttää otsikon manuaalisesti ja antaa ohjelman täyttää rivit, tai voit antaa ohjelman luoda viivästyskululaskut kaikille asiakkaille automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskululaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.  
3. Valitse **Ehdota lisäkululaskurivejä** -toiminto.
4. Määritä suodatin **Ehdota lisäkululaskurivejä** -sivun **Asiakastapahtuma**-pikavälilehdessä, jos haluat luoda viivästyskululaskuja vain tietyille tapahtumille.

    > [!NOTE]
    > Vaikka ne on luetteloitu, **Maksun** ja **Hyvityslaskun** valitseminen **Asiakirjatyyppi**-suodattimiksi ei vaikuta siihen, koska **Ehdota viivästyskululaskun rivejä** -toiminto käsittelee vain positiivisia määriä.
5.  Aloita eräajo valitsemalla **OK**.  

## <a name="to-update-finance-charge-memo-texts"></a>Viivästyskululaskutekstien päivitys  
Joskus voit haluta muuttaa viivästyskuluehtoihin määrittämiäsi alku- ja lopputekstejä. Jos teet tämän silloin, kun olet luonut viivästyskululaskut – mutta et vielä lähettänyt niitä, voit antaa ohjelman päivittää muutetut tekstit laskuihin.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskululasku** ja valitse sitten liittyvä linkki.  
2. Avaa viivästyskululaskun, jonka tekstiä haluat muuttaa, ja valitse sitten **Päivitä lisäkulun teksti** -toiminto.
3. Voit määrittää **Päivitä lisäkulun teksti** -sivulla suodattimen, jos haluat päivittää useita laskuja.
4. Päivitä aloitus- ja lopputekstit valitsemalla **OK**.  

## <a name="to-issue-finance-charge-memos"></a>Viivästyskululaskujen lähettäminen
Kun olet luonut viivästyskululaskut ja tehnyt tarvittavat muutokset, voit joko tulostaa testiraportteja tai lähettää viivästyskululaskut.

Kun muistutus lähetetään, tapahtumat kirjataan **Viivästyskuluehdot**-sivun määritysten mukaan. Tämän määrityksen mukaisesti korko ja/tai lisämaksut joko kirjataan asiakkaan tilille ja pääkirjanpitoon tai ei. **Asiakkaan kirjausryhmät** -sivun asetukset määrittävät, mille tileille kirjataan.

Viivästyskululaskun jokaiselle asiakastapahtumalle luodaan tapahtuma **Muistutus-/viivästyskulutapah.**-sivulle.

Jos **Kirjaa korko**- tai **Kirjaa lisämaksu** -valintaruudut on valittu **Viivästyskuluehdot**-sivulla, myös seuraavat tapahtumat luodaan:

- Yksi tapahtuma **Asiakastapahtumat**-sivulla
- Yksi myyntisaamistapahtuma liittyvällä KP-tilillä
- Yksi korkotapahtuma ja/tai yksi lisämaksutapahtuma liittyvällä KP-tilillä

Lisäksi viivästyskululaskun lähettämisen seurauksena voi olla ALV-tapahtumia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskululaskut** ja valitse sitten liittyvä linkki.
2. Valitse ensin soveltuva lasku ja sitten **Lähetä**-toiminto.
3. Täytä **Lähetä viivästyskululaskut** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.

Viivästyskululasku on joko tulostettu tai lähetetty määritettyyn sähköpostiin PDF-liitteenä.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Lähetetyn viivästyskululaskun peruuttaminen
Jos viivästyskululaskut lähetettiin vahingossa, voit peruuttaa ne, ennen kuin ne lähetetään vastaanottajalle. Voit tehdä sen joko yksi kerrallaan tai eränä.
1. Valitse **Lähetetyt viivästyskululaskut** -sivulla vähintään yhden peruutettavan viivästyskululaskun rivi ja valitse sitten **Peruuta**-toiminto.
2. Täytä **Peruuta lähetetyt viivästyskululaskut** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Muistutus-/Viivästyskulutapahtumien katsominen  
Kun lähetät muistutuksen, muistutustapahtuma luodaan **Muistutus-/viivästyskulutap.**-sivulle kullekin asiakastapahtuman sisältävälle muistutusriville. Voit sitten hakea tietyn asiakkaan muistutustapahtumien yleiskuvauksen.    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.  
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Tapahtumakirjaukset**-toiminto.
3. Valitse **Asiakastapahtumat**-sivulla tapahtumarivi, jonka muistutukset haluat nähdä, ja valitse sitten **Muistutus-/viivästyskulutapah.**-toiminto.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
