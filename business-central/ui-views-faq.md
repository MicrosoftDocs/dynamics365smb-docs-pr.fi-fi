---
title: Luettelonäkymien usein kysytyt kysymykset
description: Lisätietoja suodattimien tallentamisesta luettelonäkyminä.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 04/01/2021
ms.author: mikebc
ms.openlocfilehash: c47f7a6ad3f60cf7f2b0cab31e4abc995fdbae12
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783009"
---
# <a name="list-views-faq"></a>Luettelonäkymien usein kysytyt kysymykset
Tässä artikkelissa vastataan kysymyksiin, joita kokeneet käyttäjät usein kysyvät luettelonäkymien käyttämisestä ja suodattimien tallentamisesta.  

### <a name="how-do-views-handle-expressions"></a>Näkyminen tapa käsitellä lausekkeita

Kun tallennat näkymän, jossa on lausekkeita sisältäviä suodattimia (kuten päivämäärävälejä, operaattoreita, avainsanoja tai suodatintunnuksia) lauseke tallennetaan siitä muodostuvien tulosten sijaan. Kun tallennetaan esimerkiksi näkymä, joka suodattaa **Luontipäivämäärä**-kentän lausekkeella `-1W..today`, haettavat tietueet liittyvät aina kuluvaan päivään silloinkin, kun näkymää käytetään seuraavassa kuussa.

### <a name="where-are-list-views-saved"></a>Luettelonäkymien tallennuspaikka

Luettelonäkymät ovat kentän piilottamisen tai siirtymisvalikon muokkaamisen tavoin osa käyttäjän mukautusta, ja ne tallennetaan tietokantaan. Kaikkien mukautusten poistaminen luettelosta poistaa pysyvästi myös omat näkymät ja muut mukautukset, kuten näkymien uudelleenjärjestelyn. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Miksi tallennuskuvaketta ei ole?

On olemassa pari syytä, miksi Tallenna-kuvake ja Asetukset-valikko eivät näy suodatinruudun näkymien vieressä.

Voi olla, että mukautus ei ole käytössä käyttäjän roolille. Tässä tapauksessa sinulla on edelleen käyttöoikeus järjestelmänäkymiin, jotka ovat sivujen vakio-osia. Voit muokata näitä näkymiä, kuten muuttaa tai lisätä suodattimia. Et vain voi tallentaa muutoksia. Toinen syy voi olla se, että etsimäsi sivu on *työkirja*-tyyppinen sivu – ei luettelo.

### <a name="on-which-page-types-can-i-use-list-views"></a>Millä sivutyypeillä luettelonäkymiä voi käyttää?

Näkymät ovat käytettävissä vain luettelosivuilla.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Mistä tiedän, olenko luettelo-tyyppisellä sivulla?

Käytä sivun tarkastusta. Voit avata sivun tarkastuksen painamalla Ctrl + Alt + F1. Etsi sitten **Sivu**-kentästä sanaa **luettelo** sulkeista lopussa.

### <a name="are-views-also-available-on-other-form-factors"></a>Ovatko näkymät käytettävissä myös muissa laitetyypeissä?

Kyllä. Kaikki työpöytäselaimeen tai -sovellukseen tallennetut näkymät ovat käytettävissä myös tableteissa tai älypuhelimessa. Näkymiä ei voi muokata tai mukauttaa mobiililaitteissa.

### <a name="are-my-personal-views-always-accessible"></a>Voinko aina käyttää omia näkymiäni?

Näkyvät ovat käytettävissä luettelosivulla riippumatta siitä, käytätkö siirtymisvalikkoa **Kerro, mitä haluat tehdä** -ikkunaa tai luettelosivun URL-linkkiä. Näkymät eivät ole käytettävissä luettelo-osissa, hauissa tai silloin, kun luettelosivu näkyy valintaikkunana.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Miten alkuperäiset suodattimet palautetaan näkymään sen jälkeen, kun sitä on muokattu?

Valitse suodatinruudun alareunassa **Nollaa suodattimet** -toiminto, jos haluat poistaa näkymään tehdyt suodatusmuutokset sekä palauttaa alkuperäiset suodatetut kentät ja suodatusehdot.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Mitä eroa on näkymien piilottamisella ja poistamisella?

Kun näkymä poistetaan, se poistetaan pysyvästi. Kun näkymä piilotetaan, se piilotetaan tilapäisesti suodatinruudussa, mutta tuoda sen uudelleen näkyviin valitsemalla **Näytä**-toiminnon.

### <a name="how-can-i-share-my-views-with-others"></a>Miten voin jakaa näkymäni muiden kanssa?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tarjoa tapaa jakaa tarkkaa luettelonäkymää. Voit kuitenkin jakaa nykyiset suodattimesi, jotta muut käyttäjät voivat nähdä samanlaisen tietueluettelon. Kopioi vain URL-osoite työpöytäselaimeen ja jaa se työtovereiden kanssa. Suodattimien jakaminen ei kuitenkaan takaa, että vastaanottaja saa täsmälleen saman suodatinjoukon, jonka näet omassa selaimessa.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Voiko näkymiä hakea Kerro, mitä haluat tehdä -ikkunassa?

Ei. **Kerro, mitä haluat tehdä** -ikkuna näyttää vain sivun hakutulokset, mutta tämän jälkeen saat suosikkinäkymäsi yhdellä toiminnolla, kun siirryt sivulle.

### <a name="what-is-shared-layout"></a>Mikä on jaettu asettelu?

Kaikki luettelosivun näkymät jakavat yhteisen sarakeasettelun. Asettelu sisältää näytettävät sarakkeet, niiden järjestyksen, leveyden, kiinnitä-ruudun ja pikasyöttöasetukset. Sarakeasettelun mukauttaminen vaikuttaa luettelosivulla myös muihin saman asettelun jakaviin näkymiin.

Joillakin luettelon järjestelmänäkymien sarakkeilla on yksikölliset asettelut. Ne voivat esimerkiksi järjestää sarakkeet näyttämään vain näkymän kannalta oleellisimmat sarakkeet. Yksilöllisiä asetteluja sisältävät näkymät voi tarkistaa valitsemalla ![Näytä enemmän vaihtoehtoja](media/show-more-options-icon.png "Näytä enemmän vaihtoehtoja") -kuvakkeen ja katsomalla, onko **Jaettu asettelu** -valintaruutu valittu. Käyttäjä voi mukauttaa näkymän sarakkeen asettelua yksiköllisen asettelun avulla, jolloin se ei vaikuta luettelosivun muihin näkymiin. Vain kehittäjät voivat määrittää yksilöllisen sarakeasettelun näkymälle, jolla oli alun perin jaettu asettelu.

### <a name="what-does-the-show-system-filters-link-do"></a>Mitä Näytä järjestelmäsuodattimet -linkin käyttö aiheuttaa?

Joillakin luettelosivuilla suodatinruudun alareunassa näkyy **Näytä järjestelmäsuodattimet**, erityisesti, kun sivulla on järjestelmän määrittämiä suodattimia. Näitä erikoissuodattimia käytetään tavallisesti, kun halutaan näyttää tietueita senhetkisen kontekstin perusteella. Esimerkkinä voisi olla se, että tilausluettelo täytyy suodattaa tietylle asiakkaalle.

Sovelluskehittäjät määrittävät järjestelmäsuodattimet käyttämällä suodatinryhmää 0. Lisätietoja järjestelmäsuodattimista on kohdassa [FilterGroup-metodi](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Sivulla on useita näkymiä, joita en ole luonut. Mistä ne ovat peräisin?

Luettelossa näkyy sekä omia näkymiä että järjestelmänäkymiä. Järjestelmänäkymät voivat olla peräisin liiketoimintasovelluksesta tai laajennuksista tai sitten ne voivat olla roolikohtaisia, jos luettelo on mukautettu roolikohtaisesti.

### <a name="why-do-some-views-provide-fewer-options"></a>Miksi joissakin näkymissä on vähemmän vaihtoehtoja?

Joissakin näkymissä on mahdollista tallentaa vain näkymän kopio, kun taas toisissa ei voi tallentaa näkymän muutoksia. Näkymän luontitapa määrittää näkymässä käytettävissä olevat vaihtoehdot. Näkymiä voi luoda useilla tavoilla:

- Tallennetut omat näkymät
- Liiketoimintasovellukseen vakiona kuuluvat järjestelmänäkymät, laajennusten lisäämät näkymät tai roolikohtaiset näkymät. Toisin kuin omissa näkymissä suodattimiin tehtyjä muutoksia ei voi tallentaa kyseiseen järjestelmänäkymään.
- Vanhat järjestelmänäkymät, jotka ovat osa liiketoimintasovellusta mutta jotka on luotu vanhalla [!INCLUDE[prod_short](includes/prod_short.md)] -versiolla. Näissä näkymissä on vähemmän vaihtoehtoja. Ne voidaan vain tallentaa uutena näkymänä, eikä niitä voi myöskään piilottaa tai järjestää uudelleen. Vanhojen järjestelmänäkymien käyttö lopetetaan tulevassa [!INCLUDE[prod_short](includes/prod_short.md)] -päivityksessä.

### <a name="how-do-i-convert-legacy-system-views"></a>Miten vanhat järjestelmänäkymät muunnetaan?

Vanhat järjestelmänäkymät ovat luettelonäkymiä, jotka kehittäjät loivat vanhalla [!INCLUDE[prod_short](includes/prod_short.md)] -versiolla sijoittamalla ne Roolikeskus-sivulle. Vaikka nämä näkymät näkyvät nyt suoraan luettelosivulla, niiden käyttökokemus on heikennetty ja niissä on vähemmän vaihtoehtoja. Voit muuntaa vanhan järjestelmänäkymän mukautettavaksi omaksi näkymäksi tallentamalla vanhan näkymän uutena näkymänä. Järjestelmänvalvojat voivat valita vastaavasti roolikohtaisten vanhojen näkymien muuntamisen mukauttamalla käyttäjäroolia ja tallentamalla vanhan näkymän uutena roolikohtaisena näkymänä.

Vanhojen järjestelmänäkymien käyttö lopetetaan tulevassa [!INCLUDE[prod_short](includes/prod_short.md)] -päivityksessä.

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Organisaation muut käyttäjät tarvitsevat vastaavanlaiset luettelonäkymät vakiomuotoisena. Mitä voin tehdä?

Omien näkymien käyttäminen on nopeaa ja kätevää, mutta [!INCLUDE[prod_short](includes/prod_short.md)] sisältää myös muita työkaluja, joilla voi määrittää tiettyjen käyttäjäroolien tai organisaation kaikkien käyttäjien tarvitsemia luettelonäkymiä.
 - Kehittäjät voivat mukauttaa ympäristöä ja luoda laajennuksia luettelonäkymiä organisaation kaikille käyttäjille.
 - Muut kuin koodaajat, kuten järjestelmänvalvojat tai osastopäälliköt, voivat luoda roolikohtaisia luettelonäkymiä mukauttaessaan roolia **Profiilit (roolit)** -sivulla.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Käytän työssäni useita kieliä. Miten näkymän nimi käännetään?

Kun uusi näkymä tallennetaan tai aiemmin luodulle näkymälle annetaan uusi nimi, kyseiselle näkymälle on annettava tunnistettava ja merkityksellinen nimi. Nimi tallennetaan käytössä olevalla kielellä, ja se näkyy myös silloin, kun sinä tai muut käyttäjät käyttävät erikielisiä [!INCLUDE[prod_short](includes/prod_short.md)] -versioita. Jos haluat tarjota käännettyjä näkymän nimiä, vaihda kieli **Omat asetukset** -sivun avulla. Nimeä sitten näkymä uudelleen, jolloin käännetty nimi tallennetaan uudelle kielelle.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Voiko lausekkeita sisältäviä näkymiä käyttää kaikilla kielillä?

Vain symboleja, kuten `|` tai `..`, käyttäviä lausekkeita voi käyttää huoletta millä tahansa kielellä. Jos näkymän lausekkeissa on kirjaimia, avainsanoja tai suodatintunnuksia, niiden käyttö on mahdollista vain lausekkeiden luontikielellä.

### <a name="see-also"></a>Katso myös

[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Toimintojen ja tietojen etsiminen](ui-search.md)  
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]