---
author: brentholtorf
ms.topic: include
ms.date: 05/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
**Käyttäjät**-luettelossa voi näkyä muita käyttäjiä oman yrityksesi lisäksi. Kun jälleenmyyntikumppaniyrityksen valtuutettu järjestelmänvalvoja kirjautuu [!INCLUDE [prod_short](prod_short.md)] -ympäristöön asiakkaansa puolesta, hänet luodaan automaattisesti [!INCLUDE [prod_short](prod_short.md)] -käyttäjäksi. Tällä tavalla delegoitujen järjestelmänvalvojan tekemät toimet kirjataan lokiin [!INCLUDE [prod_short](prod_short.md)] -ohjelmassa, kuten asiakirjojen kirjaaminen ja niihin liittyvät käyttäjätunnukset.  

Kun *rakeisia delegoituja järjestelmänvalvojan oikeuksia (GDAP)* käytetään, käyttäjä näkyy **käyttäjät**-luettelossa ja hänelle voidaan määrittää mitä tahansa oikeuksia. Niitä ei näytetä nimen ja muiden henkilötietojen kanssa, vaan yrityksen nimen ja yksilöllisen tunnuksen kanssa. Sekä sisäiset että ulkoiset järjestelmänvalvojat näkevät nämä käyttäjät **Käyttäjät**-luettelossa, ja heillä on täysi avoimuus näiden käyttäjien tekemiseen esimerkiksi [muutoslokin](../across-log-changes.md) kautta. He eivät kuitenkaan näe näiden käyttäjien todellista nimeä. GDAP-käyttäjät on lueteltu käyttäjänimineen seuraavassa muodossa: `User123456@partnerdomain.com`. Heillä saattaa olla käyttäjänimi, joka vastaa kumppanin yrityksen nimeä, eikä sähköpostiosoite ole henkilön todellinen sähköpostiosoite. Tällä tavalla GDAP-käyttäjätilit eivät paljasta henkilökohtaisia tietoja. Jos sinun on selvitettävä, kuka tällaisen pseudonyymin takana on, sinun on otettava yhteyttä yritykseen, jossa tämä käyttäjä työskentelee tai työskenteli.  
