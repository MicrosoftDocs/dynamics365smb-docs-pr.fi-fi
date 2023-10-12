---
title: Contoso Coffeen tuotannon esittely
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin tuotanto-ominaisuuksia.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4765
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a>Contoso Coffeen tuotannon esittely

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään tuotanto-ominaisuuksia Business Centralissa.  

Sovellus sisältää neljä tuotetta, jotka on optimoitu eri skenaarioita varten:

- **SP-SCM1009 Airpot**  

  Tämä tuote on tuoterakenne, jossa on alikokoonpano **Reititys**. Käytä sitä vakiotuotantovirtojen osoittamiseen. Siihen on määritetty vaihtoehtoisia reitityksiä, joita voidaan käyttää osoittamaan eri skenaarioita, joihin liittyy alihankkijoita. Arvostusmenetelmä on *Vakio*.  

- **SP-SCM1011 Airpot Duo**  

  Tämä tuote edellyttää nimikeseurantaa, ja siinä on komponentti, joka edellyttää myös nimikeseurantaa. Arvostusmenetelmä on *Määrätty*.  

- **SP-SCM1004 Autodrip**  

  Tämä tuote on tuoterakenne, jossa on alikokoonpano **Reititys**. On suositeltavaa osoittaa sen avulla eri materiaalin ottotavat sekä komponenteille että operaatioille. Arvostusmenetelmä on *Vakio*.

- **SP-SCM1006 AutoDripLite**

  Tällä tuotteella on kolme eri varianttia ja kolme tuoterakennetta, jotka voidaan liittää varastointiyksiköihin. Tuote käyttää haamutuoterakenteen käsitettä. Arvostusmenetelmä on *Vakio*.

Kaikkien skenaarioiden tuotanto toiminnot käyttävät sijaintia *MAIN*.  

> [!IMPORTANT]
> Ennen kuin suoritat mitään Contoso Coffeen skenaarioista, kirjaa kaikki nimikepäiväkirja rivit, joilla on alkusaldot. Lisätietoja vaatimuksista on [Contoso Coffee -tietojen määrittäminen](#set-up-contoso-coffee-manufacturing-data) -osiossa.

## <a name="set-up-contoso-coffee-manufacturing-data"></a>Contoso Coffeen tuotantotietojen määrittäminen

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

|Kenttä  |Kuvaus  |
|---------|---------|
|**Tuotantosijainti** |Määrittää varaston, jota haluat käyttää tuotantotoiminnoissa. Oletus arvo on *MAIN*, mutta sitä voi muuttaa tarpeidesi mukaan.|


Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

## <a name="scenarios"></a>Esimerkkitilanteet

Contoso Coffeen tuotannon esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoitteluskenaarioita:

1. [Uuden tuotannon tuoterakenteen ja tuoterakenneversion luominen](create-new-production-bom-version.md)  
2. [Uuden reitityksen luominen](create-new-routing.md)  
3. [Sitovasti suunnitellun tuotantotilauksen luominen ja muuttaminen](create-firm-planned-production-order-change.md)  
4. [Yhdistä automaattinen ja manuaalinen materiaalinotto](combine-automatic-manual-flushing.md)  
5. [Käytä tilauksen suunnittelua tarjonnan luomiseksi ja varaamiseksi](order-planning-create-reserve-supply.md)  
6. [Alihankintatoiminnon määrittäminen ja käsitteleminen](set-up-process-subcontracting-operation.md)  
7. [Määritä uusi kapasiteetti](set-up-new-capacity.md)  
8. [Nimikevarianttien, joille on määritetty eri tuoterakenteet, kysyntäennuste](variants.md)  

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

> [!IMPORTANT]
> Nämä vaihekuvaukset edellyttävät, että käyttäjäkokemukseksi on asetettu *Premium* **Yritystiedot**-sivulla.

## <a name="see-also"></a>Katso myös

[Tuotanto](../../production-manage-manufacturing.md)  
[Business Centralin tuotantoraportit ja analytiikka](../../production-reports.md)  
