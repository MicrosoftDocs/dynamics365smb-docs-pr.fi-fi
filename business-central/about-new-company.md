---
title: Uusien yritysten luominen asetusten ohjatun määritysoppaan avulla
description: 'Business Central -sovellukseen on helppo luoda uusi, tyhjä yritys. Asetusten ohjattu määritysopas antaa tarkkoja ohjeita, ja voit tuoda liiketoimintatiedot.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa

[!INCLUDE[prod_short](includes/prod_short.md)]in liiketoimintayksikölle tai yritykselle kuuluvaa liiketoimintatietojen säilöä kutsutaan *yritykseksi*. Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]iin, saat käyttöösi esimerkkiyrityksen ja tyhjän yrityksen, jonka nimi on *Oma yritys*. Yritysten välillä siirtyminen on helppoa: valitse vain **Omat asetukset** ja siirry toiseen yritykseen. Voit myös luoda uusia yrityksiä [!INCLUDE[prod_short](includes/prod_short.md)]issa yrityksen tarpeiden mukaan.  

> [!NOTE]
> Jotta voisit luoda uuden yrityksen, sinulle täytyy olla määritetty **Super**-käyttöoikeusjoukko.

Kun luot uuden yrityksen, asetusten ohjattu määritysopas auttaa varmistamaan, että perustoiminnot ovat kohdallaan. Voit tuoda tämän jälkeen tiedot vanhasta järjestelmästä tai toisesta [!INCLUDE[prod_short](includes/prod_short.md)]in yrityksestä.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Valitse oikea malli

Jos päätät lisätä yrityksen [!INCLUDE[prod_short](includes/prod_short.md)]iin, pääset alkuun käyttämällä ohjattua **Luo uusi yritys** -asetusten määritystä. Asetusoppaan voi valita **Yritykset**-sivulla ja **Omat asetukset** -kohdassa **Yritys**-kentän valintaruudussa.  

Asennusoppaassa on kolme mallia ja tyhjä vaihtoehto:

- **Arviointi – esimerkkitiedot**  
    Luo yritys, joka muistuttaa esittely-yritystä, jossa on malli- ja asetustietoja. Tämän tyyppinen yritys on käytettävissäsi ilman, että siirrytään 30 päivän kokeilujaksoon, jota muut tyypit edellyttävät.  
- **Laajennettu arviointi - Kokonaisesimerkkitiedot** Luo yritys, jolla on lisätoiminnon laajuus ja joka sisältää kaiken tarvittavan tuotteen arviointiin niissä yrityksissä, joissa on edistyneitä prosesseja. Tämän tyyppinen yritys on käytettävissäsi ilman, että siirrytään 30 päivän kokeilujaksoon, jota muut tyypit edellyttävät.
- **Tuotanto – vain määritystiedot**  
    **Oman yrityksen** kaltaisen yrityksen luominen käyttäen asetustietoja, kuten tilikarttaa, maksutapoja ja rahoitusraporttien määrityksiä, mutta ei esimerkkitietoja. Voit käyttää tätä yritystä 30 päivän kokeilujakson ajan.
- **Luo uusi – ei tietoja**  
    Luo tyhjä yritys ilman asetustietoja. Voit käyttää tätä yritystä 30 päivän kokeilujakson ajan.  

Jos haluat, että uuden yrityksen käytön aloittaminen on helppoa, valitse **Tuotanto - Vain määritystiedot** ja tuo omat liiketoimintatietosi, kuten asiakkaat, nimikkeet ja toimittajat. Valitse **Uusi**-malli, jos haluat määrittää kaiken itse alusta alkaen. Voit siinä tapauksessa aloittaa tärkeimpien asetustietojen käytön käyttämällä asetusten ohjatun **Yrityksen asennus** -määrityksen ohjeita.  

> [!NOTE]  
> Kun luot uuden yrityksen, kestää joitakin minuutteja, ennen kuin sitä voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa. **Yritykset**-sivulla oleva asennuksen tila ilmaisee, kun uusi yritys on valmis. Voit siirtyä sitten uuteen yritykseen **omissa asetuksissa**.  

30 päivän kokeilujakson aikana luotavien yritysten määrää ei ole rajoitettu, mutta niitä voi käyttää vain kokeilujakson aikana. Pyydä lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]-kumppanilta. Katso myös [Dynamics 365 Business Central -kokeiluversion UKK](trial-faq.md) -artikkeli.  

Järjestelmänvalvoja saa lisätietoja kokeiluversioista ja tilauksista [täältä](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## Kopioi yritys

**Yritykset** -sivulla voit käyttää **Kopiointi**-toimintoa toisen yrityksen luomiseen olemassa olevan yrityksen sisällön perusteella. Yrityksen kopioimisesta on hyötyä esimerkiksi silloin, kun haluat testata yritystä häiritsemättä tuotantotietoja.

> [!Important]
> Älä käytä Kopioi-toimintoa yrityksen varmuuskopiointiin. Varmuuskopion ottaminen alkaa viemällä tietokanta .bacpac-tiedostona. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Tietokantojen vieminen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export).

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Määritä yritys

Kun kirjaudut uuteen yritykseen, ohjattu **Yrityksen asennus** -asetusten ohjattu määritysopas helpottaa aloittamista. Opas kysyy yritystä koskevia tietoja, kuten osoite, pankkitiedot ja varaston arvostusmenetelmä. Nämä tiedot muodostavat perustan monille alueille [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, joten niitä ei tarvitse määrittää manuaalisesti.  

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää esimerkiksi yrityksen osoitteen laskuissa ja muissa asiakirjoissa sekä pankkitiedot maksuissa. Arvostusmenetelmää käytetään hintojen ja varaston arvostuksen laskemiseen.  

Kun perustiedot on annettu, voi määrittää loput keskeiset alueet. Sen jälkeen voi aloittaa liiketoimintatietojen, kuten asiakkaiden ja toimittajien, lisäämisen. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman määrittäminen](setup.md).  

## Yritykset ja ympäristöt

[!INCLUDE [company_environment](includes/company_environment.md)]

Lisätietoja on kohdassa [Siirtyminen toiseen yritykseen tai ympäristöön](ui-organization-switch.md). Lisätietoja ympäristöistä: [Business Central Onlinen infrastruktuurin ymmärtäminen](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (vain englanniksi).  

## Yrityksen nimen muuttaminen

Kun olet luonut yrityksen, sen nimeä ei voi muuttaa. Voit kuitenkin muuttaa sen **näyttönimeä** eli tekstiä, joka näkyy kaikkialla sovelluksessa yrityksen nimenä.  

> [!TIP]
> Voit nimetä yrityksen uudelleen, jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiota.

## Lisää Contoso Coffee

Contoso Coffee -sovellus sisältää esittelytietoja, joiden avulla voit tutkia [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman kehittyneitä ominaisuuksia. Etsi sovellus AppSourcessa ja asenna se tyhjään yritykseen, esimerkiksi yritykseen eristysympäristössä. Lisätietoja on kohdassa [Johdatus Contoso Coffee -demotietoihin](contoso-coffee/contoso-coffee-intro.md).  

## Katso myös

[Business Central -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Business Central Onlinen infrastruktuurin ymmärtäminen (vain englanniksi)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
