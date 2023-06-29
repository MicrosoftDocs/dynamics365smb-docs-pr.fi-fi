---
title: 'Toimintaohje: Raporttien luominen XBRL-kielellä'
description: 'XBRL on XML-pohjainen kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jotta nämä voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="create-reports-with-xbrl"></a><a name="create-reports-with-xbrl"></a>Luo raportteja XBRL-linkityksellä.

> [!NOTE]
> Olemme poistamassa XBRL-raportoinnin toiminnot tuotteesta [!INCLUDE[prod_short](includes/prod_short.md)]. Lue lisää [Vuoden 2022 julkaisuaalto 1:n muutoksista](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL, (e**X**tensible **B**usiness **R**eporting **L**anguage), on XML-pohjainen (eXtensible Markup Language) kieli taloudellisten tietojen merkitsemiseen ja yrityskäyttöön, jonka avulla yritykset voivat tehokkaasti ja tarkasti käsitellä ja jakaa tietojaan. XBRL-aloite sallii lukuisten yrityksen resurssisuunnittelu (ERP) -ohjelmistoyritysten ja kansainvälisten kirjanpitojärjestöjen tekemän maailmanlaajuisen taloudellisen raportoinnin. Aloitteen tavoitteena on tarjota standardi pankkien, sijoittajien ja julkishallinnon taloudellisen tiedon raportointiin. Liiketoiminnan raportointi voi olla:  

* Tilinpäätökset  
* Rahoitukselliset tiedot  
* Muita kuin rahoituksellisia tietoja  
* Säädösten alaisia kirjauksia, kuten vuosittaiset ja neljännesvuosittaiset tilinpäätökset  

> [!NOTE]
> Voit tuoda KP-malleja ja luoda XBRL-instanssiasiakirjoja yhdistämällä tilikartan KP-tietoja rahoitusraportteja varten suunniteltujen taksonomioiden elementteihin, kuten tase- ja tulosraportteihin.
>
> XBRL-ominaisuudet Business Centralissa tukevat taksonomioita erittelyä 2.1 varten. Taksonomiat voivat kuitenkin sisältää muita kuin ei-tuettuja elementtejä, kuten kaavalinkkikannat tai iXBRL (inline XBRL), tai muita rakenteellisia eroja. On suositeltavaa vahvistaa XBRL-ominaisuudet ennen sen käyttöä raportoinnissa.
>
> Taksonomioiden täysi tuki voi vaatia kolmannen osapuolen XBRL-koodausta ja -työkaluja. XBRL International Organization on luettelo työkaluista ja palveluista; tietyn taksonomian XBRL-raportointivaatimusten mukaan haluat ehkä tutustua näihin resursseihin. Lisätietoja on kohdassa [Aloita käyttö yrityksessä](https://go.microsoft.com/fwlink/?linkid=2153466) ja [Työkalut ja palvelut](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a><a name="extensible-business-reporting-language"></a>XBRL (eXtensible Business Reporting Language)

XBRL-taksonomioita ylläpitää www.xbrl.org. Voit ladata taksonomioita ja lukea lisää XBRL-sivustolta.  

Oletetaan, että joku haluaa sinulta taloudellisia tietoja. He antavat sinulle taksonomian (XML-asiakirjan), joka sisältää vähintään yhden mallin ja tällaisessa mallissa on vähintään yksi täytettävä rivi. Rivit vastaavat lähettäjän pyytämiä yksittäisiä taloushallinnon tietoja. Tuot tämän taksonomian ja täytät sitten skeemat kirjoittamalla tilit, jotka vastaavat kutakin riviä ja mitkä laskelmat halutaan, kuten nettomuutos tai päivämäärä. Jossain tapauksissa syötetään vakio, esim. työntekijöiden lkm. Nyt instanssiasiakirja (XML asiakirja) on valmis lähetettäväksi pyytäjälle. Idea on, että tämä on toistuva tapahtuma, joten mikäli taksonomiaan ei tehdä muutoksia, voidaan uusi instanssiasiakirja tuottaa uusilta jaksoilta tarvittaessa.

## <a name="xbrl-comprises-the-following-components"></a><a name="xbrl-comprises-the-following-components"></a>XBRL koostuu seuraavista komponenteista

XBRL **Määrittely** kertoo mitä XBRL on, ja kuinka rakentaa XBRL instanssiasiakirjoja ja -taksonomioita. XBRL-määrittelyt kuvaavat XBRL:ää teknisesti ja ovat tarkoitetut teknisille ihmisille.  

XBRL **Mallit** ovat XBRL alatason komponentteja. Malli on fyysinen XSD-tiedosto (kutsutaan myös XML-skeeman määritelmäksi), joka ilmaisee, kuinka XBRL-instanssiasiakirjat ja taksonomiat tulee rakentaa.

XBRL **Linkkikannat** ovat fyysisiä XML-tiedostoja, jotka sisältävät tietoja XBRL-mallin kuvaamista elementeistä, kuten etiketit yhdellä tai useammalla kielellä, kuinka ne suhtautuvat toisiinsa, kuinka elementtejä summataan, jne.  

XBRL **Taksonomia** on ryhmän luoma “sanakirja”, joka on yhteensopiva XBRL-kuvauksen kanssa, joka mahdollistaa finanssitietojen jakamiseen.  

XBRL **Instanssiasiakirja** on yritysraportti esim. Tilinpäätös, joka on tehty XBRL-määrittelyn mukaan. Arvojen merkitys instanssiasiakirjassa on selitetty taksonomiassa. Tosiasiassa instanssiasiakirja on melko hyödytön mikäli sen luomiseen käytettyä taksonomiaa ei ole käytettävissä.  

## <a name="layered-taxonomies"></a><a name="layered-taxonomies"></a>Kerrostetut taksonomiat

Taksonomia voi koostua perustaksonomiasta, esimerkiksi US GAAP (Yhdysvalloissa yleisesti hyväksytyt kirjanpitoperiaatteet) tai IAS (kansainväliset kirjanpitoperiaatteet), ja sitten sillä voi olla vähintään yksi laajennus. Tämän ilmaisemiseksi taksonomia viittaa yhteen tai useampaan malliin, joista kukin on erillinen taksonomia. Kun lisätaksonomiat on ladattu tietokantaan, uudet elementit yksinkertaisesti lisätään olemassa olevien perään.  

## <a name="linkbases"></a><a name="linkbases"></a>Linkkikannat

XBRL Spec. 2:ssa taksonomia kuvataan useassa XML-tiedostossa. Ensisijainen XML-tiedosto on itse taksonomian mallitiedosto (.xsd-tiedosto), joka sisältää vain järjestelemättömän luettelon raportoitavista elementeistä tai tiedoista. Tämän lisäksi yleensä käytetään joitakin linkkikantatiedostoja (.xml). Linkkikantatiedostot sisältävät dataa, joka täydentää raakaa taksonomiaa (.xsd -tiedosto). Linkkikantatiedostoja on kuutta tyyppiä, joista neljällä on merkitystä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmalle. Nämä ovat:

* Tunnus linkkikanta: Tämä linkkikanta sisältää tunnukset tai nimet tai etiketit elementeille. Tiedosto voi sisältää etikettejä useilla kielillä, jotka on määritetty XML-ominaisuudessa ’lang’. XML-kielitunniste sisältää yleensä kaksikirjaimisen lyhenteen, ja vaikka lyhenteen arvaaminen on melko helppoa sillä ei ole mitään yhteyttä Microsoft Windows -kieleen tai kielikoodeihin, joita on käytetty demodatassa. Eli kun tarkastelet tietyn taksonomian kieliä, näet kaikki tunnukset taksonomian ensimmäiselle elementille eli näet esimerkin kaikista kielistä. Taksonomialla voi olla useita liitettyjä linkkikantoja, kunhan nämä linkkikannat sisältävät eri kielet.  
* Esityslinkkikanta: Tämä linkkikanta sisältää tietoa elementtien rakenteesta, tai tarkemmin sanottuna sen, miten taksonomian julkaisija ehdottaa, että sovellus esittää taksonomian käyttäjälle. Linkkikanta sisältää linkkejä, jotka yhdistävät kaksi elementtiä pää- ja alaelementtien suhteeksi. Kun kaikkia näitä linkkejä käytetään, elementit voidaan esittää hierarkisesti. Huomaa, että esityslinkkikanta käsittelee juuri tätä: elementtien esittämistä käyttäjälle.
* Laskentalinkkikanta: Tämä linkkikanta sisältää tietoa siitä miten elementit summataan. Rakenne on melko samanlainen kuin esityslinkkikannassa, poikkeuksena se, että jokaisella linkillä tai ’kaarella’, kuten niitä kutsutaan, on paino-ominaisuus. Paino voi olla 1 tai –1 ilmaisten sen, että pitääkö elementti lisätä vai vähentää pääelementistään. Huomaa, että summaukset eivät ole välttämättä linjassa visuaalisen esityksen kanssa.  
* Viittauslinkkikanta: Tämä linkkikanta on xml-tiedosto, joka sisältää lisäinformaatiota datasta, jonka taksonomian julkaisija vaatii.

## <a name="set-up-xbrl-lines"></a><a name="set-up-xbrl-lines"></a>Määritä XBRL-rivit

Kun olet tuonut tai päivittänyt taksonomian, skeemojen rivit on täytettävä kaikilla tiedoilla, joita tarvitaan tiettyjen talousraportointivaatimusten täyttämiseksi. Näihin tietoihin kuuluvat yrityksen perustiedot, varsinainen tilinpäätös, liitteitä tilinpäätökseen, erittelyt, jne.  

XBRL-rivit määritellään linkittämällä taksonomiatiedot pääkirjanpitosi tietoihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-taksonomiat**, valitse sitten vastaava linkki.  
2. Valitse **XBRL-taksonomiat**-sivulla luokitus luettelosta.  
3. Valitse **Rivit**-toiminto.  
4. Valitse rivi ja täytä kentät.  
5. Saat tarkat tiedot täytettävistä tiedoista valitsemalla **Tiedot**-toiminnon.  
6. Voit määrittää tilikartan KP-tilien linkittämisen XBRL-riveille valitsemalla **KP-linkitysrivit** -toiminnon.  
7. Voit lisätä huomautuksia raporttiin valitsemalla **Muistiot**-toiminnon.  

   > [!TIP]
   > Jos haluat jättää rivejä pois viedyistä tiedoista, valitse lähdetyypiksi **EI KOHDISTETTAVISSA**.

   > [!NOTE]  
   > Voit viedä vain tietoja, jotka vastaavat **Lähdetyyppi** -kentän valintaa. Näitä tietoja ovat esimerkiksi kuvaukset ja muistiinpanot.  

   > [!NOTE]  
   > Taksonomiat voivat sisältää elementtejä, joita [!INCLUDE[prod_short](includes/prod_short.md)] ei tue. Jos elementti ei ole tuettu, **Lähdetyyppi**-kenttä näyttää **Ei kodistettavissa** ja **Kuvaus**-kentässä näkyy virhesanoma, kuten **Odottamaton tyyppi: "tiettyä tyyppiä ei tunnisteta"**. Jos elementti on vietävä, valitse vastaava lähdetyyppi. Yleensä tämä on vakio tai kuvaus. Näin voit syöttää ja viedä tietoja, mutta tällaisilla elementeillä voi olla kelpoisuussääntöjä, joita ei voi tarkistaa ennen viemistä.

## <a name="import-an-xbrl-taxonomy"></a><a name="import-an-xbrl-taxonomy"></a>XBRL-taksonomian tuominen

Ensimmäinen vaihe XBRL-toiminnon käytössä on se, että tuot taksonomian yrityksesi tietokantaan. Taksonomia koostuu yhdestä tai useammasta mallista ja joistakin linkkikannoista. Kun olet tuonut sekä malli(t) että linkkikannat ja kohdistanut linkkikannat malliin, voit määrittää rivit ja kohdistaa oikeat KP-tilit oikeisiin taksonomian riveihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-taksonomiat**, valitse sitten vastaava linkki.  
2. Luo **XBRL-taksonomiat**-sivulla uusi rivi ja kirjoita taksonomian nimi ja kuvaus.  
3. Valitse ensin **Mallit**, lisää sitten mallin kuvaus.  
4. Voit tuoda mallin valitsemalla **XBRL-mallit**-sivulla **Tuo**-toiminnon ja lataamalla tiedoston tekemällä jonkin seuraavista toimista:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Voit tuoda linkkikannan valitsemalla **XBRL-mallit**-sivulla **Linkkikannat**-toiminnon ja lataamalla tiedoston tekemällä jonkin seuraavista toimista:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Nyt voit kohdistaa linkkikannan malliin tai odottaa. Toista kunnen olet tuonut kaikki linkkikannat.  
7. Kohdista linkkikanta malliin valitsemalla **Kohdista taksonomiaan** -toiminto.  

> [!IMPORTANT]  
> Linkkikannan kohdistaminen voi viedä aikaa, joten sen asemesta, että kohdistaisit kaikki linkkikannat yksitellen niiden tuomisen jälkeen, voit odottaa, kunnes olet tuonut ne kaikki ja kohdistaa ne kaikki samalla kertaa. Voit tehdä tämän valitsemalla **Ei**, kun ohjelma kysyy, haluatko kohdistaa juuri tuomasi linkkikannan malliin. Sitten valitaan rivit, joilla on linkkikannat, jotka halutaan ottaa käyttöön.  

## <a name="update-an-xbrl-taxonomy"></a><a name="update-an-xbrl-taxonomy"></a>XBRL-taksonomian päivittäminen

Kun taksonomia muuttuu tulee nykyinen taksonomia päivittää sen mukaiseksi. Syy päivitykseen voi olla muutos mallissa, linkkikannassa tai uusi linkkikanta. Taksonomian päivittämisen jälkeen tulee vain linkittää rivit muuttuneiden ja uusien rivien kohdalla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XBRL-taksonomiat**, valitse sitten vastaava linkki.  
2. Valitse **XBRL-taksonomiat**-sivulla **Mallit**-toiminto.  
3. Voit päivittää mallin valitsemalla ensin päivitettävän mallin, sitten **Tuo**-toiminnon.  
4. Päivitä tai lisää uusi linkkikanta valitsemalla **Linkkikannat**-toiminnon.  
5. Valitse sopiva linkkikanta tai luo uusi rivi näppäinyhdistelmä <kbd>Ctrl</kbd>+<kbd>N</kbd>. Valitse linkkikannan tyyppi ja lisää kuvaus.  
6. Tuo linkkikanta valitsemalla **Tuo**-toiminto.  
7. Valitse **Kyllä**, niin voit kohdistaa linkkikannan malliin.  

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Taloudelliset liiketoimintatiedot](bi.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
