---
title: Document Exchange -palvelun määrittäminen | Microsoft Docs
description: Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 8804b9bb7f7b8112e54e8a9953198db8686f768d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133380"
---
# <a name="set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen
Osana tiedonvaihtokehystä voit vaihtaa myynti- ja osto asiakirjoja kauppakumppaneiden kanssa ilman lisävaiheita, kuten dokumenttien liittämistä sähköpostiviesteihin PDF-tiedostoina. Kun esimerkiksi olet valmis laskuttamaan asiakasta, voit kirjata laskun ja lähettää sen maksettavaksi tiedostona, jonka asiakas voi vastaanottaa liiketoiminnan hallintasovelluksessaan. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).

> [!NOTE]
> Business Centralin on-premises -version asiakirjojen vaihtopalvelun määrittäminen edellyttää joitakin lisävaiheita valtuutusta varten. Lisätietoja on kohdassa [Business Central On-Premises -version asetukset](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Yhdistäminen kauppakumppaneihin
Sähköisten asiakirjojen vaihtaminen edellyttää yhteyttä kauppakumppaneihin. [!INCLUDE[prod_short](includes/prod_short.md)] online on määritetty käyttämään Business Central Integration-sovellusta, jotta suojatun yhteyden luominen on helppoa. Sovellus on saatavilla Tradeshift App Storessa, ja kaikki sinun ja liikekumppanisi tarvitsee vain luoda Tradeshift-tili ja ottaa sitten sovellus käyttöön. Business Central Integration -sovellus on saatavilla tuotanto- ja sandbox-versioina. Esimerkiksi sandbox-version käyttäminen on hyvä asiakirjojen vaihtamisen testaamista varten. Voit vaihtaa tuotanto- ja sandbox-versioiden välillä kääntämällä **Sandbox**-valitsimen päälle tai pois päältä **Document Exchange -palvelun asetukset** -sivulla. Kun teet näin, **Palvelu**-pikavälilehden tiedot päivitetään.

Vaihtoehtoisesti jos haluat käyttää muuta palvelua, sinun on annettava tiedot yhteyden muodostamista varten. Lisätietoja on kohdassa [Document Exchange -palveluun yhdistäminen](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Yhteyden muodostaminen Business Central Integration -sovellukseen Tradeshiftissa
Voit luoda nopeasti Tradeshift-tilin ja aloittaa Business Central Integration -sovelluksen käytön **Document Exchange -palvelun asetukset** -sivulta. Valitse joko **Aktivoi sovellus** linkki ilmoituksessa tai **Sovelluksen URL** -kenttä ja siirry sovellukseen Tradeshift App Storessa. Kirjaudu sisään tai rekisteröidy Tradeshiftin kirjautumissivulla.

> [!NOTE]
> Kun olet kirjautunut Tradeshift-tiliisi, sivustosi ei ehkä siirrä sivulle, jolla sovellus aktivoidaan. Voit tehdä sen napsauttamalla uudelleen Business Centralissa **Document Exchange -palvelun asetukset** -sivun linkkiä, jolloin siirryt suoraan sovellukseen.

Jos päätät lopettaa Business Central Integration -sovelluksen käyttämisen, poista se Tradeshift App Storessa. 

## <a name="to-connect-to-a-document-exchange-service"></a>Document Exchange -palveluun yhdistäminen  
Jos haluat käyttää toista asiakirjan vaihtopalvelua, sinun täytyy antaa joitakin tietoja yhteyden muodostamiseksi palveluun.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Document Exchange -palvelun asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjäagentti**|Anna teksti, jolla voidaan tunnistaa yrityksesi asiakirjan vaihtoprosesseissa.|  
    |**Käytössä**|Määritä, onko yhteys palveluun otettu käyttöön.<br><br> **Huomautus:** Kun palvelu otetaan käyttöön, ainakin kaksi työjonon tapahtumaa luodaan lähettämään ja vastaanottamaan sähköisiä asiakirjoja. Kun palvelu poistetaan käytöstä, työjonon tapahtumat poistetaan.|  
    |**Eristysympäristö**|Määrittää, muodostetaanko yhteys asiakirjavaihtopalvelun Sandbox-versioon.|
    |**Rekisteröitymisen URL-osoite**|Määritä verkkosivu, jossa document exchange -palvelu rekisteröidään.|  
    |**Sovelluksen URL-osoite**|Valitse linkki, jonka avulla voit avata sovelluskaupan ja ottaa Business Central Integration -sovelluksen käyttöön tai poistaa sen käytöstä.|
    |**Palvelun URL-osoite**|Määritä sen document exchange -palvelun osoite, joka kutsutaan, kun lähetät ja vastaanotat sähköisiä asiakirjoja.|  
    |**Kirjautumisen URL-osoite**|Määritä sen sivun URL-osoite, jossa document exchange -palveluun kirjaudutaan. Tämä on sivu, johon annat yrityksesi käyttäjänimen ja salasanan.|  
    
    > [!NOTE]  
    > Kirjautumistiedot salataan automaattisesti. Salausta ei voi poistaa käytöstä.

    > [!NOTE]
    > Jos et pysty muodostamaan yhteyttä asiakirjan vaihtopalveluun valtuutusongelman vuoksi, syynä voi olla se, että [!INCLUDE[prod_short](includes/prod_short.md)] ei voi uudistaa automaattisesti käyttöoikeustunnusta. Tämä voi johtua tapahtua, jos palvelua ei ole käytetty pitkään aikaan. Voit uudistaa tunnuksen manuaalisesti **Uudista tunnus** -toiminnon avulla.

## <a name="settings-for-business-central-on-premises"></a>Business Central On-Premises -version asetukset
Jotta voisit yhdistää Business Central on-premises -versioon, sinun on luotava sovellus Tradeshift App Storessa. Kun teet näin, käytä **Document Exchange Service Setup** -sivun **Uudelleenohjauksen URL** -kenttää. Kun olet rekisteröinyt sovelluksesi, Tradeshift antaa asiakastunnuksen ja asiakassalaisuuden. Anna [!INCLUDE[prod_short](includes/prod_short.md)]issa kyseiset arvot **Document Exchange -palvelun asetukset** -sivun **Valtuutus**-pikavälilehdessä.

Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetClientId- ja OnGetClientSecret-tapahtumat codeunitissa 1410 Doc. Exch. Service Mgt.

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]