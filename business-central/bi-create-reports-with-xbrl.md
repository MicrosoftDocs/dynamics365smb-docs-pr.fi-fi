---
title: Raporttien luominen XBRL-kielellä | Microsoft Docs
description: XBRL, joka tarkoittaa eXtensible Business Reporting Language, on XML-pohjainen kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jotta nämä voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9c806874d1bfea91224f0c458efea8a1da2d87f8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776839"
---
# <a name="create-reports-with-xbrl"></a>Luo raportteja XBRL-linkityksellä.
XBRL, joka tarkoittaa eXtensible Business Reporting Language, on XML-pohjainen kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jotta nämä voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan. XBRL-aloite sallii lukuisten ERP-ohjelmistoyritysten ja kansainvälisten kirjanpitojärjestöjen tekemän maailmanlaajuisen taloudellisen raportoinnin. Aloitteen tavoitteena on tarjota standardi pankkien, sijoittajien ja julkishallinnon taloudellisen tiedon raportointiin. Liiketoiminnan raportointi voi olla:  

 • tilinpäätöksiä  
 • rahoituksellisia tietoja  
 • muita kuin rahoituksellisia tietoja  
 • säädösten alaisia kirjauksia, kuten vuosittaiset ja neljännesvuosittaiset tilinpäätökset.  

> [!NOTE]
> Voit tuoda KP-malleja ja luoda XBRL-instanssiasiakirjoja yhdistämällä tilikartan KP-tietoja rahoitusraportteja varten suunniteltujen taksonomioiden elementteihin, kuten tase- ja tulosraportteihin.
> 
> XBRL-ominaisuudet Business Centralissa tukevat Specification 2.1 -taksonomioita , mutta taksonomiat voivat sisältää ei-tuettuja elementtejä, kuten kaavojen linkkijoukkoja, iXBRL, tai muita rakenteellisia eroja. On suositeltavaa vahvistaa XBRL-ominaisuudet ennen sen käyttöä raportoinnissa.
> 
> Taksonomioiden täysi tuki voi vaatia kolmannen osapuolen XBRL-koodausta ja -työkaluja. XBRL International -organisaatiolla on luettelo työkaluista ja palveluista, joita voit käyttää XBRL-raportoinnissa. Tietyn taksonomian XBRL-raportointivaatimusten mukaan haluat ehkä tutkia näitä resursseja. Lisätietoja on kohdassa [Aloita käyttö yrityksessä](https://go.microsoft.com/fwlink/?linkid=2153466) ja [Työkalut ja palvelut](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>XBRL (eXtensible Business Reporting Language)
XBRL (e **X** tensible **B** usiness **R** eporting **L** anguage) on XML-pohjainen kieli talousraportointiin. XBRL mahdollistaa standardin vakiomuotoisen raportoinnin koko finanssitietojen käyttäjäketjulle; noteeratut ja yksityiset yritykset, tilintarkastajat, viranomaiset, analyytikot, sijoitusyhteisöt, pääomamarkkinat ja luotottajat sekä kolmannet osapuolet kuten ohjelmistotalot ja tiedon jalostajat.  

Taksonomioita ylläpitää www.xbrl.org. Voit ladata taksonomioita tai lukea lisää ko. sivustolta.  

Joku joka haluaa taloushallinnon tietoja sinulta, antaa sinulle taksonomian (XML-asiakirjan), joka sisältää vähintään yhden mallin ja tällaisessa mallissa on vähintään yksi täytettävä rivi. Rivit vastaavat lähettäjän pyytämiä yksittäisiä taloushallinnon tietoja. Taksonomia tuodaan ja malli(t) täytetään antamalla tili(t), jotka vastaavat kutakin riviä sekä aikaväli, kuten nettomuutos tai päivän saldo. Jossain tapauksissa syötetään vakio, esim. työntekijöiden lkm. Nyt instanssiasiakirja (XML asiakirja) on valmis lähetettäväksi pyytäjälle. Idea on, että tämä on toistuva tapahtuma, joten mikäli taksonomiaan ei tehdä muutoksia, voidaan uusi instanssiasiakirja tuottaa uusilta jaksoilta tarvittaessa.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL koostuu seuraavista komponenteista  
XBRL **Määrittely** kertoo mitä XBRL on, ja kuinka rakentaa XBRL instanssiasiakirjoja ja XBRL -taksonomioita. XBRL -Määrittelyt kuvaavat XBRL:ää teknisesti ja ovat tarkoitetut teknisille ihmisille.  

XBRL **Mallit** ovat XBRL alatason komponentteja. Malli on fyysinen XSD-tiedosto, joka ilmaisee, kuinka instanssiasiakirjat ja taksonomiat tulee rakentaa.  

XBRL **Linkkikannat** ovat fyysisiä XML-tiedostoja, jotka sisältävät erilaisia tietoja XBRL-mallin kuvaamista elementeistä, kuten etiketit yhdellä tai useammalla kielellä, kuinka ne suhtautuvat toisiinsa, kuinka elementtejä summataan, jne.  

XBRL **Taksonomia** on ryhmän luoma “sanakirja”, joka on yhteensopiva XBRL-kuvauksen kanssa ja jota käytetään finanssitietojen jakamiseen.  

XBRL **Instanssiasiakirja** on yritysraportti esim. Tilinpäätös, joka on tehty XBRL-määrittelyn mukaan. Arvojen merkitys instanssiasiakirjassa on selitetty taksonomiassa. Instanssiasiakirja on melko hyödytön mikäli sen luomiseen käytettyä taksonomiaa ei ole käytettävissä.  

## <a name="layered-taxonomies"></a>Kerrostetut taksonomiat  
Taksonomia voi koostua perustaksonomiasta, esim. US-gaap tai IAS, sekä yhdestä tai useammasta laajennuksesta. Tämän ilmaisemiseksi taksonomia viittaa yhteen tai useampaan malliin, joista kukin on erillinen taksonomia. Kun lisätaksonomiat on ladattu tietokantaan, uudet elementit yksinkertaisesti lisätään olemassa olevien perään.  

## <a name="linkbases"></a>Linkkikannat  
 XBRL Spec. 2:ssa taksonomia kuvataan useassa XML-tiedostossa. Ensisijainen XML-tiedosto on itse taksonomian mallitiedosto (.xsd-tiedosto), joka sisältää vain järjestelemättömän luettelon raportoitavista elementeistä tai tiedoista. Tämän lisäksi yleensä käytetään joitakin linkkikantatiedostoja (.xml). Linkkikantatiedostot sisältävät dataa, joka täydentää raakaa taksonomiaa (.xsd -tiedosto). Linkkikantatiedostoja on kuutta tyyppiä, joista neljällä on merkitystä Tuotenimi XBRL:lle. Nämä ovat:  

-   Tunnus linkkikanta: Tämä linkkikanta sisältää tunnukset tai nimet tai etiketit elementeille. Tiedosto voi sisältää etikettejä useilla kielillä, jotka on määritetty XML-ominaisuudessa ’lang’. XML-kielitunniste sisältää yleensä kaksikirjaimisen lyhenteen, ja vaikka lyhenteen arvaaminen on melko helppoa sillä ei ole mitään yhteyttä Windows –kieleen tai kielikoodeihin, joita on käytetty demodatassa. Eli kun käyttäjä tarkastelee tietyn taksonomian kieliä, hän näkee kaikki tunnukset taksonomia ensimmäiselle elementille eli hän näkee esimerkin kaikista kielistä. Taksonomialla voi olla useita liitettyjä linkkikantoja, kunhan nämä linkkikannat sisältävät eri kielet.  

-   Esityslinkkikanta: Tämä linkkikanta sisältää tietoa elementtien rakenteesta, tai tarkemmin sanottuna sen, miten taksonomian julkaisija ehdottaa, että sovellus esittää taksonomian käyttäjälle. Linkkikanta sisältää linkkejä, jotka yhdistävät kaksi elementtiä pää- ja alaelementiksi. Kun kaikkia näitä linkkejä käytetään, elementit voidaan esittää hierarkisesti. Huomaa, että esityslinkkikanta käsittelee juuri tätä: elementtien esittämistä käyttäjälle.  

-   Laskentalinkkikanta: Tämä linkkikanta sisältää tietoa siitä mitkä elementit summataan mihin. Rakenne on melko samanlainen kuin esityslinkkikannassa, poikkeuksena se, että jokaisella linkillä tai ’kaarella’, kuten niitä kutsutaan, on paino-ominaisuus. Paino voi olla 1 tai –1 ilmaisten sen, että pitääkö elementti lisätä vai vähentää pääelementistään. Huomaa, että summaukset eivät ole välttämättä mukana visuaalisessa esityksessä.  

-   Viittauslinkkikanta: Tämä linkkikanta on xml-tiedosto, joka sisältää lisäinformaatiota datasta, jonka taksonomian julkaisija vaatii.

## <a name="to-set-up-xbrl-lines"></a>XBRL-rivien määrittäminen  
Kun olet tuonut tai päivittänyt taksonomian, mallien riveille tulee antaa kaikki tiedot, jotka tarvitaan. Nämä tiedot sisältävät yrityksen perustiedot, varsinaisen tilinpäätöksen, erittelyt, lisäykset, yms. tiedot, jotka tarvitaan ko. raportin täyttämiseen.  

XBRL-rivit määritellään linkittämällä taksonomiatiedot pääkirjanpitosi tietoihin.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-luokittelut** ja valitse sitten liittyvä linkki.  
2.  Valitse **XBRL-taksonomiat**-sivulla luokitus luettelosta.  
3.  Valitse **Rivit**-toiminto.  
4.  Valitse rivi ja täytä kentät.   
5.  Saat tarkat tiedot täytettävistä tiedoista valitsemalla **Tiedot**-toiminnon.  
6.  Voit määrittää tilikartan KP-tilien linkittämisen XBRL-riveille valitsemalla **KP-linkitysrivit** -toiminnon.  
7.  Voit lisätä huomautuksia raporttiin valitsemalla **Muistiot**-toiminnon.  

   > [!TIP]
   > Jos haluat jättää rivejä pois viennistä, valitse lähdetyypiksi **EI KOHDISTETTAVISSA**.

   > [!NOTE]  
   > Voit viedä vain tietoja, jotka vastaavat **Lähdetyyppi** -kentän valintaa. Näitä tietoja ovat esimerkiksi kuvaukset ja muistiinpanot.  

   > [!NOTE]  
   > Taksonomiat voivat sisältää elementtejä, joita [!INCLUDE[prod_short](includes/prod_short.md)] ei tue. Jos elementti ei ole tuettu, **Lähdetyyppi**-kenttä näyttää **Ei kodistettavissa** ja **Kuvaus**-kentässä näkyy virhesanoma, kuten **Odottamaton tyyppi: "tiettyä tyyppiä ei tunnisteta"**. Jos elementti on vietävä, valitse vastaava lähdetyyppi. Yleensä tämä on vakio tai kuvaus. Näin voit syöttää ja viedä tietoja, mutta tällaisilla elementeillä voi olla kelpoisuussääntöjä, joita ei voi tarkistaa ennen viemistä.

 ## <a name="to-import-an-xbrl-taxonomy"></a>XBRL-taksonomian tuominen  
Ensimmäinen vaihe XBRL-toiminnon käytössä on se, että tuot taksonomian yrityksesi tietokantaan. Taksonomia koostuu yhdestä tai useammasta mallista ja joistakin linkkikannoista. Kun olet tuonut sekä malli(t) että linkkikannat ja kohdistanut linkkikannat malliin, voit määrittää rivit ja kohdistaa oikeat KP-tilit oikeisiin taksonomian riveihin.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-luokittelut** ja valitse sitten liittyvä linkki.  
2.  Luo **XBRL-taksonomiat**-sivulla uusi rivi ja kirjoita taksonomian nimi ja kuvaus.  
3.  Valitse ensin **Mallit** ja lisää sitten mallin kuvaus.  
4.  Tuo malli valitsemalla **XBRL-mallit**-sivulla ensin **Tuo**-toiminto ja sitten kansio ja XSD-tiedosto. Valitse **Avaa**-painike.  
5.  Tuo linkkikanta valitsemalla **XBRL-mallit**-sivulla ensin **Linkkikannat**-toiminto ja sitten kansio ja XML-tiedosto. Valitse **Avaa**-painike.  
6.  Nyt voit kohdistaa linkkikannan malliin tai odottaa. Toista kunnen olet tuonut kaikki linkkikannat.  
7. Kohdista linkkikanta malliin valitsemalla **Kohdista taksonomiaan** -toiminto.  

> [!IMPORTANT]  
>  Linkkikannan kohdistaminen voi viedä aikaa, joten sen asemesta, että kohdistaisit kaikki linkkikannat yksitellen niiden tuomisen jälkeen, voit odottaa, kunnes olet tuonut ne kaikki ja kohdistaa ne kaikki samalla kertaa. Voit tehdä tämän valitsemalla **Ei**, kun ohjelma kysyy, haluatko kohdistaa juuri tuomasi linkkikannan malliin. Sitten valitaan rivit, joilla on linkkikannat, jotka halutaan ottaa käyttöön.  

## <a name="to-update-an-xbrl-taxonomy"></a>XBRL-taksonomian päivittäminen  
Kun taksonomia muuttuu tulee nykyinen taksonomia päivittää sen mukaiseksi. Syy päivitykseen voi olla muutos mallissa, linkkikannassa tai uusi linkkikanta. Taksonomian päivittämisen jälkeen tulee vain linkittää rivit muuttuneiden ja uusien rivien kohdalla.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-luokittelut** ja valitse sitten liittyvä linkki.  
2.  Valitse **XBRL-taksonomiat**-sivulla **Mallit**-toiminto.  
3.  Voit päivittää mallin valitsemalla ensin päivitettävän mallin ja sitten **Tuo**-toiminnon.  
4.  Päivitä tai lisää uusi linkkikanta valitsemalla **Linkkikannat**-toiminnon.  
5.  Valitse asianmukainen linkkikanta tai luo uusi rivi painamalla Ctrl + N. Valitse linkkikannan tyyppi tai lisää kuvaus.  
6.  Tuo linkkikanta valitsemalla **Tuo**-toiminto.  
7.  Valitse **Kyllä**, niin voit kohdistaa linkkikannan malliin.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)    
[Business Intelligence](bi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]