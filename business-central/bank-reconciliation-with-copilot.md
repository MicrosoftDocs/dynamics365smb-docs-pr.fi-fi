---
title: Pankkitilien täsmäyttäminen täsmäytysavustajan avulla
description: 'Tietoja siitä, miten pankkitilit täsmäytetään Copilotin avulla Business Centralissa.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/15/2024
ms.custom: bap-template
---

# Pankkitilien täsmäyttäminen Copilotin avulla (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Tässä artikkelissa kerrotaan, miten pankkitilin täsmäytysavustaja auttaa pankkitapahtumien täsmäytyksessä Business Centralin tapahtumien kanssa.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Tietoja pankkitilin täsmäytysavustajasta

Pankkitilin täsmäytysavustaja on joukko tekoälyä käyttäviä ominaisuuksia, jotka auttavat pankkitilien täsmäytyksessä. Pankkitilin täsmäytysavustaja tarjoaa kaksi erillistä tehtävää Copilotin kautta:

- Tapahtumien ja kirjanpitotietojen yhteensovittamisen parantaminen

   Saatat jo tuntea **Täsmäytä automaattisesti** -toiminnon **Pankkitilin täsmäytys** -sivulla, joka yhdistää automaattisesti useimmat pankkitapahtumat kirjapitomerkintöihin. Operaatiota kutsutaan *automaattiseksi täsmäytykseksi*. Vaikka automaattinen täsmäytys toimii hyvin, sen käyttämät algoritmit voivat joskus johtaa moniin täsmäyttämättömiin tapahtumiin. Copilot käyttää tekoälyteknologiaa, kun halutaan tarkastaa jäljellä olevat tapahtumat ja tunnistaa useampia vastaavuuksia päivämäärien, summien ja kuvausten perusteella. Jos asiakas esimerkiksi maksoi useita laskuja yhtenä kertakorvauksena, Copilot täsmäyttää yksittäisen tiliotteen rivin useiden laskutapahtumien kanssa.

   Siirry kohtaan [Täsmäytä pankkitilit Copilotin avulla](#reconcile-bank-accounts-with-copilot).

- Ehdotetut pääkirjanpitotilit

  Jäljellä olevien pankkitapahtumien osalta, joita ei voida yhdistää mihinkään kirjanpitoon, Copilot vertaa tapahtumakuvausta KP-tilien nimiin ja ehdottaa todennäköisimpää KP-tiliä, jolle kirjataan. Copilot voi esimerkiksi ehdottaa, että narratiivisen "Bensa-asema 24" -tapahtuman tapahtumat kirjataan Kuljetus-tilille.
  
   Siirry kohtaan [Julkaise täsmäyttämättömät pankkitilitapahtumamäärät ehdotetuille kirjanpitotileille](#post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts).

## Vaatimukset

- Pankkitilin täsmäytysavustaja on aktivoitu. Järjestelmänvalvoja tekee tämän tehtävän. [Lisätietoja Copilotin ja tekoälyn ominaisuuksien määrittämisestä](enable-ai.md).
- Business Centralin pankkitilit, jotka haluat täsmäyttää, on linkitetty online-pankkitiliin tai ne on määritetty pankin tiliotteen tuontimuodon avulla. 
- Pankkitilien täsmäytys Business Centralissa on sinulle tuttua, kuten kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md) on kuvattu. 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## Täsmäytä pankkitilit Copilotin avulla

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot pankkitilin täsmäytyksessä on tarkoitettu käytettäväksi automatisoinnin täydennyksenä. Tästä syystä, kun käytät Copilotia, automaattinen vastaavuustoiminto suorittaa ensin alkuperäiset vastaavuudet. Sen jälkeen Copilot yrittää täsmäyttää sellaisten tapahtumien kanssa, joita automaattinen täsmäytystoiminto ei käsitellyt.   

Pankkitilien täsmäytykseen Copilotin avulla on olemassa kaksi tapaa. Copilotin avulla voit aloittaa uuden täsmäytyksen pankkitililtä, suoraan **Pankkitilin täsmäytys** -luettelosta, tai voit käyttää Copilotia uudessa tai olemassa olevassa täsmäytyksessä **Pankkitilin täsmäytys** -kortilla.

# [Pankkitilin täsmäytysluettelosta](#tab/fromlist) 

Tämän lähestymistavan avulla luodaan ja täsmäytetään uusi pankkitilin täsmäytys alusta. Tämä lähestymistapa edellyttää, että valitset pankkitilin ja tuot pankin tiliotetiedoston, jos pankkitiliä ei ole linkitetty online-tiliin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytykset** ja valitse sitten vastaava linkki. 
1. Avaa **Täsmäytä Copilotin avulla** -ikkuna valitsemalla **Täsmäytä Copilotin avulla** -toiminto.
1. Määritä **Suorita tämän pankkitilin täsmäytys** -kenttä sille pankkitilille, jonka haluat täsmäyttää.

   ![Näyttää täsmäytä Copilotin avulla -ikkunan, jossa täsmäytys tehdään alusta alkaen](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Jos valittua pankkitiliä ei ole linkitetty verkkopankkitiliin, sinun on tuotava tiliotetiedosto. Voit tuoda tiedoston valitsemalla arvon **Käytä tapahtumatietoja** -kentästä tai valitsemalla paperiliitin-painikkeen **Luo**-painikkeen vieressä. Käytä sitten **Valitse tuotava tiedosto** -komentoa tuodaksesi tiliotetiedoston joko vetämällä se laitteeltasi tai selaamalla laitettasi.
1. Voit täsmäyttää Copilotin avulla valitsemalla **Luo**.

   Copilot alkaa tuottaa ehdotettuja osumia. Kun se on valmis, Täsmäytä Copilotin avulla -ikkuna avaa täsmäytysprosessin tulokset.

1. Tarkista ehdotetut täsmäytykset seuraavassa osiossa kuvatulla tavalla.

# [Pankkitilin täsmäytyksen kortista](#tab/fromcard) 

Tämän lähestymistavan avulla voit käyttää Copilot-toimintoa joko uudessa pankkitilin täsmäytyksessä, jonka luot manuaalisesti, tai muokkaamalla aiemmin luotua täsmäytystä. 


1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytykset** ja valitse sitten vastaava linkki. 
1. Tee jompikumpi seuraavista:

   - Aloita uusi täsmäytys valitsemalla **Uusi** . 
   - Valitse ja avaa aiemmin luotu täsmäytys luettelosta.
1. Valitse **Pankkitilin täsmäytys** -kortissa **Täsmäytä Copilotin avulla**

   ![Näyttää täsmäytyksen Copilot-toiminnon avulla Pankkitilin täsmäytys -kortilla](media/bank-reconciliation-copilot-card.svg) 

   Copilot alkaa tuottaa ehdotettuja osumia. Kun se on valmis, **Täsmäytä Copilotin avulla** -ikkuna avaa täsmäytysprosessin tulokset. 

1. Tarkista ehdotetut täsmäytykset seuraavassa osiossa kuvatulla tavalla. 
---

### Ehdotettujen osumien tarkistaminen, tallentaminen ja hylkääminen

Copilotin suorittamisen jälkeen **Täsmäytä Copilotin avulla** -ikkunassa näkyvät eritellyt tulokset sekä ehdotetut osumat. Tällöin Copilotin ehdottamia vastaavuuksia ei ole tallennettu, joten sen avulla voit tarkastaa ehdotukset ja tallentaa tai hylätä haluamasi tiedot.

![Näyttää täsmäytä Copilotin avulla -ikkunan ja ehdotetut vastaavuudet](media/bank-reconciliation-copilot-window.png) 

Copilot-ikkuna on jaettu seuraaviin kahteen osaan. Ylemmässä osiossa on yleistietoja lopputuloksesta, kuten seuraavassa taulukossa kuvataan.  Alemmassa **Vastaavuusehdotus**-osassa on luettelo Copilotin ehdottamista osumista.

|Kenttä|Kuvaus|
|-|-|
|Kohdistettu automaattisesti|Määrittää, kuinka monta tiliotteen riviä automaattinen täsmäytystoiminto vastaa. Valitse arvo, jota haluat tarkastella täsmäytyskortissa.  |
|Copilotin kohdistamat|Määrittää, kuinka monella tiliotteen rivillä on Copilotin ehdottamia täsmäytyksiä. Täsmäytysten yksityiskohdat voi nähdä **Ehdotetut täsmäytykset** -osassa.|
|Tiliotteen loppusaldo|Määrittää loppusaldon, joka näytetään pankin tiliotteessa, jota täsmäytät|
|Kirjaa, jos kohdistettu kokonaan|Ota tämä kytkin käyttöön, jos haluat kirjata pankkitilin täsmäytyksen automaattisesti, kun kaikki rivit (100 %) täsmäävät ja olet valinnut **Säilytä**.|

#### Tallenna tai hylkää ehdotetut kohdistukset

Tarkista **Täsmäytetyt ehdotukset** -osassa ehdotetut vastaavuudet rivi riviltä ja ryhdy asianmukaisiin toimiin:

- Jos haluat hylätä yksittäisen ehdotetun vastaavuuden, valitse se luettelosta ja valitse **poista rivi** -toiminto.

- Jos haluat hylätä kaikki ehdotetut osumat ja sulkea Copilot-ikkunan, valitse poista-painike (roskapönttö) ![Näytä roskapönttökuvake, jonka avulla poistetaan kaikki Copilot-ehdotukset pankkitilin täsmäytyksestä](media/copilot-delete-trash-can.png) ikkunan alareunassa olevan **Säilytä se** -painikkeen vieressä.

- Jos haluat kirjata täydellisen täsmäytyksen automaattisesti, kun tallennat sen, ota käyttöön **Lähetä, jos se on täysin käytössä** -kytkin.  
- Tallenna Copilot-ikkunassa tällä hetkellä näkyvät vastaavuudet valitsemalla **Säilytä se**.

## Julkaise täsmäyttämättömät pankkitilitapahtumamäärät ehdotetuille kirjanpitotileille

Tässä osiossa opit käyttämään Copilotia täsmäyttämättömien pankkitilin tiliotteen rivien kirjaamiseen (määritetty **Ero**-kentässä) pääkirjanpitotilille. Tämän tehtävän voi tehdä vain olemassa olevasta täsmäytyksestä.

1. Siirry **Pankkitilin täsmäytykset** -luetteloon ja avaa täsmäytys, joka sisältää täsmäyttämättömät rivit.

   Aloita avaamalla olemassa oleva pankkitilin täsmäytys. Tämä vaihe antaa selkeän kuvan kaikista täsmäyttämättömistä pankin tiliotteen riveistä, jotka tulee siirtää pääkirjanpidon tilille.

1. Määritä **Pankin tiliotteen rivit** -ruudussa vastaamattomat pankin tiliotteen rivit -ruutu ja valitse vähintään yksi rivi, jonka haluat täsmäyttää.

   Nämä ovat tiliotteen rivejä, joihin Copilot keskittyy uusien maksujen kirjaamiseen pääkirjanpidon tilille.

1. Aloita prosessi valitsemalla **Kirjaa ero KP-tilille**.

   ![Näyttää siirron KP-tilille Copilot-toiminnon avulla Pankkitilin täsmäytys -kortilla](media/bank-reconciliation-transfer-gl-copilot-card.png) 

   Tämä vaihe kehottaa Copilotia aloittamaan uusien maksujen kirjaamisehdotusten luomisen.

1. Kun Copilot on saanut ehdotukset valmiiksi, **Copilotin ehdotukset erojen kirjaamiseksi KP-tileille** -ikkuna aukeaa.

   Tässä ikkunassa näkyvät **Vastaavat ehdotukset** -osan ehdotukset. Kokemus on samanlainen kuin Copilotin kanssa täsmäytys.

   ![Näyttää siirron KP-tilille Copilotin ehdottamat vastaavuudet kanssa -sivun pankkitilin täsmäytystä varten](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

1. Tarkista jokainen ehdotus rivi riviltä ehdotettujen kirjattavien maksujen oikeellisuuden varmistamiseksi.

   - Jos poraudut ehdotukseen valitsemalla sen luettelosta, sinut viedään tililuetteloon. Tässä voit valita toisen tilin. Tällainen manuaalinen korjaus on mahdollista vain, kun käytetään **Eron kirjaaminen KP-tiliin** -työnkulkua, ei vastaavassa työnkulussa. 
   - Jos valitset **Tallenna...** ehdotuksen vieressä voidaan lisätä linkitys **Teksti tiliin -yhdistämismääritys** -sivulle, joten seuraavan kerran, kun tämä teksti näkyy sopivana, se linkitetään ehdotettuun tiliin.

1. Hylkää tai tallenna ehdotukset.

   - Jos haluat hylätä tietyn ehdotukseden, valitse se luettelosta ja valitse **Poista rivi**. Jos haluat hylätä kaikki ehdotukset ja poistua Copilotista, valitse poista-painike (roskapönttö) ![Näytä roskapönttökuvake, jonka avulla poistetaan kaikki Copilot-ehdotukset pankkitilin täsmäytyksestä](media/copilot-delete-trash-can.png) ikkunan alareunassa olevan **Säilytä se** -painikkeen vieressä.

   - Jos ehdotukset täyttävät vaatimuksesi ja haluat tallentaa ne, valitse **Säilytä se**.

      Tämä vaihe vahvistaa valittujen ehdotusten siirron pankkitilikirjauksista kirjanpitotilille. Ohjelma kirjaa uudet maksut ehdotetuille KP-tileille ja kohdistaa vastaavat rivit tuloksena syntyviin pankkitilitapahtumiin.

## Seuraavat vaiheet

[Vahvista pankkitilin täsmäytys](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## Katso myös
[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
[Vastuullisen tekoälyn usein kysyttyjä kysymyksiä pankkitäsmäytysavustajasta](faqs-bank-reconciliation.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
