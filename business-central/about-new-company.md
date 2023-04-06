---
title: Uusien yritysten luominen asetusten ohjatun määritysoppaan avulla
description: 'Business Central -sovellukseen on helppo luoda uusi, tyhjä yritys. Asetusten ohjattu määritysopas antaa tarkkoja ohjeita, ja voit tuoda aiemmin luomasi liiketoimintatiedot.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/01/2021
ms.author: edupont
---
# Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)]issa

[!INCLUDE[prod_short](includes/prod_short.md)]in liiketoimintayksikölle tai yritykselle kuuluvaa liiketoimintatietojen säilöä kutsutaan *yritykseksi*. Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]iin, saat käyttöösi esimerkkiyrityksen ja tyhjän yrityksen, jonka nimi on *Oma yritys*. Yritysten välillä siirtyminen on helppoa: valitse vain **Omat asetukset** ja siirry toiseen yritykseen. Voit myös luoda uusia yrityksiä [!INCLUDE[prod_short](includes/prod_short.md)]issa yrityksen tarpeiden mukaan.  

Kun luot uuden yrityksen, asetusten ohjattu määritysopas auttaa varmistamaan, että perustoiminnot ovat kohdallaan. Voit tuoda tämän jälkeen tarvittavat tiedot vanhasta järjestelmästä tai toisesta [!INCLUDE[prod_short](includes/prod_short.md)]in yrityksestä.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Valitse oikea malli

Jos päätät lisätä yrityksen [!INCLUDE[prod_short](includes/prod_short.md)]iin, pääset alkuun käyttämällä ohjattua **Luo uusi yritys** -asetusten määritystä. Ohjatun asetustoiminnon voi valita **Yritykset**-sivulla ja **Omat asetukset** -kohdassa **Yritys**-kentän valintaruudussa.  

Ohjatussa asennuksessa on kaksi mallia ja tyhjä vaihtoehto:

- **Arviointi - Mallitiedot**  
    Näin luotu yritys muistuttaa esittely-yritystä, jossa on malli- ja asetustietoja. Tämän tyyppinen yritys on käytettävissäsi ilman, että siirrytään 30 päivän kokeilujaksoon, jota muut tyypit edellyttävät.  
- **Tuotanto - Vain määritystiedot**  
    Näin luotu yritys muistuttaa **omaa yritystä**, jossa on asetustietoja mutta mallitiedot puuttuvat. Voit käyttää tätä yritystä 30 päivän kokeilujakson ajan.  
- **Luo uusi - Ei tietoja**  
    Näin luotu yritys on tyhjä eikä siinä ole asetustietoja. Voit käyttää tätä yritystä 30 päivän kokeilujakson ajan.  

Jos haluat, että uuden yrityksen käytön aloittaminen on helppoa, valitse **Tuotanto - Vain määritystiedot** ja tuo omat liiketoimintatietosi, kuten asiakkaat, nimikkeet ja toimittajat. Valitse **Uusi**-malli, jos haluat määrittää kaiken itse alusta alkaen. Voit siinä tapauksessa aloittaa tärkeimpien asetustietojen käytön käyttämällä asetusten ohjatun **Yrityksen asennus** -määrityksen ohjeita.  

> [!NOTE]  
> Kun luot uuden yrityksen, kestää joitakin minuutteja, ennen kuin sitä voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa. **Yritykset**-sivulla oleva asennuksen tila ilmaisee, kun uusi yritys on valmis. Voit siirtyä sitten uuteen yritykseen **omissa asetuksissa**.  

30 päivän kokeilujakson aikana luotavien yritysten määrää ei ole rajoitettu, mutta niitä voi käyttää vain kokeilujakson aikana. Pyydä lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]-kumppanilta. Katso myös [Dynamics 365 Business Central -kokeiluversion UKK](trial-faq.md) -artikkeli.  

Järjestelmänvalvoja saa lisätietoja kokeiluversioista ja tilauksista [täältä](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## Kopioi yritys

**Yritykset** -sivulla voit käyttää **Kopiointi**-toimintoa toisen yrityksen luomiseen olemassa olevan yrityksen sisällön perusteella. Tästä on hyötyä esimerkiksi silloin, kun haluat testata yritystä häiritsemättä tuotantotietoja.

> [!Important]
> Tätä toimintoa ei voi käyttää yrityksen varmuuskopiointiin. Yrityksen varmuuskopion ottaminen alkaa viemällä tietokanta .bacpac-tiedostona. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Tietokantojen vieminen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export).

## Määritä yritys

Kun kirjaudut uuteen yritykseen, ohjattu **Yrityksen asennus** -toiminto suoritetaan automaattisesti, mikä helpottaa aloittamista. Sinulta kysytään yritystä koskevia tietoja, kuten osoite, pankkitiedot ja varaston arvostusmenetelmä. Nämä tiedot kysytään, koska ne ovat perustietoja monilla [!INCLUDE[prod_short](includes/prod_short.md)]in alueilla ja tällä tavoin niitä ei tarvitse määrittää myöhemmin manuaalisesti.  

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää esimerkiksi yrityksen osoitteen laskuissa ja muissa asiakirjoissa sekä pankkitiedot maksuissa. Arvostusmenetelmää käytetään hintojen ja varaston arvostuksen laskemiseen.  

Kun perustiedot on annettu, voi määrittää loput keskeiset alueet. Sen jälkeen voi aloittaa liiketoimintatietojen, kuten asiakkaiden ja toimittajien, lisäämisen. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman määrittäminen](setup.md).  

## Yritykset ja ympäristöt

[!INCLUDE [company_environment](includes/company_environment.md)]

Lisätietoja on kohdassa [Siirtyminen toiseen yritykseen tai ympäristöön](ui-organization-switch.md). Lisätietoja ympäristöistä: [Business Central Onlinen infrastruktuurin ymmärtäminen](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (vain englanniksi).  

## Yrityksen nimen muuttaminen

Kun yritys on luotu, sen nimeä ei voi muuttaa. Mutta voit muuttaa sen **näyttönimeä** eli tekstiä, joka näkyy kaikkialla sovelluksessa yrityksen nimenä.  

> [!TIP]
> Voit nimetä yrityksen uudelleen, jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiota.

## Lisää Contoso Coffee

Contoso Coffee -sovellus sisältää esittelytietoja, joiden avulla voit tutkia [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman kehittyneitä ominaisuuksia. Etsi sovellus AppSourcessa ja asenna se tyhjään yritykseen, esimerkiksi yritykseen eristysympäristössä. Lisätietoja on kohdassa [Johdatus Contoso Coffee -demotietoihin](contoso-coffee/contoso-coffee-intro.md).  

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-new-companies-dynamics-365-business-central/)

## Katso myös

[Business Central -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Business Central Onlinen infrastruktuurin ymmärtäminen (vain englanniksi)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
