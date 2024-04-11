---
title: Luetteloiden tietojen analysointi Copilotin avulla (esiversio)
description: Tietoja tietojen analysoinnista Business Centralin Copilotin avulla.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Luetteloiden tietojen analysointi Copilotin avulla (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Tässä artikkelissa käsitellään luettelosivujen tietojen analysointia *analyysiavustajan* avulla.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Tietoja analyysiavustajasta

Analyysiavustaja on Business Centralin luettelosivujen [analyysitilan](analysis-mode.md) Copilot. Tämä analyysitila mahdollistaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Analysoidessa tietoja analyysitilassa luodaan *analyysin* välilehti, jossa tiedot muunnetaan näyttämään toivotut koosteet ja yhteenvedot. Kentät voidaan esimerkiksi järjestää riveiksi ja sarakkeiksi, suodattimet määrittää, sarakkeet lajitella ja kenttiä käyttää pivot-toimintona. Analyysiavustajan avulla tätä tehtävää ei tarvitse tehdä manuaalisesti vaan samaan (tai ainakin alkuun) päästään käyttämällä sanoja. Toivottu rakenne ilmaistaan luonnollisella kielellä, kuten lajittele määrä pienimmästä suurimpaan tai näytä keskimääräinen kustannus luokkakohtaisesti, ja analyysiavustaja käyttää tekoälyä luomaan ehdotetun asettelun analyysivälilehteen.


<!-- 

 However, the data analysis mode requires some understanding of how to structure fields to meet the desired aggregations and summarizations. It requires you to move fields around to the appropriate areas within analysis mode pane which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals. Analysis assist minimizes these requirments by enabling you to express the desired layout in words. , like "group which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals
--> 
## Vaatimukset

- Analyysiavustajaominaisuus on aktivoitu ja sen käyttöoikeus on myönnetty. Tämä tehtävän suorittaa yleensä järjestelmänvalvoja. [Lisätietoja Copilotin ja tekoälyominaisuuksien määrittämisestä](enable-ai.md).
- Business Centralin näyttökieleksi on määritetty jokin seuraavista englannin kielialueista: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Lisätietoja kielen vaihtamisesta](ui-change-basic-settings.md#language).
- Business Central -ympäristö on jossain muussa maassa tai muulla alueella kuin Kanadassa. (Tämä ominaisuus ei ole vielä saatavana Kanadassa.)

<!--
> [!NOTE]
> You may notice some list pages that don't include the **Analyze** switch for changing to the analysis mode. The reason is that developers can disable analysis mode on specific pages by using the [AnalysisModeEnabled property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.-->

## Aloittaminen

1. Avaa analysoitava luettelosivu.

   Esimerkiksi **Nimikkeet**-sivua voidaan käsitellä valitsemalla ![Suurennuslasi, joka avaa Kerro minulle -ominaisuuden.](media/ui-search/search_small.png) -kuvake, (<kbd>Alt</kbd>+<kbd>Q</kbd>), syöttämällä *Nimikkeet* ja valitsemalla sitten vastaava linkki.

1. Tietojen analysoinnin Copilotin avulla voi aloittaa suoraan luettelosivulta tai siirtymällä ensin analyysitilaan. Pääset alkuun jollakin seuraavista tavoista:

    - Valitse sivun yläosan toimintopalkissa ![Näkyvissä avustajakuvake](media/copilot-icon.png) **Copilot** > **Analysoi luettelo**.
    - Valitse sivun yläosan toimintopalkissa ![Näkyvissä analyysitilaan siirtymiskuvake](media/analysis-mode-icon.png) **Siirry analyysitilaan** ja valitse sitten ![Näkyvissä avustajakuvake](media/copilot-icon.png) **Copilot** > **Luo uusi analyysi**.

1. Kirjoita **Analysoi** Copilotin avulla -ikkunaan toivotun asettelu kuvaus. Tätä Kuvausta kutsutaan *kehotteeksi*.

    ![Näkyvissä analyysiavustajan Copilot](media/analysis-assist.png)

    > [!TIP]
    > Ohjeita kehotteen kirjoittamiseen saa valitsemalla ![Näkyvissä kehotteen näyttämiskuvake](media/prompt-guide-icon.png) **Kehoteopas** ja valitsemalla aloituskohdaksi yhden vaihtoehdoista. Suluissa `[ ]` oleva teksti on esimerkki eikä sitä ole Copilot-ikkunassa.

1. Valitse **Luo** ja odota, kun Copilot luo uuden analyysivälilehden asettelun.
1. Tarkista uuden analyysivälilehden tulokset.

   > [!NOTE]
   > Jos uudesta analyysivälilehdestä siirrytään pois (esimerkiksi toiseen analyysivälilehdelle tai toiselle sivulle) tai välilehden asetteluun tehdään muutoksia (kuten sarakkeiden lajitteluun tai asetuksiin **Sarakkeet**- ja **Analyysisuodattimet**-välilehdissä), uusi analyysivälilehti tallennetaan automaattisesti ja Copilot sulkeutuu.

1. Luotuun analyysiin voidaan tehdä muutoksia jommallakummalla tavalla:

   - Aiempia ohjeita voi hyödyntää kirjoittamalla tiedot **Lisää analyysia koskevia muita tietoja** -ruutuun ja valitsemalla sitten ![Näkyvissä muuttamisnuoli](media/analysis-assist-adjust-button.png) **Muuta**-nuolen. Copilot muistaa aiemmat ohjeet ja käyttää niitä muutosten tekemiseen.

   - Alusta voi aloittaa lisäämällä uudet ohjeet, valitsemalla ![Näkyvissä kehotteen muokkauksen kynäkuvake](media/edit-pencil.png) **Muokkaa kehotetta:**, lisäämällä tiedot kehotteeseen ja valitsemalla sitten **Luo**.

1. Jos haluat tallentaa analyysivälilehden, valitse **Säilytä se**. Jos et halua tallentaa sitä, valitse **Hylkää**.

## Kehotetta koskevia vihjeitä ja esimerkkejä

Copilotin tehokkaiden kehotteiden luonnissa on olennaista saada täsmällisiä ja osuvia analyysiehdotuksia. Lisäksi on keinoja, joilla kehotteisiin lisättävän tekstin voi minimoida, mikä nopeuttaa kirjoittamista. Seuraavassa on vihjeitä ja ohjeita sekä esimerkkejä:

- Käytä lyhyitä lauseita pitkien tai useiden lauseiden sijaan.
- Varmista, että kehotteissa käytettävien kenttien nimet muistuttavat riittävästi sivulla olevien kenttien nimiä.
- Käytä luonnollista kieltä sekä ilmaise toivottu tietorakenne ystävällisesti ja keskustelunomaisesti.
- Käytä yleisiä tietoanalyyseissa käytettyjä avainsanoja, fraaseja ja termejä, kuten `group by`, `sum` ja `sort by`.
- Jos ensimmäisen vastaus ei ole toivotunlainen, lisää seurantaohjeita tai muotoile viimeisen ohje uudelleen.
- Yleisiä lyhenteitä voi käyttää.
- Kirjainkoolla ei ole merkitystä.

### Esimerkkejä

Seuraavissa kehote-esimerkeissä käytetään analyysiavustajaa **Nimikkeet**-luettelossa. Nimikesivulla on kolme analyysissa käytettävää yhteenlaskettavia kenttiä: **Varastosaldo**, **Yksikkökustannus** ja **Yksikköhinta**.

Kehote: `Show items by brand and unit of measure`

Tämä kehote yrittää näyttää kaikkien yhteenlaskettavien kenttien yhteissummat brändin ja **Perusmittayksikkö**-kentän mukaan ryhmiteltynä. Tässä tapauksessa brändi ei vastaa minkään kentän nimeä, joten Copilot ei todennäköisesti löydä vastaavaa kenttää, joten se pyytää muotoilemaan kehotteen uudelleen ja yrittämään uudelleen.

Kehote: `Show items by type and uom`

Tämä kehote näyttää kaikkien yhteenlaskettavien kenttien yhteissummat **Tyyppi**-kentän ja **Perusmittayksikkö**-kentän mukaan ryhmiteltynä. Sen sijaan että kirjoitettaisiin mittayksikkö, käytetään lyhennettä `uom`.

Kehote: `Show total quantity per type per UoM`

Tämä kehote luo pivot-taulukon **Varastosaldo**-kentän, **Perusmittayksikkö**- ja **Tyyppi**-kentän mukaan.

## Katso myös

[Vastuullisen tekoälyn usein kysyttyjä kysymyksiä analyysiavustajasta](faqs-analysis-assist.md)  
[Tapauskohtainen tietoanalyysi](reports-adhoc-analysis.md)  
