---
title: Markkinointitekstin lisääminen nimikkeille
description: Kirjoita markkinointiteksti Business Central -sovelluksen nimikkeille.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Markkinointitekstin lisääminen nimikkeille

Voit kirjoittaa nimikettä koskevan *markkinointitekstin* mille tahansa Business Centralin rekisteröidylle nimikkeelle. Vaikka markkinointiteksti on eräänlainen kuvaus, se on eri kuin nimikkeen **Kuvaus**-kenttä. **Kuvaus**-kenttää käytetään tyypillisesti suppeana näyttönimenä, jotta tuote voidaan määrittää nopeasti. Toisaalta markkinointiteksti on rikas ja kuvaava teksti. Sen tarkoitus on lisätä markkinointi-ja mainossisältöä, joka tunnetaan myös nimellä *copy*. Tämä teksti voidaan sitten julkaista tuotteen kanssa, jos se on julkaistu verkkokaupassa, kuten Shopifyssa, tai liittää sähköposteihin tai muihin asiakkaiden kanssa käytäviin keskusteluihin.

Markkinointitekstin voi luoda kahdella tavalla. Helpoin tapa päästä alkuun on käyttää Copilotia, mikä ehdottaa sinulle tekoälyn luomaa tekstiä. Toinen vaihtoehto on aloittaa tyhjästä. 

## <a name=copilot></a>Copilotin avulla luotujen markkinointitekstiehdotusten hakeminen

Copilot luo nopeasti tekstiehdotuksen, joka luodaan puolestasi automaattisesti. Tekoälyn luoma teksti on räätälöity nimikkeelle ja se antaa hyvän lähtökohdan. Teksti perustuu seuraaviin tietoihin:

- Nimikkeelle määritetyt määritteet – esimerkiksi kuvaus, väri, dimensiot, materiaali ja niin edelleen. [Lisätietoja on nimikemääritteistä](inventory-how-work-item-attributes.md).
- Nimikkeen **Kuvaus**-kenttä.
- Nimikeluokka. [Lisätietoja nimikkeiden luokittelusta](inventory-how-categorize-items.md).
- Valittavissa olevat tyyliasetukset, kuten äänensävy, muoto ja pituus.

Copilot on suunniteltu säästämään sinua ja auttamaan luovan ja mukaansatempaavan tekstin kirjoittamisessa, joka kuvastaa brändiä ja on yhdenmukainen koko tuotelinjan kanssa. Aloita luomalla ehdotus ja muuta ehdotettua tekstiä tarpeen mukaan.

### Käytettävissä olevat kielet

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### Vaatimukset

Markkinointitekstiehdotustoiminto on aktivoitu ympäristössä. Tämän toiminnon tekee tavallisesti ylläpitäjä. Lisätietoja on kohdassa [Määritä Copilot ja tekoälyominaisuudet](enable-ai.md).

### Luo ensimmäinen luonnos Copilotin avulla

Lisää aiemmin luotuun nimikkeeseen markkinointitekstiä noudattamalla seuraavia vaiheita. Saat lisätietoja uuden nimikkeen luomisesta valitsemalla [Rekisteröi uudet nimikkeet](inventory-how-register-new-items.md).

1. Avaa Business Centralissa nimike, jota haluat muokata suorittamalla seuraavat vaiheet:

   - Valitse oikeasta yläkulmasta ![Lamppu, joka avaa kerro minulle -ominaisuuden 22.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"). -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki, joka näyttää saatavilla olevat nimikkeet.

   - Kaksoisnapsauta nimikettä tai valitse sen arvo kohdassa **Nro**-sarakkeessa .

1. Nimikkeen kortissa on kaksi tapaa, joilla voit aloittaa markkinointitekstin kirjoittamisen avustajan avulla: **Markkinointiteksti**-tietoruudusta tai käyttämällä **Markkinointiteksti**-toimintoa. Nämä menetelmät esitetään seuraavassa nimikekortin kaaviossa.  

   [![Näyttää nimikkeen kortin, jossa on markkinointitekstiruutu](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Voit luoda nimikkeen ensimmäisen luonnoksen tekemällä jonkin seuraavista vaiheista:

   - Valitse **Teee luonnos Copilotin avulla** sivun oikeassa reunassa olevan tietoruudun **markkinointiteksti**-ruudussa. 

     Copilot aloittaa markkinointitekstin laatimisen.

   - Valitse sivun yläosassa **Markkinointiteksti**-toiminto ja valitse **Muokkaa markkinointitekstiä** -ikkunassa **Tee luonnos Copilotin avulla**.  Näyttöön tulee **Tee luonnos markkinointitekstistä Copilotin avulla** -ikkuna ja se sisältää nimikkeen kaikki käytettävissä olevat määritteet.
1. Valitse määritteet, joille haluat Copilotin perusehdotuksia, ja valitse sitten **Luo**. Voit muuttaa valittuja määritteitä ja muita vaihtoehtoja myöhemmin. Copilot aloittaa markkinointitekstin laatimisen. 

   ![Näyttää muokkaa markkinointitekstiä -ikkuna](media/marketing-text-copilot-attributes.svg)

1. Kun Copilot on saanut luonnoksen valmiiksi, teksti näkyy Copilot-editorin ikkunassa tarkistettavaksi ja muokattavaksi.

   [![Näyttää Luo Copilotilla -ikkunat](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Voit nyt saada lisää ehdotuksia, yrittää parantaa saamiasi ehdotuksia, muokata tekstiä, ja enemmän. Siirry [Tarkista, Muokkaa ja Tallenna](#review-edit-and-save-text) -kohtaan lisätietoja varten.

### Tarkista, muokkaa ja tallenna teksti

Kun olet saanut ensimmäisen luonnoksen, sinun täytyy tarkistaa se ja tehdä tekstiin muutoksia, jotta saat sen valmiiksi julkaistavaksi. Tämä työ tehdään Copilot-editorilla, jonka avulla voit saada lisää ehdotuksia, muuttaa asetuksia vaikuttaaksesi ehdotuksiin ja manuaalisesti tehdä muutoksia ja muokata tekstiä.

> [!IMPORTANT]
> Tekoälyn Copilotissa luoma teksti on vain ehdotus, ja siinä voi olla virheitä. Se edellyttää ihmisen valvontaa ja tarkistuksen sen varmistamiseksi, että se on tarkka ja asianmukainen. Tarkastele ehdotettua tekstiä ja muokkaa sitä tarpeen mukaan, ennen kuin tallennat ja julkaiset sen julkista käyttöä varten.

Viimeistele ja tallenna markkinointiteksti seuraavien ohjeiden avulla.

1. Tee muutokset tekstiin suoraan teksti-ruudussa. Käytä ruudun alaosassa olevaa työkalupalkkia, kun haluat muotoilla ja tyylitellä tekstiä, lisätä linkkejä ja paljon muuta.
2. Saat uuden ehdotuksen valitsemalla **Luo uudelleen**.
3. Jos et ole tyytyväinen ehdotuksiin, tehosta tekstiehdotuksia **Sävy**-, **muoto**- ja **painotus**-valinta-asetusten avulla.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Ohjeita ehdotusten parantamisesta on kohdassa [Paranna ja räätälöi tekstiehdotuksia](#improve-and-tailor-text-suggestions).

4. Voit siirtyä ehdotuksissa edestakaisin käyttämällä sivun yläreunassa olevia edellinen ja seuraava -linkkejä (*x* **/** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Tarkasta tekstin oikeus ja tarkoituksenmukaisuus huolellisesti:

   - Jos haluat tallentaa tekstin, valitse **Säilytä se**. 
   - Jos et halua tallentaa, valitse hylkää-painike (roska-astia) ![Näyttää roska-astiakuvakkeen kaikkien pankkitilin täsmäytystä koskevien Copilot-ehdotusten poistamiseksi](media/copilot-delete-trash-can.png).

### Tekstiehdotusten parantaminen ja mukauttaminen

Voit parantaa tekstiehdotuksia ja nipistää niitä henkilökohtaisten tai yrityksen mieltymysten mukaisiksi muutamalla toimenpiteellä.

1. Muuta Copilotin käyttämiä nimikkeen määritteitä.

   Copilotin ehdotukset perustuvat osittain nimikkeelle määritellylle määritteelle. Jos haluat tarkastella käytettävissä olevia määritteitä ja nykyisiä asetuksia, valitse muokkaa ![Näyttää muokkauskuvakkeen Copilot-ikkunassa, kun haluat muuttaa määritteitä](media/edit-pencil.png) -kuvake vasemmassa yläkulmassa. Valitse **Nimikemääritteet**-sivulla määritteet, jotka parhaiten kohdistetaan niiden ominaisuuksien mukaan, joita haluat edistää. Mitä enemmän osuvia määritteitä sisällytät, sitä monipuolisempi tulos on. Jos sinusta tuntuu, että sinulta puuttuu joitakin avainmääritteitä, lisää niitä. Lisätietoja määritteistä on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)
1. Muuta **sävy**-, **muoto**- ja **painotus**-asetusten asetuksia.

   |Asetus|Kuvaus|
   |-|-|
   |Sävy |Käytä tätä vaihtoehtoa, kun haluat vaikuttaa siihen, millaisia sanoja, lauseita ja välimerkkejä käytetään kohdeyleisön sitouttamiseksi. Voit valita useista esimääritetyistä äänensävyistä, jotka vaihtelevat **muodollisista** (mikä vaikuttaa liiketoiminnan sävyyn) **luovaan** (mikä johtaa epäviralliseen sävyyn). |
   |Muoto ja pituus|Käytä tätä vaihtoehtoa, kun haluat hallita tekstin yleistä rakennetta, joka koostuu kolmesta osasta, jotka kattavat neljä eri vaihtoehtoa: <ul><li>**Tunnisterivi** - tarttuva lause tai lyhyt lause, joka yksilöi nimikkeen tai brändin.</li><li>**Kappale** - yhden kappaleen sujuva ja sanallinen teksti, joka koostuu useista kokonaisista lauseista.</li><li>**Tunnisterivi + kappale** - tunnisterivi ja sitä seuraava kappale</li><li>**Johdanto** - johdantolause, joka muistuttaa tunnuslausetta, ja sen jälkeen luettelo keskeisistä kiinnostavista kohdista.</li></ul> |
   |Korostus|Valitse tämän asetuksen avulla luettelo niistä esimääritetyistä ominaisuuksista, joita haluat korostaa tekstissä. Valitse laatu, joka vastaa parhaiten sen tyyppistä nimikettä, josta kirjoitat. Ominaisuudet eivät vastaa suoraan nimikkeen määritteitä, kuvausta tai luokkaa. Esimerkiksi **laatu** voisi olla hyvä valinta sekä pyörälle että työpöydälle, kun taas **Nopeus** sopisi pyörään, mutta ei työpöytään.|

1. Paranna nimikekortin **Kuvaus**-kenttää.

   **Kuvaus**-kentän tekstiä käytetään muodossa, joka on sellaisenaan useassa kohdassa ehdotetussa tekstissä, joten on tärkeää, että kuvaus kuvaa parhaiten, miten haluat nimikkeeseen viitattavan markkinointitekstissä. 

1. Varmista, että nimikekortin **Nimikekategorian koodi** -kenttään on asetettu oikea luokka.

   Copilot etsii luokkaan liittyviä sanoja ja lauseita ja työstää niitä ehdotettuun tekstiin.

### Monikielinen työskentely 

Teksti luodaan aina käyttäjän [asetuksissasi](ui-change-basic-settings.md#language) määritetyllä kielellä. Jos organisaatiosi toimii ja syöttää tietoja Business Centraliin eri kielellä tai jos Business Central on yhdistetty verkkokauppaasi, kuten  Shopifyhin, tämä saattaa johtaa sisällön julkaisemiseen, joka ei vastaa samanlaista markkinointisisältöä. .

## Luo teksti tyhjästä

1. Avaa Business Centralissa nimike, jota haluat muokata seuraavalla tavalla:

    1. Valitse oikeasta yläkulmasta ![Lamppu, joka avaa kerro minulle -ominaisuuden 22.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"). -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki, joka näyttää saatavilla olevat nimikkeet.
    2. Voit avata nimikkeen kaksoisnapsauttamalla sitä tai valitsemalla sen numeron **Nro**-kentässä .

2. Tee jompikumpi seuraavista:

   - Valitse **Muokkaa** sivun oikeassa reunassa olevan tietoruudun **markkinointiteksti**-ruudussa.
   - Valitse **Markkinointiteksti**-toiminto.
3. Tee muutokset tekstiin suoraan **markkinointiteksti**-ruudussa. Käytä ruudun alaosassa olevaa työkalupalkkia, kun haluat muotoilla ja tyylitellä tekstiä, lisätä linkkejä ja paljon muuta.
4. Valitse **OK**, kun olet valmis tallentamaan tekstin.

## Katso myös

[Markkinointitekstiehdotusten yleiskatsaus](ai-overview.md)  
[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
[Markkinointitekstiehdotusten usein kysytyt kysymykset](faqs-marketing-text.md)  
[Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
