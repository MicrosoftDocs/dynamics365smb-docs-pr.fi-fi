---
title: Contoso Coffeen esittely
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin varastointiominaisuuksia.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Contoso Coffeen fyysisen varastoinnin esittely

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään varastointiominaisuuksia Business Centralissa. Voit määrittää fyysisen varastoinnin ominaisuuksia monella eri tavalla, katso [Yleiskuvaus erilaisista määritysvaihtoehdoista](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Sovellus sisältää kolme sijaintia, jotka on optimoitu eri skenaarioita varten:

- **HOPEINEN**  

  Tämä sijainti on määritetty käyttämään varastopaikkoja. Se voidaan helposti määrittää tukemaan perus- tai lisätietoja. 

- **KELTAINEN**  

  Tässä sijainnissa käytetään varastoinnin lisäkonfiguraatiota, mutta se ei käytä varastopaikkoja. Se voidaan määrittää uudelleen tukemaan perusmäärityksiä.

- **VALKOINEN**  

  Tässä sijainnissa käytetään kehittynyttä fyysisen varastoinnin konfiguraatiota, jossa on ohjatut hyllytykset ja poiminnat, joiden avulla nimikkeet liikkuvat koko fyysisessä varastossa.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Contoso Coffeen varastointitietojen määrittäminen

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Kun asianmukaiset sovellukset on asennettu, siirry [Contoson demotyökalu](https://businesscentral.dynamics.com/?page=5194) -sivulle kohteessa [!INCLUDE [prod_short](../../includes/prod_short.md)], valitse *Varastomoduuli*-rivi ja valmistele moduulit käyttämällä **Määritä**-toimintoa. Asetukset kuvaillaan seuraavissa taulukoissa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Sijainti Varastopaikka**  |Sijainti, jota käytetään perussijaintiskenaarioissa.|
|**Sijainnin lisäasetukset**  |Sijainti, jota käytetään logistiikan perusskenaarioissa.|
|**Sijaintiohjattu hyllytys ja poiminta**  |Sijainti, jota käytetään logistiikan lisäskenaarioissa.|
|**Sijainti Kuljetuksessa**  |Siirtoskenaarioiden kuljetuksessa-sijainnissa käytettävä sijainti.|
|**Asiakasnro**  |Asiakas, jota käytetään myyntitoimintojen perusskenaarioissa ja yksinkertaisissa skenaarioissa.|
|**Toimittajanro**  |Toimittaja, jota käytetään kaikissa ostotoimintojen skenaarioissa.|
|**Nimikkeen 1 nro**  |Kaikissa skenaarioissa käytettävä päänimike.|
|**Nimikkeen 2 nro**  |Kaikissa skenaarioissa käytettävä lisänimike.|
|**Nimikkeen 3 nro**  |Nimike, jolla on seuranta.|

Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

> [!IMPORTANT]
> Jos käytät skenaarioita, haluat ehkä varmistaa, että käyttäjä on lisätty valittujen sijaintien osalta. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Esimerkkitilanteet

Contoso Coffeen varastoinnin esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoitteluskenaarioita:

1.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen varaston perusmäärityksissä](warehouse-basic-flow-putaway-pick.md)
2.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen sekavaraston perusmäärityksissä](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku edistyneessä fyysisen varaston määrityksessä, jossa on ohjattu hyllytys ja poiminta](warehouse-directed-flow.md)

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

## <a name="see-also"></a>Katso myös

[Varaston määrittäminen](../../inventory-setup-inventory.md) 
[Tietoja sijaintien määrittämisestä](../../inventory-how-setup-locations.md) 
[Varastointi](../../warehouse-manage-warehouse.md) 
[Suunnittelutiedot](../../design-details-warehouse-overview.md) 
