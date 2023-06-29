---
title: Sulje kiinteän kohdistuksen kautta tulleita nimiketapahtumia.
description: 'Ktaso, miten voit luoda kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille nimikepäiväkirjassa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 40
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen

Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille. Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen.  

> [!IMPORTANT]  
> Tällä tavoin tehdyt kiinteät kohdistukset koskevat vain kustannuksia, eivät määrää. Näin ollen kirjattu positiivinen nimiketapahtuma ei sulje käytettyä lähtevää tapahtumaa, ja pysyy itse avoinna. Tämä pätee myös silloin, kun positiivisen tapahtuman kiinteä kohdistus kirjataan negatiiviseen tapahtumaan, jota tavallinen positiivinen tapahtuma ei ole sulkenut, jolloin sekä negatiivinen että positiivinen tapahtuma jäävät avoimiksi.  
>
> Tämä tarkoittaa myös sitä, että varastokautta ei voi sulkea, jos tällainen tapahtuma on olemassa.  

Voit tietyin edellytyksin muuttaa ja uudelleen käyttää kohdistustapahtumia **Kohdistustyökirja**-sivulla.  

Seuraavassa ohjeessa neuvotaan, miten sulkea nämä tapahtumat suorittamalla kaksi korjaavaa kirjausta nimikepäiväkirjaan.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Sulje avoimet nimiketapahtumat, jotka aiheutuvat nimikepäiväkirjan kiinteästä kohdistuksesta

1. Kirjaa **Kohdistukset tapahtumista** -kentässä positiivinen muutos ja vastaava määrä. Tämä sulkee alkuperäisen korjaavan negatiivisen tapahtuman, jossa on kiinteä kohdistus.  

    **Kohdistukset tapahtumista** -kenttä määrittää lähtevän nimikepäiväkirjatapahtuman numeron, jonka kustannukset välitetään saapuvaan nimikepäiväkirjatapahtumaan silloin, kun kirjaat saapuvan transaktion tyyppiä **Posit. muutos** tai **Osto** nimikepäiväkirjan kanssa.  
2. Kirjaa negatiivinen muutos **Kohdistetaan tapahtumaan** -kentässä. Tämä sulkee alkuperäisen korjaavan positiivisen tapahtuman, jossa on kiinteä kohdistus.  

    **Kohdistukset tapahtumista** -kenttä määrittää, onko nimikepäiväkirjan rivin määrä kohdistettava jo kirjattuun asiakirjaan. Jos rivi on kohdistettava jo kirjattuun asiakirjaan, anna sen nimiketapahtuman numero, johon haluat kohdistaa nimikepäiväkirjan rivin.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Nimiketapahtumien poistaminen ja uudelleenkohdistaminen](finance-how-to-remove-and-reapply-item-entries.md)  
[Myynnin palautusten ja peruutusten käsittely](sales-how-process-sales-returns-cancellations.md)  
[Varastonarvostuksen ja kustannuslaskennan määrittäminen](finance-set-up-inventory-valuation-and-costing.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
