---
title: Roolien sivujen mukauttaminen
description: 'Lisätietoja profiilin (roolin) käyttöliittymän mukauttamisesta siten, että kaikki käyttäjät, joille kyseinen rooli on määritetty, näkevät mukautetun työtilan.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# Profiilien sivujen mukauttaminen

Business Central sisältää sekä käyttäjien että järjestelmänvalvojien [mukauttamisen](ui-personalization-user.md). Mukauttamisen avulla käyttäjät voivat räätälöidä työtilaansa muokkaamalla sivun asetuksia omien mieltymystensä mukaan. Järjestelmänvalvojat voivat mukauttaa tietyn profiilin sivujen asetteluja liiketoiminnan roolien tai osastojen perusteella esimerkiksi siten, että kaikki määritetyt käyttäjät näkevät saman mukautetun sivun. Mukauttamisen ansiosta käyttäjät voivat näyttää, piilottaa ja siirtää sivun kenttiä ja toimintoja. Järjestelmänvalvojien käyttämä mukauttaminen sisältää myös muita ominaisuuksia. Järjestelmänvalvojien tekemä mukauttaminen mahdollistaa niiden kenttien näyttämisen, jotka ovat lähdetaulukossa tai laajennustaulukoissa, mutta joita ei ole määritetty sivuobjektissa. Tämä ei ole mahdollista käyttäjän tekemässä mukautuksessa.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli. Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.

Sivun mukauttaminen aloitetaan **Profiilit (roolit)** -sivulla, josta järjestelmänvalvojat aloittavat yksittäisten profiilikorttien käyttäjien profiilien hallinnan. Sivun asettelun mukauttamisen lisäksi voi kunkin profiilin **Profiili (rooli)** -sivulla voi hallita useita muita profiilien asetuksia. Lisätietoja on kohdassa [Profiilien hallinta](admin-users-profiles-roles.md).

## Vaatimukset

- Business Central -tilillä on oltava **D365-profiilin hallinnan** käyttöoikeuksien joukko tai vastaavat käyttöoikeudet. 

   **D365-profiilin hallinnan** käyttöoikeuksien joukko sisältää **9026 Lisää kenttä taulukkoon** -järjestelmäobjektin suoritusoikeuden. Jos tätä käyttöoikeutta ei ole, käyttäjä ei voi lisätä kenttiä sivulle, jos niitä ei ole määritetty sivuobjektissa. 

## Sivujen mukauttaminen profiilia varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten vastaava linkki.
2. Valitse ensin sen profiilin rivi, jonka sivuja haluat mukauttaa, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Mukauta sivuja** -toiminto.

    [!INCLUDE[prod_short](includes/prod_short.md)] avaa valitun profiilin uudessa selaimen välilehdessä siten, että **Mukauttaminen**-palkki on aktivoitu. **Mukauttaminen**-palkissa on samat toiminnot kuin käyttäjien käyttämässä **Mukautus**-palkissa.

4. Mukauta sivuja kyseisen roolin tai osaston tarpeiden mukaan samalla tavoin kuin käyttäjä tekee omat mukautuksensa. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

    > [!NOTE]
    > Voit siirtyä mukauttamisen aikana käyttämällä toiminnossa <kbd>Ctrl</kbd>+<kbd>napsautus</kbd>-yhdistelmää, jos nuolenpää osoittaa toiminnon olevan valittuna.

5. Kun olet muuttanut yhden tai usean sivun asettelua, valitse**Mukauttaminen**-palkissa **Valmis**-painike.
6. Sulje selaimen välilehti.

Sivujen mukauttaminen on nyt tallennettu profiiliin.

## Kaikkien profiilin mukautettujen sivujen näyttäminen

Saat tarvittaessa yleiskuvan profiiliin mukautetuista sivuista, mikä auttaa suunnittelemaan esimerkiksi sivujen lisämukautuksia tai poistamisia.

- Valitse **Profiili (rooli)** -sivulla **Hallitse mukautettuja sivuja** -toiminto.

**Mukautetut sivut** -sivulla voit poistaa mukautuksia ja tehdä vian määrityksen tarkistamalla mahdolliset ongelmat.  

## Profiilin kaikkien mukautusten poistaminen

Voit peruuttaa kaikki profiiliin tehdyt mukautukset. Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta. Voit poistaa kaikki mukautukset toisella toiminnolla. Lisätietoja on kohdassa [Kaikkien käyttäjän tekemien mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Valitse mukautetun profiilin **Profiili (rooli)** -sivulla **Poista mukautetut sivut** -toiminto.

Profiilin sivujen asetteluksi palautetaan oletusasettelu.  

## Profiilin tiettyjen sivujen mukautusten poistaminen

Voit poistaa profiilin yksittäisen sivun mukautukset. Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta. Voit poistaa tietyn sivun mukautukset toisella toiminnolla. Lisätietoja on kohdassa [Tiettyjen sivujen mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Valitse **Profiili (rooli)** -sivulla **Hallitse mukautettuja sivuja** -toiminto.
2. Valitse **Mukautetut sivut** -sivulla vähintään yhden poistettavan sivun mukautuksen rivi ja valitse sitten **Poista**-toiminto.

Valitun sivun asettelu muutetaan vastaamaan tekemiäsi muutoksia.

## Kentän lisääminen

Voit lisätä sivulle kenttiä **Lisää kenttä sivulle** -ruudussa. Se avataan valitsemalla **+ Kenttä** -toiminto mukautustilassa. On tärkeä ymmärtää, että **Lisää kenttä sivulle** -ruutua käytetään näytettäessä kentät, jotka ovat jo joko sivulla tai sen lähdetaulukoissa, mutta jotka parhaillaan ovat piilotettuina näkymässä. Uusia kenttiä ei voi luoda.

**Lisää kenttä sivulle** -ruudussa ovat kaikki kentät, jotka voidaan näyttää sivulla. Kentät on jaettu seuraaviin luokkiin sivun rakenteen, sen lähdetaulukon ja laajennusten taustalla olevan rakenteen mukaan:

|Luokka|Kuvaus|
|-|-|
|Taulukon kentät eivät ole sivuobjektissa|Sisältää kenttiä, jotka on määritetty perustaulukossa tai laajennustaulukoissa, mutta joita ei ole määritetty sivulla. Näiden kenttien työkaluvihje sisältää **Taulukon määrittämä** -selitteen.<br><br>|
|Taulukkoon sidotut sivukentät|Sisältää kentät, jotka on määritetty perustaulukossa tai taulukon laajennuksissa, ja jotka on määritetty myös sivulla näkyviksi tai piilotetuiksi. Näiden kenttien työkaluvihje sisältää **Sivun määrittämä** -selitteen.|
|Sivukentät, joita ei ole sidottu taulukkoon| Kentät, jotka on määritetty vain sivulla, ei perustaulukossa tai laajennustaulukoissa. Näitä kenttiä käytetään yleensä muuttujassa tai laskennassa. Näiden kenttien työkaluvihje sisältää **Sivun määrittämä** -selitteen.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Luettelon yläpuolella olevan suodatuspainikkeen avulla voit muuttaa kenttien luokan, joka esiintyy **Lisää kenttä sivulle** -ruudussa.  

:::image type="content" source="media/customization-filter.svg" alt-text="Näyttää suodatuspainikkeen Lisää kenttä -ruudussa mukautustilassa.":::
 
### Lisää taulukkokenttä, joka ei ole sivuobjektissa

Jos haluat määrittää vain taulukko -kentän sivulla käytettäväksi käyttäjille, lisää se ensin sivulle. Kun olet lisännyt kentän, käyttäjät voivat halutessaan näyttää tai piilottaa kentän mukauttamisen avulla. Kentän voi lisätä muutamalla eri tavalla.

- Sen voi esimerkiksi vetää **Lisää kenttä sivulle** -ruudusta haluttuun kohtaan.
- Toinen tapa on valita kenttä ruudussa ja näyttää suositeltu sijainti sivulla. Siirry sitten kentän sijaintiin sivuilla, valitse nuolenpää ja valitse sitten **Lisää**. 

Kun kenttä on lisätty,  **Lisää kenttä sivulle** -ruudun kentän työkaluvihjeeksi tulee **Sivun määrittämä**. Lisätty kenttä on lukittu, eikä sitä siis voi muokata. Lukitusta ei myöskään voi poistaa.

## Kentän poistaminen

Jos olet lisännyt taulukkokentän, joka ei alun perin ollut sivuobjektissa, voit poistaa sen uudelleen. Kentän poistaminen on eri asia kuin sen piilottaminen. Kun piilotat kentän, käyttäjät voivat yhä näyttää sen työtilassa mukauttamisen avulla. Jos poistat kentän, käyttäjät eivät voi enää näyttää kenttää tai piilottaa sitä. Jos kenttä on tällä hetkellä näkyvissä käyttäjän työtilassa, se katoaa sieltä poistamisen jälkeen. 

Voit poistaa kentän valitsemalla sivun kentässä olevan nuolenpään ja valitsemalla sitten **Poista**. Jos et löydä kenttää, valitse se **Lisää kenttä sivulle** -ruudussa osoittaaksesi sen piilotetun sijainnin. 

> [!IMPORTANT]
> Kentän poistaminen ei poista tietoja, jotka on tallennettu kenttään tai sen lähdetaulukoihin. Kenttä vain poistetaan näkyvistä. 

## Muokkaamisen lukitseminen ja lukituksen poistaminen

Järjestelmänvalvojan tekemän mukauttamisen avulla sivun useimmat kentät voidaan lukita (muokkaus sallitaan) ja niiden lukitus voidaan poistaa (muokkaus estetään). Voit lukita kentän tai poistaa sen lukituksen valitsemalla kentän sivulla ja valitsemalla sitten nuolenpään. Valitse lopuksi **Lukitse muokkaus** tai **Poista muokkauksen lukitus**. On tärkeää pitää mielessä muutama kenttien lukitsemista ja lukituksen poistamista koskeva seuraava sääntö:

- Kentät, jotka alun perin eivät olleet sivuobjektissa, vaan lisättiin sivulle mukauttamisen avulla, ovat aina lukittuja. Niiden lukitusta ei voi poistaa järjestelmänvalvojan tai käyttäjän tekemän mukauttamisen avulla.
- Kentän rakenne voi myös estää kentän muokkaamisen. Jos AL-kehittäjä on määrittänyt kentän [Editable-ominaisuuden](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) arvoksi `false`, kenttä on aina lukittuna, eikä sen lukitusta voi poistaa.
- On tärkeää huomioida, että muokkauksen lukitustoiminto on tarkoitettu tietojen tarkkuuden, yhdenmukaisuuden ja luotettavuuden parantamiseksi. Sitä ei ole tarkoitettu tietojen eheyden turvaamiseksi.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Tärkeitä tietoja ja vinkkejä 

- Kaikki kentät eivät välttämättä ole mukautettavissa **Lisää kenttä sivulle** -ruudussa. Taulukon kehittäjä voi estää kenttää näkymästä mukautuksessa määrittämällä kentän [AllowInCustomization-ominaisuuden](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) arvoksi `false`.
- Sivua, joka ei ole [analyysitilassa](analysis-mode.md), ei voi mukauttaa. **Analysoi**-vaihtopainikkeen aktivointi on poistettu. Jos siirryt mukautustilaan sivun ollessa analyysitilassa, analysointitila poistetaan automaattisesti käytöstä. 
- Joillakin sivuilla on useita sivukenttiä, jotka on linkitetty samaan lähdetaulukkoon. **Lisää kenttää sivulle** -ruudussa näkyvät kaikki nämä sivukentät erikseen. Voit näyttää, piilottaa tai siirtää näitä kenttiä itsenäisesti ilman, että ne vaikuttavat muihin kenttiin.
- Jos osa tai ryhmä on piilotettu, voit yhä tunnistaa osan tai ryhmän sisällä olevat piilotetut kentät. Et kuitenkaan voi lisätä, siirtää tai näyttää kenttiä osassa tai ryhmässä ennen kuin ne on määritetty näkyviksi. 
## Katso myös

[Oman työtilan mukauttaminen](ui-personalization-user.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
