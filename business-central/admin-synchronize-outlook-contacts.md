---
title: Jaa kontaktit Business Centralin ja Outlookin välillä
description: 'Palvelulla on laaja integrointi Microsoft 365:n kanssa, jotta voit jakaa kontakteja Outlookin ja Business Centralin välillä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook" />Business Centralin kontaktien synkronisointi Microsoft Outlookin yhteystietojen kanssa

Voit määrittää kontaktien synkronoinnin siten, että kontakteillasi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on samat tiedot kuin kontakteillasi Microsoft Outlookissa. Myyjät esimerkiksi saattavat käyttää Outlookia ja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa samanaikaisesti. Jos kontaktit ovat samat molemmissa, työ on yksinkertaisempaa.  

Synkronoimasi kontaktit säilytetään oletusarvoisesti Outlookin kansioruudun suosikkien **Business Central** -kansiossa. Business Central -kansion avulla on helpompi tunnistaa, mitkä kontaktit synkronoidaan. Voit määrittää suodattimia synkronoidaksesi vain tietyt kontaktit [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta Outlookiin. Synkronoinnin määrittämisen jälkeen voit synkronoida manuaalisesti tai automatisoida prosessin suorittamaan synkronoinnin säännöllisin väliajoin.  

## <a name="prerequisites" />Vaatimukset

- [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjäprofiilissasi määritetään oma Microsoft 365 -sähköpostitilisi.

  Voit tarkistaa tämän asetuksen **Käyttäjät**-luettelossa oman käyttäjäprofiilisi **Microsoft 365 -todennus** -osassa.
- [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelman avulla olet määrittänyt kontaktin synkronoinnin [Määritä yhteystietojen synkronointi paikallisen Outlook for Business Central -ohjelman kanssa](admin-contact-sync-setup-onprem.md) -kohdassa kuvatulla tavalla

## <a name="set-up-synchronization" />Synkronoinnin määritys

Määrität, miten haluat synkronoida Outlookin yhteystiedot [!INCLUDE[prod_short](includes/prod_short.md)]:n **Exchangen synkronointiasetukset** -sivulla. 

**Exchangen synkronointiasetukset** -sivulla voit tarkistaa, että yhteys Exchangeen toimii ja määrittää sitten synkronoinnin. **Exchangen synkronointiasetukset** -sivulla voit avata **Kontaktien synkronointiasetukset** -sivun ja aloittaa synkronoinnin. Voit myös määrittää suodattimen määrittääksesi, mitkä kontaktit synkronoidaan. Voit esimerkiksi suodattaa nimen, tyypin, yrityksen jne. perusteella. Voi myös muuttaa sen kansion oletusnimeä, johon yhteystiedot synkronoidaan Outlookissa.  

Kunkin työtovereistasi voi myös määrittää oman Exchange-synkronointinsa ja määrittää suodattimia sille, mitkä kontaktit halutaan synkronoida.  

Synkronoinnin määrittämisen jälkeen voit synkronoida kontaktin muutokset manuaalisesti tai voit automatisoida prosessin määrittämällä työjonotapahtuman. Lisätietoja automaatiosta on tämän artikkelin seuraavassa osassa.

### <a name="automate-synchronization" />Synkronoinnin automatisointi

Voit luoda työjonotapahtuman, joka synkronoi kontaktit määrittämäsi aikataulun mukaan. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md). 

Seuraava taulukko sisältää **Työjonotapahtumakortin** asetukset, jotka on tarkoitettu kontaktien synkronointia varten:

|Kenttä|Kontaktin synkronoinnin asetus|
|-----|-----|
|Suoritettavan objektin tyyppi|Koodiyksikkö|
|Suoritettavan objektin tunnus|6700|

## <a name="synchronize-contacts" />Kontaktien synkronointi

Jos olet tottunut käyttämään kontakteja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, sinun on helppo suorittaa synkronointi manuaalisesti **Kontaktit**-luettelosta aina, kun se sinulle sopii. Voit synkronoida kontakteja kahdella tavalla:

* **Synkronoi Microsoft 365:nn kanssa**

  Synkronoi kaikki edellisen synkronoinnin jälkeiset muutokset [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta Microsoft 365:een viimeisimmän muokkauksen päivämäärän perusteella. Kaikki uudet yhteystiedot Microsoft 365:ssä synkronoidaan [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Tyypillisesti tämä toiminto on täyttä synkronointia nopeampi. 

* **Täysi synkronointi Microsoft 365:n kanssa**

  Synkronoi kaikki yhteyshenkilöt molempiin suuntiin riippumatta viimeisen synkronoinnin päivämäärästä tai viimeksi muokattu -päivämäärästä.  

Molemmissa tapauksissa kontaktit synkronoidaan Outlookista vain jos niiden pakolliset kentät on täytetty. Pakolliset kentät Microsoft 365:een synkronointiin ovat **Nimi** ja **Sähköpostiosoite**, minkä lisäksi kontaktin on oltava tyyppiä **Henkilö**. [!INCLUDE[prod_short](includes/prod_short.md)] on kontaktitietojen lähde, joten [!INCLUDE[prod_short](includes/prod_short.md)] -kontaktitiedot tallennetaan, jos kaksoiskappaleita esiintyy.  

> [!NOTE]
> Jos poistat kontaktin Outlookissa, mutta haluat säilyttää sen [!INCLUDE[prod_short](includes/prod_short.md)] ohjelmassa, kontakti luodaan Outlookissa uudelleen seuraavan synkronoinnin yhteydessä. 

## <a name="see-also" />Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Kontaktien (Henkilöt) käyttäminen Outlookin verkkoversiossa](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
