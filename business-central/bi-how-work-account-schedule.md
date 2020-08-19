---
title: Luo taloudellisia raportteja KP-raporttimalleja käyttäen
description: Kuvailee, miten KP-raporttimalleja voidaan käyttää erilaisten näkymien ja raporttien luomiseen taloushallinnon suorituskykytietojen analysointia varten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 07/22/2020
ms.author: edupont
ms.openlocfilehash: 783e93fd4b9c33a249556b75bc880daff0afd24b
ms.sourcegitcommit: e22666f90262c7d2084ca6c74ca7d66652fc6df6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617336"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla

Saat KP-raporttimallien avulla tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. KP-raporttimallit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia pääkirjanpidon budjettitapahtumiin. Tulokset näkyvät roolikeskuksen kaavioissa, kuten kassavirtakaaviossa, ja raporteissa, kuten Tuloslaskelma- ja Tase-raporteissa.

Voit käyttää näitä kahta raporttia esimerkiksi liiketoimintajohtajan ja kirjanpitäjän roolikeskusten **Tilinpäätökset** -toiminnon avulla.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää käyttövalmiita KP-raporttimalleja. Voit myös määrittää itse verrattavat luvut määrittämällä omat rivit ja sarakkeet. Voit esimerkiksi luoda KP-raporttimalleja katteen laskemista varten erilaisille dimensioille, kuten osastoille tai asiakasryhmille. Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.  

KP-raporttimallien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä. Voit esimerkiksi tarkastella pääkirjanpidon tapahtumia budjettitapahtumien prosenttiosuuksina. Tämä edellyttää, että budjetit on luotu. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## <a name="account-schedules"></a>KP-raporttimallit

KP-raporttimalleja käytetään tilikartan tilien järjestämiseksi tavalla, joka sopii kyseisten tilien tietojen esittämiseen. Voit määrittää eri asetteluja määrittääksesi tiedot, jotka haluat suodattaa tilikartasta. Yksi KP-raporttimallien päätehtävistä on toimia paikkana laskelmille, joita ei voi tehdä suoraan tilikartassa. Tällainen laskelma voi olla esimerkiksi tiliryhmien välisummien luominen. Välisummat voi sisällyttää uusiin summiin ja niitä voi käyttää sitten muissa summissa. Käyttäjät voivat esimerkiksi luoda KP-raporttimalleja katteen laskemista varten sellaisille dimensioille kuin osastoille tai asiakasryhmille. Lisäksi pääkirjanpidon tapahtumia ja pääkirjanpidon budjettitapahtumia voi suodattaa esimerkiksi nettomuutoksen tai veloitussumman perusteella.

Voit myös vertailla KP-raporttimalleja ja sarakeasetteluja kaavojen avulla. Tällaisen vertailun avulla voit

* luoda mukautettuja raportteja
* luoda tarvittavan määrän KP-raporttimalleja, joista kullakin on yksilöllinen nimi
* määrittää useita raportin asetteluita sekä tulostaa raportit käyttäen nykyisiä lukuja.

## <a name="gl-account-categories"></a>KP-tilin luokat

KP-tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Kun olet määrittänyt tililuokat **KP-tilin luokat** -sivulla ja valinnut **Luo KP-raporttimallit** -toiminnon, tärkeimpien rahoituslaskelmien perustana olevat KP-raporttimallit päivitetään. Kun seuraavan kerran suoritat toisen näistä raporteista, esimerkiksi **Tase-raportin**, uudet kokonaissummat ja korvaustapahtumat lisätään muutosten perusteella.

> [!NOTE]
> Ylimmän tason tililuokat, kuten **Velat**-solmu, ovat kiinteitä, eikä niitä voi lisätä. Voit kuitenkin poistaa ja lisätä tililuokkia alemmilla tasoilla ja muuttaa niiden rakennetta määrittääksesi, miten liittyvä KP-raporttimalli näkyy raporteissa.
>
> On suositeltavaa luoda ja jäsentää omat alemman tason KP-tililuokat alusta alkaen hierarkkisesti sen sijaan, että yrittäisit järjestää aiemmin luotuja. Voit esimerkiksi jäsentää **Velat**-solmun uudelleen niin, että siinä on uusi **Oma pääoma** -solmu, ja sen perässä ovat **Lyhytaikaiset velat**- ja **Pitkäaikaiset velat** -solmut.

## <a name="to-create-a-new-account-schedule"></a>Uuden KP-raporttimallin luominen

KP-raporttimallien käyttäminen kirjanpitotilien lukujen analysoimista varten tai pääkirjanpidon tapahtumien vertaamiseksi pääkirjanpidon budjettitapahtumiin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen vakioversion KP-raporttimallit perustuvat vakiotalousraportteihin, jotka eivät ehkä vastaa liiketoimintasi tarpeita. Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan KP-raporttimallin. Lisätietoja on alla vaiheessa 3.

**KP-raporttimallin yleiskuvaus** -sivulla voi esikatsella KP-raporttimallin määrittämän talousraportin. Seuraavassa kohdassa on olennaista tiedostaa, että KP-raporttimalleiksi määritetyt rivit ja sarakkeet ovat näkyvissä vain **KP-raporttimallin yleiskuvaus** -sivulla, jossa ne voidaan myös tarkistaa. Tämä sivu avataan KP-raporttimallista valitsemalla **Yleiskuvaus**-toiminto. **KP-raporttimalli**-sivu puolestaan on pelkkä määritysalue.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.  
2. Valitse **KP-raporttimallit**-sivulla **Uusi**-toiminto ja luo uusi KP-raporttimallin nimi.
3. Voit vaihtoehtoisesti valita **Kopioi KP-raporttimalli**-toiminnon, täyttää kaksi kenttä ja valitse lopuksi **OK**.
4. Täytä tarvittavat kentät. Valitse **Sarakeasettelun oletusarvo** -kentässä aiemmin luotu asettelu. Voit muokata sitä tarvittaessa myöhemmin.

    Sarakeasettelujen avulla voi määrittää sarakkeet eri parametrien avulla, taloustiedot näytetään riveillä näiden parametrien perusteella. Voit esimerkiksi suunnitella sarakeasettelun, jossa on neljä saraketta ja jonka avulla voit verrata nettomuutosta ja saldoa samalta kaudelta tältä ja edelliseltä vuodelta. Lisätietoja on kohdassa [Sarakeasettelun muokkaaminen](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Valitse **Muokkaa KP-raporttimallia** -toiminto.
6. Luo kullekin sellaiselle taloushallinnon elementille rivi, jonka haluat nähdä raportissa. Voit esimerkiksi luoda yhden rivin nykyisille vastaaville ja toisen rivin käyttöomaisuudelle. Esimerkkejä on CRONUS-esittely-yrityksen KP-raporttimalleissa.
7. Valitsemalla **Yleiskuvaus**-toiminnon saat näkyviin tuloksena olevan raportin.
8. Valitse **KP-raporttimallin yleiskuvaus** -sivun **Sarakeasettelun nimi** -kentässä toinen sarakeasettelu. Näet nyt toisten parametrien mukaisia taloudellisia tietoja.
9. Valitse **OK**-painike.

Olet määrittänyt KP-raporttimallin perusteen, näytettävät taloudelliset tiedot ja aiemmin luodun sarakeasettelun, jonka mukaan tiedot näytetään rivikohtaisesti eri parametrien perusteella. Jos vaiheessa 4 valittu oletussarakeasettelu ei ole tarkoituksenmukainen, noudata seuraavan menettelyn ohjeita.

### <a name="to-edit-a-column-layout"></a>Sarakeasettelun muokkaaminen

Määritä sarakeasettelun avulla, mitkä sarakkeet sisältyvät tuloksena olevaan raporttiin. Voit esimerkiksi suunnitella asettelun, jonka avulla voit verrata nettomuutosta ja saldoa samalta kaudelta tältä ja edelliseltä vuodelta.

> [!NOTE]
> KP-raporttimallin tulostetussa, esikatsellussa tai tallennetussa voi olla esillä enintään viisi saraketta. Jos KP-raporttimalli on tarkoitettu vain **KP-raporttimallin yleiskatsaus** -sivulla analysoitavaksi, voit luoda haluamasi määrän sarakkeita.

1. Valitse **KP-raporttimallit**-sivulla ensin sopiva KP-raporttimalli ja sitten **Muokkaa sarakeasetuksia** -toiminto.
2. Luo **Sarakeasettelut**-sivulla jokaiselle sarakkeelle rivi, jonka perusteella taloustiedot näytetään talousraportissa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **OK**-painike.
4. Avaa **KP-raporttimallin yleiskuvaus** -sivu ajoittain ja varmista, että uusi sarakeasettelu toimii odotetusti.

> [!NOTE]
> Kullekin riville määritetyt sarakkeet vastaavat **KP-raporttimallin yleiskatsaus** -sivulla sarakkeita 3 ja siitä eteenpäin. Kaksi ensimmäistä saraketta, **Rivikoodi** ja **Kuvaus**, ovat kiinteitä sarakkeita.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Prosenttilukuja laskevan sarakkeen luominen

Joskus haluat ehkä sisällyttää KP-raporttimalliin sarakkeen, joka laskee prosenttiluvut kokonaissummasta. Jos esimerkiksi eri rivit jakavat myynnin dimensioittain, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -sivulla KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto, jos haluat määrittää KP-raporttimallin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.  
4. Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.  
5. Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
6. Valitse **Muokkaa sarakeasetuksia** -toiminto, kun haluat määrittää sarakkeen.  
7. Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perää %-merkki. Jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
8. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## <a name="to-set-up-account-schedules-with-overviews"></a>KP-raporttimallien määrittäminen käyttäen yleiskuvauksia

KP-raporttimallin käyttäminen pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -sivulla KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto  
4. Valitse **KP-raporttimalli**-sivun **Nimi**-kentässä haluamasi KP-raporttimallin nimi.
5. Valitse **Syötä tilit** -toiminto.  
6. Valitse tilit, joita haluat ilmoitukseesi ja valitse sitten **OK**-painike.

    Tilit on nyt lisätty KP-raporttimalliin. Halutessasi voit myös muuttaa sarakeasettelua.  
7. Valitse **Yleiskuvaus**-toiminto.  
8. Määritä **KP-raporttimallin yleiskatsaus** -sivun **Dimensiosuodattimet**-pikavälilehdessä budjettisuodattimeksi haluamasi suodattimen nimi.  
9. Valitse **OK**-painike.  

Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja

KP-raporttimalli voi verrata eri kirjanpitojaksojen tuloksia, kuten tämän kuun tuloksia edellisen vuoden saman kuukauden tuloksiin. Voit tehdä sen avaamalla **sarakeasettelu**-sivun ja mukauttamalla sen lisäämällä **Vertailujakson kaava** -kentän sarakkeeksi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md). Tämän jälkeen kenttä voidaan määrittää jakson kaavaksi.  

Kirjanpitojakson ei tarvitse vastata kalenteria, mutta jokaisessa tilikaudessa on oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee jakson kaavan avulla vertailujakson summan suhteessa raporttipyynnön päivämääräsuodattimen jaksoon. Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon. Jaksomääritysten lyhenteet ovat seuraavat:

| Lyhenne | Kuvaus                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| J            | Jakso                                                                                |
| VJ           | Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.                                   |
| NJ           | Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso. Käytä NJ:tä kaavoissa määrittääksesi kauden, joka aloittaa tai lopettaa kaavan. Esimerkiksi FY\[1..NJ\] tarkoittaa kuluvaa aikaa kuluvan tilikauden alusta lähtien.|
| TK           | Tilikausi. Esimerkiksi TK\[1..3\] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä |

Esimerkkejä kaavoista:

| Kaava         | Kuvaus                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Nykyinen jakso                                                                                  |
| \-1J            | Edellinen jakso                                                                                 |
| \-1TK\[1..EJ\]  | Koko edellinen tilikausi                                                                     |
| \-1TK           | Nykyinen jakso edellisenä tilikautena                                                          |
| \-1TK\[1..3\]   | Edellisen tilikauden ensimmäinen vuosineljännes                                                           |
| \-1TK\[1..NJ\]  | Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien molemmat kaudet |
| \-1TK\[NJ..EJ\] | Edellisen tilikauden nykyisestä jaksosta edellisen tilikauden viimeiseen jaksoon, molemmat kaudet mukaan lukien   |

Jos haluat laskea tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään. Jos esimerkiksi kentän arvoksi määritetään -1Y, [!INCLUDE [prodshort](includes/prodshort.md)] vertaa tätä vuoden takaiseen samaan kauteen.

> [!NOTE]
> Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartan tiedoissa. Voit esimerkiksi luoda KP-raporttimallin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräkaava** -kentän arvoksi *-1FY*. Tämän jälkeen raportti suoritetaan helmikuun 28. päivä ja määrität päivämääräsuodatukseksi tammikuun ja helmikuun. Tämän tuloksena KP-raporttimalli vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.  

Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
