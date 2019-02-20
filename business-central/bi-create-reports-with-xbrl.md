---
title: "Raporttien luominen XBRL-kielellä | Microsoft Docs"
description: "XBRL, joka tarkoittaa eXtensible Business Reporting Language, on XML-pohjainen kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jotta nämä voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 2b17ad5dabed505b358b8c2be6414b17228724b8
ms.contentlocale: fi-fi
ms.lasthandoff: 11/29/2018

---
# <a name="create-reports-with-xbrl"></a>Luo raportteja XBRL-linkityksellä.
XBRL, joka tarkoittaa eXtensible Business Reporting Language, on XML-pohjainen kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jotta nämä voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan. XBRL-aloite sallii lukuisten ERP-ohjelmistoyritysten ja kansainvälisten kirjanpitojärjestöjen tekemän maailmanlaajuisen taloudellisen raportoinnin. Aloitteen tavoitteena on tarjota standardi pankkien, sijoittajien ja julkishallinnon taloudellisen tiedon raportointiin. Liiketoiminnan raportointi voi olla:  

 • tilinpäätöksiä  
 • rahoituksellisia tietoja  
 • muita kuin rahoituksellisia tietoja  
 • säädösten alaisia kirjauksia, kuten vuosittaiset ja neljännesvuosittaiset tilinpäätökset.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)]in avulla yritykset voivat tuottaa XBRL-muotoisia tietoja ja hyödyntää kielen mahdollistaman joustavuuden ja automatisoinnin sekä tietojen keräämisessä että jakamisessa.  

## <a name="extensible-business-reporting-language"></a>XBRL (eXtensible Business Reporting Language)
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) on XML-pohjainen kieli talousraportointiin. XBRL mahdollistaa standardin vakiomuotoisen raportoinnin koko finanssitietojen käyttäjäketjulle; noteeratut ja yksityiset yritykset, tilintarkastajat, viranomaiset, analyytikot, sijoitusyhteisöt, pääomamarkkinat ja luotottajat sekä kolmannet osapuolet kuten ohjelmistotalot ja tiedon jalostajat.  

Taksonomioita ylläpitää www.xbrl.org. Voit ladata taksonomioita tai lukea lisää ko. sivustolta.  

Joku joka haluaa taloushallinnon tietoja sinulta, antaa sinulle taksonomian (XML-asiakirjan), joka sisältää vähintään yhden mallin ja tällaisessa mallissa on vähintään yksi täytettävä rivi. Rivit vastaavat lähettäjän pyytämiä yksittäisiä taloushallinnon tietoja. Taksonomia tuodaan ohjelmaan ja malli(t) täytetään syöttämällä tili(t), jotka vastaavat jokaista riviä sekä aikaväli esim. nettomuutos tai päivän saldo. Jossain tapauksissa syötetään vakio, esim. työntekijöiden lkm. Jossain tapauksissa syötetään vakio, esim. työntekijöiden lkm. Nyt instanssiasiakirja (XML asiakirja) on valmis lähetettäväksi tiedon vastaanottajalle. Idea on, että tämä on toistuva tapahtuma, joten mikäli taksonomiaan ei tehdä muutoksia, voidaan uusi instanssiasiakirja tuottaa uusilta jaksoilta tarvittaessa.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL koostuu seuraavista komponenteista  
XBRL **Määrittely** kertoo mitä XBRL on, kuinka rakentaa XBRL instanssiasiakirjoja ja XBRL -taksonomioita. XBRL -Määrittelyt kuvaavat XBRL:ää teknisesti ja ovat tarkoitetut teknisille ihmisille.  

XBRL **Mallit** ovat XBRL alatason komponentteja. Malli on fyysinen XSD-tiedosto, joka ilmaisee, kuinka instanssiasiakirjat ja taksonomiat tulee rakentaa.  

XBRL **Linkkikannat** ovat fyysisiä XML-tiedostoja, jotka sisältävät erilaisia tietoja XBRL-mallin kuvaamista elementeistä, kuten etiketit yhdellä tai useammalla kielellä, kuinka ne suhtautuvat toisiinsa, kuinka elementtejä summataan, jne.  

XBRL **Taksonomia** on ryhmän luoma “sanakirja”, joka on yhteensopiva XBRL-kuvauksen kanssa ja jota käytetään finanssitietojen jakamiseen.  

XBRL **Instanssiasiakirja** on yritysraportti esim. Tilinpäätös, joka on tehty XBRL-määrittelyn mukaan. Arvojen merkitys instanssiasiakirjassa on selitetty taksonomiassa. Instanssiasiakirja on melko hyödytön mikäli sen luomiseen käytettyä taksonomiaa ei ole käytettävissä.  

## <a name="layered-taxonomies"></a>Kerrostetut taksonomiat  
Taksonomia voi koostua perustaksonomiasta, esim. US-gaap tai IAS, sekä yhdestä tai useammasta laajennuksesta. Tämän ilmaisemiseksi, taksonomia viittaa yhteen tai useampaan malliin, jotka kaikki ovat erillisiä taksonomioita. Kun lisätaksonomiat on ladattu tietokantaan, uudet elementit yksinkertaisesti lisätään olemassa olevien perään.  

## <a name="linkbases"></a>Linkkikannat  
 XBRL Spec. 2:ssa taksonomia kuvataan useassa XML-tiedostossa. Ensisijainen XML-tiedosto on itse taksonomian mallitiedosto (.xsd-tiedosto), joka sisältää vain järjestelemättömän luettelon raportoitavista elementeistä tai tiedoista. Tämän lisäksi yleensä käytetään joitakin linkkikantatiedostoja (.xml). Linkkikantatiedostot sisältävät dataa, joka täydentää raakaa taksonomiaa (.xsd -tiedosto). Linkkikantatiedostoja on kuutta tyyppiä, joista neljällä on merkitystä Tuotenimi XBRL:lle. Nämä ovat:  

-   Tunnus linkkikanta: Tämä linkkikanta sisältää tunnukset tai nimet tai etiketit elementeille. Tiedosto voi sisältää etikettejä useilla kielillä, jotka on määritetty XML-ominaisuudessa ’lang’. XML-kielitunniste sisältää yleensä kaksikirjaimisen lyhenteen, ja vaikka lyhenteen arvaaminen on melko helppoa sillä ei ole mitään yhteyttä Windows –kieleen tai kielikoodeihin, joita on käytetty demodatassa. Eli kun käyttäjä tarkastelee tietyn taksonomian kieliä, hän näkee kaikki tunnukset taksonomia ensimmäiselle elementille eli hän näkee esimerkin kaikista kielistä. Taksonomialla voi olla useita liitettyjä linkkikantoja, kunhan nämä linkkikannat sisältävät eri kielet.  

-   Esityslinkkikanta: Tämä linkkikanta sisältää tietoa elementtien rakenteesta, tai tarkemmin; kuinka taksonomian julkaisija ehdottaa, että ohjelma esittää taksonomian käyttäjälle. Linkkikanta sisältää linkkejä, jotka yhdistävät kaksi elementtiä pää- ja alaelementiksi. Kun kaikkia näitä linkkejä käytetään, elementit voidaan esittää hierarkisesti. Huomaa, että esityslinkkikanta käsittelee juuri tätä: elementtien esittämistä käyttäjälle.  

-   Laskentalinkkikanta: Tämä linkkikanta sisältää tietoa siitä mitkä elementit summataan mihin. Rakenne on melko samanlainen kuin esityslinkkikannassa, poikkeuksena se, että jokaisella linkillä tai ’kaarella’, kuten niitä kutsutaan, on paino-ominaisuus. Paino voi olla 1 tai –1 ilmaisten sen, että pitääkö elementti lisätä vai vähentää pääelementistään. Huomaa, että summaukset eivät ole välttämättä mukana visuaalisessa esityksessä.  

-   Viittauslinkkikanta: Tämä linkkikanta on xml-tiedosto, joka sisältää lisäinformaatiota datasta, jonka taksonomian julkaisija vaatii.

## <a name="to-set-up-xbrl-lines"></a>XBRL-rivien määrittäminen  
Kun olet tuonut tai päivittänyt taksonomian, mallien riveille tulee antaa kaikki tiedot, jotka tarvitaan. Nämä tiedot sisältävät yrityksen perustiedot, varsinaisen tilinpäätöksen, erittelyt, lisäykset, yms. tiedot, jotka tarvitaan ko. raportin täyttämiseen.  

XBRL-rivit määritellään linkittämällä taksonomiatiedot pääkirjanpitosi tietoihin.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-taksonomiat** ja valitse sitten liittyvä linkki.  
2.  Valitse **XBRL-taksonomiat**-sivulla luokitus luettelosta.  
3.  Valitse **Rivit**-toiminto.  
4.  Valitse rivi ja täytä kentät.   
5.  Saat tarkat tiedot täytettävistä tiedoista valitsemalla **Tiedot**-toiminnon.  
6.  Voit määrittää tilikartan KP-tilien linkittämisen XBRL-riveille valitsemalla **KP-linkitysrivit** -toiminnon.  
7.  Voit lisätä huomautuksia raporttiin valitsemalla **Muistiot**-toiminnon.  

> [!NOTE]  
>  Voit viedä vain dataa, joka vastaa lähdetyyppiä, jonka olet valinnut **Lähdetyyppi** -kentässä, sisältäen kuvauksen ja muistiot.  

> [!NOTE]  
>  Rivejä, jotka eivät ole relevantteja voidaan merkitä tyypillä EI **KOHDISTETTAVISSA**, jolloin niitä ei viedä.

 ## <a name="to-import-an-xbrl-taxonomy"></a>XBRL-taksonomian tuominen  
Ensimmäinen vaihe XBRL-toiminnon käytössä on se, että tuot taksonomian yrityksesi tietokantaan. Taksonomia koostuu yhdestä tai useammasta mallista ja joistakin linkkikannoista. Kun olet tuonut sekä malli(t) että linkkikannat ja kohdistanut linkkikannat malliin, voit määrittää rivit ja kohdistaa oikeat KP-tilit oikeisiin taksonomian riveihin.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **XBRL-taksonomiat** ja valitse sitten liittyvä linkki.  
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

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **XBRL-taksonomiat** ja valitse sitten liittyvä linkki.  
2.  Valitse **XBRL-taksonomiat**-sivulla **Mallit**-toiminto.  
3.  Voit päivittää mallin valitsemalla ensin päivitettävän mallin ja sitten **Tuo**-toiminnon.  
4.  Päivitä tai lisää uusi linkkikanta valitsemalla **Linkkikannat**-toiminnon.  
5.  Valitse asianmukainen linkkikanta tai luo uusi rivi painamalla Ctrl + N. Valitse linkkikannan tyyppi tai lisää kuvaus.  
6.  Tuo linkkikanta valitsemalla **Tuo**-toiminto.  
7.  Valitse **Kyllä**, niin voit kohdistaa linkkikannan malliin.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)    
[Business Intelligence](bi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

