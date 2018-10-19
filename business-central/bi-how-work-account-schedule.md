---
title: "Luo taloudellisia raportteja KP-raporttimalleja käyttäen"
description: "Kuvailee, miten KP-raporttimalleja voidaan käyttää erilaisten näkymien ja raporttien luomiseen taloushallinnon suorituskykytietojen analysointia varten."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla
Saat KP-raporttimallien avulla tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. KP-raporttimallit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia pääkirjanpidon budjettitapahtumiin. Tulokset näkyvät roolikeskuksen kaavioissa, kuten kassavirtakaaviossa, ja raporteissa, kuten Tuloslaskelma- ja Tase-raporteissa.

Voit käyttää näitä kahta raporttia esimerkiksi liiketoimintajohtajan ja kirjanpitäjän roolikeskusten **Tilinpäätökset** -toiminnon avulla.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää käyttövalmiita KP-raporttimalleja. Voit myös määrittää itse verrattavat luvut määrittämällä omat rivit ja sarakkeet. Voit esimerkiksi luoda KP-raporttimalleja katteen laskemista varten erilaisille dimensioille, kuten osastoille tai asiakasryhmille. Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.  

KP-raporttimallien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä. Voit esimerkiksi tarkastella pääkirjanpidon tapahtumia budjettitapahtumien prosenttiosuuksina. Tämä edellyttää, että budjetit on luotu. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Tililuokat ja KP-raporttimallit
Tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Kun olet määrittänyt tililuokat **KP-tilin luokat** -ikkunassa ja valinnut **Luo KP-raporttimallit** -toiminnon, tärkeimpien rahoituslaskelmien perustana olevat KP-raporttimallit päivitetään. Kun seuraavan kerran suoritat toisen näistä raporteista, esimerkiksi Tase-raportin, uudet kokonaissummat ja korvaustapahtumat lisätään muutosten perusteella. Lisätietoja on kohdan [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md) Tililuokat-osassa.  

## <a name="to-create-new-account-schedules"></a>Uuden KP-raporttimallin luominen  
 KP-raporttimallien käyttäminen kirjanpitotilien lukujen analysoimista varten tai pääkirjanpidon tapahtumien vertaamiseksi pääkirjanpidon budjettitapahtumiin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.  
2. Valitse **KP-raporttimallien nimet** -ikkunassa **Uusi**-toiminto ja luo uusi KP-raporttimallin nimi.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Muokkaa KP-raporttimallia** -toiminto.
5. Täytä **KP-raporttimalli** -ikkunan kentät tarpeesi mukaan.  

    Kun olet luonut uuden KP-raporttimallin ja määrittänyt rivit sinun täytyy määrittää sarakkeet. Voit joko määrittää ne manuaalisesti tai liittää ennalta määrätyn sarakeasettelun KP-raporttimalliisi.
6. Valitse **Muokkaa sarakeasetuksia** -toiminto.
7. Täytä **Sarakeasettelu**-ikkunan kentät tarpeesi mukaan.

> [!NOTE]  
> Jos KP-raporttimallin sarakeasettelun oletusarvoa ei määritetty, sarakkeet on määritettävä manuaalisesti.

### <a name="to-copy-an-existing-account-schedule"></a>Olemassa olevan KP-raporttimallin kopioiminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen vakioversion KP-raporttimallit perustuvat vakiotalousraportteihin, jotka eivät ehkä vastaa liiketoimintasi tarpeita. Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan KP-raporttimallin.
1. Valitse **KP-raporttimallit**-ikkunassa KP-raporttimalli ja valitse sitten **Kopioi KP-raporttimalli** -toiminto.
2. Täytä **Kopioi KP-raporttimalli** -ikkunassa tarvittavat kentät ja valitse sitten **OK**-painike.

### <a name="to-create-a-column-that-calculates-percentages"></a>Prosenttilukuja laskevan sarakkeen luominen  
Joskus haluat ehkä sisällyttää KP-raporttimalliin sarakkeen, joka laskee prosenttiluvut kokonaissummasta. Jos esimerkiksi eri rivit jakavat myynnin dimensioittain, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto, jos haluat määrittää KP-raporttimallin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.  
4. Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.  
5. Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
6. Valitse **Muokkaa sarakeasetuksia** -toiminto, kun haluat määrittää sarakkeen.  
7. Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perää %-merkki. Jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
8. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## <a name="to-set-up-account-schedules-with-overviews"></a>KP-raporttimallien määrittäminen käyttäen yleiskuvauksia  
KP-raporttimallin käyttäminen pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto  
4. Valitse **KP-raporttimalli** -ikkunan **Nimi**-kentässä haluamasi KP-raporttimallin nimi.
5. Valitse **Syötä tilit** -toiminto.  
6. Valitse tilit, joita haluat ilmoitukseesi ja valitse sitten **OK**-painike.

    Tilit on nyt lisätty KP-raporttimalliin. Halutessasi voit myös muuttaa sarakeasettelua.  
7. Valitse **Yleiskuvaus**-toiminto.  
8. Valitse **Dimensiosuodattimet**-pikavälilehti ja määritä Budjettisuodatus-kentässä haluamasi suodattimen nimi.  
9. Valitse **OK**-painike.  

Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja
KP-raporttimalli voi verrata eri kirjanpitojaksojen tuloksia, kuten tämän kuun tuloksia edellisen vuoden saman kuukauden tuloksiin. Voit tehdä tämän lisäämällä sarakkeen, jossa on **Vertailujakson laskukaava** -kenttä ja sitten määrittämällä kentän arvoksi jakson kaava.  

Kirjanpitojakson ei tarvitse vastata kalenteria, mutta jokaisessa tilikaudessa on oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee jakson kaavan avulla vertailujakson summan suhteessa raporttipyynnön päivämääräsuodattimen jaksoon. Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon. Jaksomääritysten lyhenteet ovat seuraavat:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lyhenne</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>J</p></td>
<td><p>Jakso</p></td>
</tr>
<tr class="even">
<td><p>VJ</p></td>
<td><p>Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.</p></td>
</tr>
<tr class="odd">
<td><p>NJ</p></td>
<td><p>Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso.</p></td>
</tr>
<tr class="even">
<td><p>TK</p></td>
<td><p>Tilikausi. Esimerkiksi TK[1..3] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä.</p></td>
</tr>
</tbody>
</table>

Esimerkkejä kaavoista:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kaava</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Tyhjä&gt;</p></td>
<td><p>Nykyinen jakso</p></td>
</tr>
<tr class="even">
<td><p>-1J</p></td>
<td><p>Edellinen jakso</p></td>
</tr>
<tr class="odd">
<td><p>-1TK[1..EJ]</p></td>
<td><p>Koko edellinen tilikausi</p></td>
</tr>
<tr class="even">
<td><p>-1TK</p></td>
<td><p>Nykyinen jakso edellisenä tilikautena</p></td>
</tr>
<tr class="odd">
<td><p>-1TK[1..3]</p></td>
<td><p>Edellisen tilikauden ensimmäinen vuosineljännes</p></td>
</tr>
<tr class="even">
<td><p>-1TK[1..NJ]</p></td>
<td><p>Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien</p></td>
</tr>
<tr class="odd">
<td><p>-1TK[NJ..EJ]</p></td>
<td><p>Edellisen tilikauden nykyisestä jaksosta alkaen, aina edellisen tilikauden viimeiseen jaksoon asti, se mukaan lukien</p></td>
</tr>
</tbody>
</table>

Jos haluat laskea tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään.

> [!NOTE]
> Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartan tiedoissa. Voit esimerkiksi luoda KP-raporttimallin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräjakson suodatus** -kentän arvoksi *-1FY*. Tämän jälkeen raportti suoritetaan helmikuun 28. päivä ja määrität päivämääräsuodatukseksi tammikuun ja helmikuun. Tämän tuloksena KP-raporttimalli vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.  


## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

