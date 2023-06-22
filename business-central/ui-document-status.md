---
title: Asiakirjojen tilarivi
description: 'Lisätietoja Avoin- ja Vapautettu-tilasta tarjous-, tilaus- ja hyvityslaskuasiakirjoissa.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents" />Asiakirjojen tilarivi

Kun luodaan tarjous, tilaus tai hyvityslasku, asiakirjaotsikon **Tila**-kentässä oletustilana on **Avoin**.

Kun olet täyttänyt asiakirjan, voit vapauttaa sen, niin [!INCLUDE[prod_short](includes/prod_short.md)] muuttaa arvon kentässä **Tila** arvoksi **Vapautettu**. Tämä tila ilmaisee, että tilaus on valmis seuraavaan käsittelyvaiheeseen ennen sen kirjausta.

| Tila | Kuvaus |
| ------ | ----------- |
| Avoin   | Asiakirjaan voi tehdä muutoksia. |
| Vapautettu | Asiakirja on vapautettu seuraavaa käsittelyvaihetta varten, eikä tässä vaiheessa voida tehdä muutoksia riveille, joiden tyyppi on *Nimike* tai *Käyttöomaisuus*.<br /><br />Voit avata vapautetun asiakirjan uudelleen, jos sen sisältöä on tarpeen muuttaa. Kun haluat siirtää korjatun asiakirjan seuraavaan käsittelyvaiheeseen, vapauta asiakirja uudelleen. |
| Odottaa hyväksyntää   | Asiakirja odottaa hyväksyntää. |
| Odottaa ennakkomaksua | Asiakirjan ennakkomaksulasku on kirjattu. |

## <a name="release-process" />Julkaisukäsittely

Vapautusprosessia voidaan käyttää monella tapaa helpottamaan tavallista asiankäsittelyä ja seuraamaan yrityksen hyväksymismenettelyjä tai fyysisen varastoinnin aktiviteettien aloittamista.

### <a name="approval-procedures" />Hyväksymismenettelyt

Yrityksesi voi käyttää vapautusprosessia osoittaakseen, että toinen käyttäjä on hyväksynyt asiakirjan, tai että ulkoinen yhteyshenkilö voi vastata asiakirjan määrityksiin seuraavien esimerkkien tapaan:

* Ostotilauksen voi vapauttaa vain, jos toimittajasi on ilmaissut, että se on valmis täyttämään tilauksen.
* Luot tilauksen, ja toisen käyttäjän täytyy ehkä suojaussyiden takia hyväksyä se ennen kuin sen voi vapauttaa.
* Kaikkien hyvitysten hyväksymisestä vastaavan päällikön tulee vapauttaa luomasi hyvityslasku.

Lisätietoja hyväksynnän työnkuluista on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).

### <a name="warehouse-activities" />Fyysisen varaston aktiviteetit

Jos tilauksen tila on **Avoin**, fyysinen varastointi ei aloita toimituksen valmistelua, eikä se odota vastaanottavansa ostotilauksen nimikkeitä. Kun vapautat tilauksen, ilmaiset, että tilaus on valmis ja että fyysinen varastointi voi sisällyttää sen aktiviteetteihinsa.

## <a name="reopen-a-released-order" />Vapautetun tilauksen avaaminen uudelleen

Vapautettuun tilaukseen voi tehdä muutoksia avaamalla sen uudelleen. Riveillä olevia, fyysisen varastoinnin jo käsittelemiä määriä voi kuitenkin vain kasvattaa.

Kun olet tehnyt muutokset ja vapautat tilauksen uudelleen, [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelma laskee ALV:n ja laskualennuksen uudelleen.

Jos vapautettuun tilaukseen tehdään muutoksia, fyysiselle varastoinnille tulee ilmoittaa muutoksista.

> [!NOTE]
> Jos haluat kirjata yksittäisen avoimen tilauksen tai hyvityslaskun ilman, että ensin vapautat sen, [!INCLUDE [prod_short](includes/prod_short.md)] vapauttaa asiakirjan automaattisesti silloin, kun kirjaat sen. Jos kirjaat tilauksia tai hyvityslaskuja käyttämällä **Kirjaa erä** -toimintoa, voit valita kirjaavasi vain vapautetut tilaukset tai hyvityslaskut.

## <a name="see-also" />Katso myös

[Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md)  
[Ostojen kirjaaminen ostolaskujen avulla](purchasing-how-record-purchases.md)  
[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)  
[Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md)  
[Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md)  
[Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)  
[Asiakirjojen arkistointi](across-how-to-archive-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
