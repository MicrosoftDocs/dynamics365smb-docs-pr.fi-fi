---
title: Luettelonäkymien usein kysytyt kysymykset
description: Lisätietoja suodattimien tallentamisesta luettelonäkyminä.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 01/01/2019
ms.author: mikebc
ms.openlocfilehash: d2caa1d9b84d99c0b43a70bca1c45da81138f7b9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316831"
---
# <a name="list-views-faq"></a>Luettelonäkymien usein kysytyt kysymykset
Tässä ohjeaiheessa vastataan kysymyksiin, joita kokeneet käyttäjät usein kysyvät luettelonäkymien käyttämisestä ja suodattimien tallentamisesta.  

### <a name="how-do-views-handle-expressions"></a>Näkyminen tapa käsitellä lausekkeita
Kun tallennat näkymän, jossa on lausekkeita sisältäviä suodattimia, kuten päivämäärävälejä, operaattoreita, avainsanoja tai suodatintunnuksia, lauseke tallennetaan siitä muodostuvien tulosten sijaan. Kun tallennetaan esimerkiksi näkymä, joka suodattaa **Luontipäivämäärä**-kentän lausekkeella **-1V..tänään**, haettavat tietueet liittyvät aina kuluvaan päivään silloinkin, kun näkymää käytetään seuraavassa kuussa.

### <a name="where-are-list-views-saved"></a>Luettelonäkymien tallennuspaikka
Luettelonäkymät ovat kentän piilottamisen tai siirtymisvalikon muokkaamisen tavoin osa käyttäjän mukautusta, ja ne tallennetaan tietokantaan. Kaikkien mukautusten poistaminen luettelosta poistaa pysyvästi myös omat näkymät ja lisämukautukset, kuten näkymien uudelleenjärjestelyn. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a>Miksi tallennuskuvaketta ei ole?
Tallennuskuvake ja asetusvalikko eivät näy näkymien vieressä suodatinruudussa, jos mukautus on poistettu käyttäjäroolissa käytöstä. Vaikka mukautus ei olisi otettu käyttäjillä käyttöön, he voivat silti käyttää sivuun vakiona kuuluvia järjestelmänäkymiä sekä muokata tai luoda suodattimia.

### <a name="on-which-page-types-can-i-use-list-views"></a>Millä sivutyypeillä luettelonäkymiä voi käyttää?
Näkymät ovat käytettävissä vain luettelo-ja työkirjasivuilla.

### <a name="are-views-also-available-on-other-form-factors"></a>Ovatko näkymät käytettävissä myös muissa laitetyypeissä?
Kyllä. Kaikki työpöytäselaimeen tai -sovellukseen tallennetut näkymät ovat käytettävissä myös tableteissa tai älypuhelimessa. Näkymiä ei voi muokata tai mukauttaa mobiililaitteissa.

### <a name="are-my-personal-views-always-accessible"></a>Voinko aina käyttää omia näkymiäni?
Samat näkyvät ovat käytettävissä luettelosivulla riippumatta siitä, käytätkö siirtymisvalikkoa **Kerro, mitä haluat tehdä** -ikkunaa tai luettelosivun URL-linkkiä. Näkymät eivät ole käytettävissä luettelo-osissa, hauissa tai silloin, kun luettelosivu näkyy valintaikkunana.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Miten alkuperäiset suodattimet palautetaan näkymään sen jälkeen, kun sitä on muokattu?
Valitse suodatinruudun alareunassa **Nollaa suodattimet** -toiminto, jos haluat poistaa näkymään tehdyt suodatusmuutokset sekä palauttaa alkuperäiset suodatetut kentät ja suodatusehdot.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Mitä eroa on näkymien piilottamisella ja poistamisella?
Kun näkymä poistetaan, se poistetaan pysyvästi. Kun näkymä piilotetaan, se piilotetaan tilapäisesti suodatinruudussa, mutta tuoda sen uudelleen näkyviin valitsemalla **Näytä**-toiminnon.

### <a name="how-can-i-share-my-views-with-others"></a>Miten voin jakaa näkymäni muiden kanssa?
Vaikka [!INCLUDE[d365fin](includes/d365fin_md.md)] ei mahdollista täsmällisen luettelonäkymän jakamista, voit jakaa nykyiset suodattimet, jolloin muut käyttäjät näkevät samankaltaisen tietueluettelon. Kopioi vain URL-osoite työpöytäselaimeen ja jaa se työtovereiden kanssa. Suodattimien jakaminen ei kuitenkaan takaa, että vastaanottaja saa täsmälleen saman suodatinjoukon, jonka näet omassa selaimessa.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Voiko näkymiä hakea Kerro, mitä haluat tehdä -ikkunassa?
Ei. **Kerro, mitä haluat tehdä** -ikkuna näyttää vain sivun hakutulokset, mutta tämän jälkeen saat suosikkinäkymäsi yhdellä toiminnolla, kun siirryt sivulle.

### <a name="what-is-shared-layout"></a>Mikä on jaettu asettelu?
Kaikki luettelosivun näkymät jakavat saman sarakeasettelun, joka määrittää näytettävät sarakkeet sekä niiden järjestyksen ja leveyden, kiinnitysruudun ja pikatapahtuma-asetukset. Sarakeasettelun mukauttaminen vaikuttaa luettelosivulla myös muihin saman asettelun jakaviin näkymiin.

Joillakin luettelon järjestelmänäkymien sarakkeilla on yksikölliset asettelut. Ne voivat esimerkiksi järjestää sarakkeet näyttämään vain näkymän kannalta oleellisimmat sarakkeet. Yksilöllisiä asetteluja sisältävät näkymät voi tarkistaa valitsemalla ![Näytä enemmän vaihtoehtoja](media/show-more-options-icon.png "Näytä enemmän vaihtoehtoja") -kuvakkeen ja katsomalla, onko **Jaettu asettelu** -valintaruutu valittu. Käyttäjä voi mukauttaa näkymän sarakkeen asettelua yksiköllisen asettelun avulla, jolloin se ei vaikuta luettelosivun muihin näkymiin. Vain kehittäjät voivat määrittää yksilöllisen sarakeasettelun näkymälle, jolla oli alun perin jaettu asettelu.

### <a name="what-does-the-show-system-filters-link-do"></a>Mitä Näytä järjestelmäsuodattimet -linkin käyttö aiheuttaa?
Joillakin luettelosivuilla suodatinruudun alareunassa näkyy **Näytä järjestelmäsuodattimet**, kun sivulla on järjestelmän määrittämiä suodattimia. Näillä erikoissuodattimilla näytetään tyypillisesti tietueita nykyisen kontekstin perusteella. Kyse voi olla esimerkiksi tietyn asiakkaan mukaan suodatettavasta tilausluettelosta.

Kehittäjät määrittävät järjestelmäsuodattimet käyttämällä suodatinryhmää 0. Teknisiä lisätietoja järjestelmäsuodattimista on kohdassa [Suodatinryhmä-toiminto](https://docs.microsoft.com/en-us/dynamics-nav/filtergroup-function--record-)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>Sivulla on useita näkymiä, joita en ole luonut. Mistä ne ovat peräisin?
Luettelossa näkyy sekä omia näkymiä että järjestelmänäkymiä. Järjestelmänäkymät voivat olla peräisin liiketoimintasovelluksesta tai laajennuksista tai sitten ne voivat olla roolikohtaisia, jos luettelo on mukautettu roolikohtaisesti.

### <a name="why-do-some-views-provide-fewer-options"></a>Miksi joissakin näkymissä on vähemmän vaihtoehtoja?
Joissakin näkymissä on mahdollista tallentaa vain näkymän kopio, kun taas toisissa ei voi tallentaa näkymän muutoksia. Näkymän luontitapa määrittää näkymässä käytettävissä olevat vaihtoehdot. Näkymiä voi luoda useilla tavoilla:
- Tallennetut omat näkymät
- Liiketoimintasovellukseen vakiona kuuluvat järjestelmänäkymät, laajennusten lisäämät näkymät tai roolikohtaiset näkymät. Toisin kuin omissa näkymissä suodattimiin tehtyjä muutoksia ei voi tallentaa kyseiseen järjestelmänäkymään.
- Vanhat järjestelmänäkymät, jotka ovat osa liiketoimintasovellusta mutta jotka on luotu vanhalla [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiolla. Näissä näkymissä on selkäesti vähemmän vaihtoehtoja. Ne voidaan vain tallentaa uutena näkymänä, eikä niitä voi myöskään piilottaa tai järjestää uudelleen. Huomaa, että vanhojen järjestelmänäkymien käyttö lopetetaan tulevassa [!INCLUDE[d365fin](includes/d365fin_md.md)] -päivityksessä.

### <a name="how-do-i-convert-legacy-system-views"></a>Miten vanhat järjestelmänäkymät muunnetaan?
Vanhat järjestelmänäkymät ovat luettelonäkymiä, jotka kehittäjät loivat vanhalla [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiolla sijoittamalla ne Roolikeskus-sivulle. Vaikka nämä näkymät näkyvät nyt suoraan luettelosivulla, niiden käyttökokemus on heikennetty ja niissä on selkeästi vähemmän vaihtoehtoja. Voit muuntaa vanhan järjestelmänäkymän mukautettavaksi omaksi näkymäksi tallentamalla vanhan näkymän uutena näkymänä. Järjestelmänvalvojat voivat valita vastaavasti roolikohtaisten vanhojen näkymien muuntamisen mukauttamalla käyttäjäroolia ja tallentamalla vanhan näkymän uutena roolikohtaisena näkymänä.

Huomaa, että vanhojen järjestelmänäkymien käyttö lopetetaan tulevassa [!INCLUDE[d365fin](includes/d365fin_md.md)] -päivityksessä.

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Organisaation muut käyttäjät tarvitsevat vastaavanlaiset luettelonäkymät vakiomuotoisena. Mitä voin tehdä?
Omien näkymien käyttäminen on nopeaa ja kätevää, mutta [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää myös muita työkaluja, joilla voi määrittää tiettyjen käyttäjäroolien tai organisaation kaikkien käyttäjien tarvitsemia luettelonäkymiä.
 - Kehittäjät voivat mukauttaa ympäristöä ja luoda laajennuksia luettelonäkymiä organisaation kaikille käyttäjille.
 - Muut kuin koodaajat, kuten järjestelmänvalvojat tai osastopäälliköt, voivat luoda roolikohtaisia luettelonäkymiä mukauttaessaan roolia **Profiilit (roolit)** -sivulla.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Käytän työssäni useita kieliä. Miten näkymän nimi käännetään?
Kun uusi näkymä tallennetaan tai aiemmin luodulle näkymälle annetaan uusi nimi, kyseiselle näkymälle on annettava tunnistettava ja merkityksellinen nimi. Nimi tallennetaan käytössä olevalla kielellä, ja se näkyy myös silloin, kun sinä tai muut käyttäjät käyttävät erikielisiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versioita. Voit antaa näkymän nimen käännöksen vaihtamalla kielen **Omat asetukset** -sivulla ja antamalla näkymälle uuden nimen, jolloin käännetty nimi tallennetaan uudella kielellä.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Voiko lausekkeita sisältäviä näkymiä käyttää kaikilla kielillä?
Vain symboleja, kuten **|** tai **..**, käyttäviä lausekkeita voi käyttää huoletta millä tahansa kielellä. Jos näkymän lausekkeissa on kirjaimia, avainsanoja tai suodatintunnuksia, niiden käyttö on mahdollista vain lausekkeiden luontikielellä.


### <a name="see-also"></a>Katso myös  
[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Toimintojen ja tietojen etsiminen](ui-search.md)    
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
