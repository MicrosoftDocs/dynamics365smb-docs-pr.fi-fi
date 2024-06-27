---
title: Pankkitilien täsmäyttäminen Copilotin avulla (esiversio)
description: 'Tietoja siitä, miten pankkitilit täsmäytetään Copilotin avulla Business Centralissa.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# Pankkitilien täsmäyttäminen Copilotin avulla (esiversio)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Tässä artikkelissa kerrotaan, miten pankkitilin täsmäytysavustaja auttaa pankkitapahtumien täsmäytyksessä Microsoft Dynamics 365 Business Centralin tapahtumien kanssa.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Tietoja pankkitilin täsmäytysavustajasta

Pankkitilin täsmäytysavustaja on joukko tekoälyä käyttäviä ominaisuuksia, jotka auttavat pankkitilien täsmäytyksessä. Se tarjoaa Copilotin avulla kaksi erillistä tehtävää:

- Tapahtumien ja kirjanpitotietojen yhteensovittamisen parantaminen

    Kuten ehkä jo tiedät, **Täsmäytä automaattisesti** -painike **Pankkitilin täsmäytys** -sivulla yhdistää automaattisesti useimmat pankkitapahtumat kirjapitomerkintöihin. Operaatiota kutsutaan *automaattiseksi täsmäytykseksi*. Vaikka automaattinen täsmäytys toimii hyvin, sen käyttämät algoritmit voivat joskus johtaa moniin täsmäyttämättömiin tapahtumiin. Copilot käyttää tekoälyteknologiaa, kun halutaan tarkastaa täsmäyttämättömät tapahtumat ja tunnistaa useampia vastaavuuksia päivämäärien, summien ja kuvausten perusteella. Jos asiakas esimerkiksi maksoi useita laskuja yhtenä kertakorvauksena, Copilot täsmäyttää yksittäisen tiliotteen rivin useiden laskutapahtumien kanssa.

    [Lisätietoja tästä tehtävästä](#reconcile-bank-accounts-with-copilot).

- Ehdotetut pääkirjanpitotilit (KP)

    Jäljellä olevien pankkitapahtumien osalta, joita ei voida yhdistää mihinkään kirjanpitoon, Copilot vertaa tapahtumakuvausta KP-tilien nimiin ja ehdottaa sitten todennäköisintä KP-tiliä, jolle kirjataan. Jos esimerkiksi täsmäyttämättömillä tapahtumilla on *Bensa-asema 24* -narratiivi Copilot saattaa ehdottaa, että ne kirjataan *Kuljetus*-tilille.

    [Lisätietoja tästä tehtävästä](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## Käytettävissä olevat kielet

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## Vaatimukset

- Pankkitilin täsmäytysavustaja on aktivoitu. Järjestelmänvalvojan on suoritettava tämä tehtävä. [Lisätietoja Copilotin ja tekoälyn ominaisuuksien määrittämisestä](enable-ai.md).
- Business Centralin pankkitilit, jotka haluat täsmäyttää, on linkitetty online-pankkitiliin tai ne on määritetty pankin tiliotteen tuontimuodon avulla.
- Pankkitilien täsmäytys Business Centralissa on sinulle tuttua, kuten kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md) on kuvattu.

## Pankkitilien täsmäyttäminen Copilotin avulla

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot pankkitilin täsmäytyksessä on tarkoitettu käytettäväksi automatisoinnin täydennyksenä. Siksi, kun käytät Copilotia, automaattinen vastaavuustoiminto suorittaa ensin alkuperäiset vastaavuudet. Sen jälkeen Copilot yrittää täsmäyttää sellaisten tapahtumien kanssa, joita automaattinen täsmäytystoiminto ei käsitellyt.

Pankkitilien täsmäytykseen Copilotin avulla on olemassa kaksi tapaa:

- Copilotin käyttäminen uuden täsmäytyksen aloittamiseksi pankkitilillä, suoraan **Pankkitilin täsmäytys** -luettelosta.
- Copilotin käytön käyttäminen uudessa tai aiemmin luodussa täsmäytyksessä **Pankkitilin täsmäytys** -kortilla.

# [Pankkitilin täsmäytysluettelosta](#tab/fromlist)

Tämän lähestymistavan avulla luodaan ja täsmäytetään uusi pankkitilin täsmäytys alusta. Tämä lähestymistapa edellyttää pankkitilin valintaa. Jos valittua pankkitiliä ei ole linkitetty verkkopankkitiliin, sinun on myös tuotava tiliotetiedosto.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytykset** ja valitse sitten vastaava linkki.
1. Avaa **Täsmäytä Copilotin avulla** valitsemalla **Täsmäytä Copilotin avulla** -ikkuna.
1. Määritä **Suorita tämän pankkitilin täsmäytys** -kenttä sille pankkitilille, jonka haluat täsmäyttää.

    ![Näyttökuva, joka näyttää Täsmäytä Copilotin avulla -ikkunan, jossa täsmäytys tehdään alusta alkaen.](media/reconcile-bank-accounts-new-copilot.svg)

1. Jos valittua pankkitiliä ei ole linkitetty verkkopankkitiliin, sinun on tuotava tiliotetiedosto. Voit tuoda tiedoston valitsemalla arvon **Käytä tapahtumatietoja** -kentästä tai valitsemalla paperiliitin-painikkeen **Luo**-painikkeen vieressä. Käytä sitten **Valitse tuotava tiedosto** -komentoa tuodaksesi tiliotetiedoston joko vetämällä se laitteeltasi tai selaamalla laitettasi.
1. Voit täsmäyttää Copilotin avulla valitsemalla **Luo**.

    Copilot alkaa tuottaa ehdotettuja osumia. Kun se on valmis, **Täsmäytä Copilotin avulla** -ikkuna näyttää täsmäytysprosessin tulokset.

1. Tarkista ehdotetut täsmäytykset seuraavassa osiossa kuvatulla tavalla.

# [Pankkitilin täsmäytyksen kortista](#tab/fromcard)

Tämän lähestymistavan avulla voit käyttää Copilot-toimintoa joko uudessa pankkitilin täsmäytyksessä, jonka luot manuaalisesti, tai muokkaamalla aiemmin luotua täsmäytystä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytykset** ja valitse sitten vastaava linkki.
1. Noudata seuraavia ohjeita:

    - Aloita uusi täsmäytys valitsemalla **Uusi** .
    - Valitse ja avaa aiemmin luotu täsmäytys luettelosta.

1. Valitse **Pankkitilin täsmäytys** -kortissa **Täsmäytä Copilotin avulla**.

    ![Näyttökuva, joka näyttää täsmäytyksen Copilot-painikkeen avulla Pankkitilin täsmäytys -kortilla.](media/bank-reconciliation-copilot-card.svg)

    Copilot alkaa tuottaa ehdotettuja osumia. Kun se on valmis, **Täsmäytä Copilotin avulla** -ikkuna näyttää täsmäytysprosessin tulokset.

1. Tarkista ehdotetut täsmäytykset seuraavassa osiossa kuvatulla tavalla.
---

### Ehdotettujen osumien tarkistaminen, tallentaminen ja hylkääminen

Copilotin suorittamisen jälkeen **Täsmäytä Copilotin avulla** -ikkunassa näkyvät eritellyt tulokset sekä ehdotetut osumat. Tässä vaiheessa Copilotin ehdottamaa vastaavuutta ei ole tallennettu. Sen vuoksi sinulla on mahdollisuus tarkastaa ehdotukset ja tallentaa tai hylätä ne haluamallasi tavalla.

![Näyttökuva, joka näyttää Täsmäytä Copilotin avulla -ikkunan ehdotetut vastaavuudet.](media/bank-reconciliation-copilot-window.png)

**Täsmäytä Copilotin avulla** -ikkuna on jaettu kahteen osaan. Ylemmässä osiossa on yleistietoja lopputuloksesta. Alemmassa osassa **Vastaavuusehdotus**, on luettelo Copilotin ehdottamista osumista.

Seuraavassa taulukossa kuvataan ylemmän osan kentät.

| Kenttä | Kuvaus |
|---|---|
| Kohdistettu automaattisesti | Tiliotteen rivien määrä, jota automaattinen täsmäytystoiminto vastaa. Valitse arvo, jota haluat tarkastella täsmäytyskortissa. |
| Copilotin kohdistamat | Niiden pankin tiliotteen rivien määrä, joille Copilot ehdotti vastaavuuksia. Täsmäytysten yksityiskohdat voi nähdä **Täsmäytä ehdotuksia** -osassa. |
| Tiliotteen loppusaldo | Loppusaldo, joka näytetään pankin tiliotteessa, jota täsmäytät. |
| Kirjaa, jos kohdistettu kokonaan | Ota tämä valinta käyttöön, jos haluat kirjata pankkitilin täsmäytyksen automaattisesti, kun kaikki rivit (100 %) täsmäävät ja olet valinnut **Säilytä**. |

Tarkista ehdotetut vastaavuudet rivi riviltä **Vastaavuudet**-kohdassa. Ryhdy sitten asianmukaisiin toimiin:

- Jos haluat hylätä yksittäisen ehdotetun vastaavuuden, valitse se luettelosta ja valitse **poista rivi**.
- Hylkää kaikki ehdotetut vastaavuudet ja sulje **Täsmäytä Copilotin avulla** -ikkuna valitsemalla hylkäyspainike (roskakori) ![Hylkää-painike.](media/copilot-delete-trash-can.png) ikkunan alareunassa olevan **Säilytä se** -painikkeen vieressä.
- Jos haluat kirjata täydellisen täsmäytyksen automaattisesti, kun tallennat sen, ota käyttöön **Lähetä, jos se on täysin käytössä** -valinnan.
- Tallenna **Täsmäytä Copilotin avulla** -ikkunassa tällä hetkellä näkyvät vastaavuudet valitsemalla **Säilytä se**.

## Julkaise täsmäyttämättömät pankkitilitapahtumamäärät ehdotetuille kirjanpitotileille

Tämä osio selittää, miten Copilotia käytetään täsmäyttämättömien pankkitilin tiliotteen rivien kirjaamiseen (kuten määritetty **Ero**-kentässä) pääkirjanpitotilille. Tämän tehtävän voi tehdä vain olemassa olevasta täsmäytyksestä.

1. Siirry **Pankkitilin täsmäytykset** -luetteloon ja avaa täsmäytys, joka sisältää täsmäyttämättömät rivit.

    Tämä vaihe antaa selkeän kuvan kaikista täsmäyttämättömistä pankin tiliotteen riveistä, jotka tulee siirtää pääkirjanpidon tilille.

1. Määritä **Pankin tiliotteen rivit** -ruudussa vastaamattomat pankin tiliotteen rivit ja valitse vähintään yksi rivi, jonka haluat täsmäyttää.

    Copilot keskittyy valittuihin riveihin, kun halutaan kirjata uusia maksuja KP-tilille.

1. Aloita prosessi valitsemalla **Kirjaa ero KP-tilille**.

    ![Näyttökuva, jossa näkyy Pankkitilin täsmäytyskortin Kirjaa ero KP-tiliin -painike.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot aloittaa uusien maksujen kirjaamisehdotusten luomisen.

1. Kun Copilot on saanut ehdotukset valmiiksi, **Copilotin ehdotukset erojen kirjaamiseksi KP-tileille** -ikkuna tulee näkyviin.

    **Vastaavat ehdotukset** -osa tässä ikkunassa näyttää ehdotukset. Kokemus muistuttaa kokemusta täsmäytyksestä Copilotin kanssa.

    ![Näyttökuva, jossa näkyy KP-tileihin eroavuuksien kirjaamiseksi esitettyjä Copilot-ehdotuksia.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Tarkista ehdotukset rivi riviltä ehdotettujen kirjattavien maksujen oikeellisuuden varmistamiseksi.

    - Jos poraudut ehdotukseen valitsemalla sen luettelosta, sinut viedään tililuetteloon. Tässä voit valita toisen tilin. Voit tehdä tällaisen manuaalisen korjauksen vain, kun käytät **Eron kirjaaminen KP-tiliin** -työnkulkua, ei vastaavassa työnkulussa.
    - Jos valitset ehdotuksen vieressä **Tallenna**, voit lisätä linkitysviestin **Teksti tiliin -linkitys** -sivulle. Seuraavan kerran, kun tämä teksti näkyy täsmäytyksen aikana, se linkitetään ehdotettuun tiliin.

1. Hylkää tai tallenna ehdotukset.

    - Hylätäksesi tietyn ehdotuksen, valitse se luettelosta ja valitse **Poista rivi**. Jos haluat hylätä kaikki ehdotukset ja sulkea Copilotin, valitse Hylkää-painike (roska-astia) ![Hylkää-painike.](media/copilot-delete-trash-can.png) ikkunan alareunassa olevan **Säilytä se** -painikkeen vieressä.
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
