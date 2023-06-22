---
title: Huoltonimikkeiden luominen
description: 'Lue, miten voit luoda huoltonimikkeitä Business Centralissa esimerkiksi huoltotilauksen sisäisesti tai toimitessasi nimikkeitä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="create-service-items" />Huoltonimikkeiden luominen

[!INCLUDE[prod_short](includes/prod_short.md)]issä huoltonimikkeellä tarkoitetaan huoltoa edellyttävää laitetta tai nimikettä. Kun luot huoltotilauksen, määrität huoltoa tarvitsevat nimikkeet. Voit linkittää huoltonimikkeen tilauksessa varaston tai huoltonimikeryhmän nimikkeeseen.    

Kun vastaanotat huoltoa tarvitsevan nimikkeen, voit rekisteröidä sen huoltonimikkeeksi. Sen voi tehdä usealla tavalla. Voit esimerkiksi luoda huoltonimikkeen **Huoltonimikkeet**-sivulla tai toisen prosessin osana esimerkiksi huoltotilausta käsiteltäessä.   

## <a name="to-create-a-service-item" />Huoltonimikkeiden luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order" />Huoltonimikkeiden luominen huoltotilauksissa

Kun vastaanotat huollettavaksi nimikkeitä, jotka haluat rekisteröidä huoltonimikkeiksi, ne voi luoda huoltonimikkeiksi **Huoltotilaus**- tai **Huoltotarjous**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Luo huoltonimike** -toiminto.  

    Numero annetaan huoltonimikkeelle ja huoltonimikekortti luodaan. Se täyttää **Huoltonimikkeen nro** -kentän uuden huoltonimikkeen numerolla.

## <a name="to-create-a-service-item-when-shipping-items" />Huoltonimikkeiden luominen nimikkeitä toimitettaessa

Kun nimikkeitä toimitetaan kirjaamalla joko myyntitilauksia tai myyntilaskuja, ohjelma rekisteröi toimitetut nimikkeet automaattisesti huoltonimikkeiksi, jos seuraava ehto toteutuu. Nimikkeiden tulee kuulua huoltonimikeryhmään, jonka **Luo huoltonimike** -kentässä on valintamerkki. Jos nimikkeille on rekisteröity sarjanumero Nimikkeen seurantarivit -sivulla, ohjelma kopioi tämän tiedon automaattisesti huoltonimikekortin **Sarjanro**-kenttään huoltonimikkeiden luonnin yhteydessä.  

Seuraavassa kuvataan, miten huoltonimikkeitä luodaan myyntitilauksissa olevia nimikkeitä toimitettaessa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa käsiteltävä myyntitilaus.  
3. Valitse **Kirjaa**- tai **Kirjaa ja tulosta** -toiminto.  
4. Valitse **Toimitus**- tai **Toimitus ja lasku** -toiminto.  
5. Ohjelma luo automaattisesti huoltonimikkeet tilauksessa oleville nimikkeille, jos ne kuuluvat huoltonimikkeiden luomiseksi määritettyyn huoltonimikeryhmään. Jos **Nimikkeen seurantarivit** -sivulla on rekisteröity sarjanumeroita, nämä määritetään huoltonimikkeille.  

> [!NOTE]  
>  Jos nimike on tuoterakenne ja olet purkanut tuoterakenteen, puretun tuoterakenteen nimikkeitä käsitellään tavallisen nimikkeen tavoin. Ohjelma luo huoltonimikkeet huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan. Jos lisäksi huoltonimike on luotu puretun tuoterakenteen nimikkeelle, joka muodostuu muista tuoterakenteen komponenteista, nämä nimikkeet luodaan puretun tuoterakenteen huoltonimikkeen huoltonimikkeen komponenteiksi.  
>   
>  Jos nimike on tuoterakenne etkä ole purkanut tuoterakennetta, ohjelma luo nimikkeelle huoltonimikkeen huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan.  

## <a name="to-insert-a-starting-fee-for-a-service-item" />Aloitusmaksujen syöttäminen huoltonimikkeille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeen työkirja** -toiminto.
3. Valitse ensin huoltorivi ja sitten **Toiminnot**. Valitse sitten **Toiminnot** ja lopuksi **Syötä aloitusmaksu** -toiminto.  

    Ohjelma lisää **Kustannus**-tyypin huoltorivin, jolla on aloitusmaksu. Tämä aloitusmaksu koskee valittua huoltonimikettä.

## <a name="see-related-microsoft-trainingtrainingmodulescreate-items" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-items/)

## <a name="see-also" />Katso myös

[Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen](service-how-setup-service-items.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huoltohallinto](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
