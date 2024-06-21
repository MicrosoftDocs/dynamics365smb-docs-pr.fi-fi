---
title: Tiedonsiirron määrittäminen tiedostojen lähettämistä ja vastaanottamista varten
description: Määritä tiedonsiirtokehys siirtääksesi tietoja ulkoisten tiedostojen kanssa sekä lähettääksesi ja vastaanottaaksesi sähköisiä asiakirjoja tai tuodaksesi tai viedäksesi pankkitiedostoja.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Tiedonsiirron määrittäminen

Ennen kuin voit lähettää ja vastaanottaa sähköisiä asiakirjoja tai tuoda ja viedä pankkitiedostoja, sinun on määritettävä tiedonsiirtokehys tiedostojen käsittelemistä varten. Lisäksi sinun on määritettävä liittyvät alueet, kuten asiakkaat, joille lähetät sähköiset laskut, tai AMC Banking 365 Fundamentals -laajennuksen, jos käytät pankkitiedostojen muuntamiseen ulkoista palveluntarjoajaa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

 Kun [!INCLUDE[prod_short](includes/prod_short.md)] on määritetty vaihtamaan tietoja ulkoisten tiedostojen kanssa, käyttäjät voivat käyttää määritystä yleisissä liiketoimintatehtävissä, kuten sähköisten asiakirjojen lähettämisessä ja vastaanottamisessa sekä pankkitiedostojen tuonnissa ja viennissä.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä valmiiksi määritetty document exchange -palvelu sallimaan lähettää ja vastaanottaa sähköisiä asiakirjoja [!INCLUDE[prod_short](includes/prod_short.md)]:n kanssa.|[Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)|  
|Määritä valmiiksi määritetty OCR-palvelu muuntamaan PDF- tai kuvatiedostot sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]in tiedoston tietueiksi.|[Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md)|  
|Määritä yksi tai kaksi esimääritettyä palvelua käyttämään päivitettyjä valuuttakursseja, jotta saat uusimmat valuutanvaihtokurssit järjestelmään **Valuutat**-sivulle.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|  
|Määritä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, toimittajat, nimikkeet ja mittayksiköt, jotka liittyvät tietojen yhdistämiseen [!INCLUDE[prod_short](includes/prod_short.md)]issa.|[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.|[SEPA-hyvityksen siirron määrittäminen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Valmistele pankkitilimuodot, maksutavat ja asiakkaan SEPA-suoraveloitussopimukset.|[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)|  
|Määritä käyttäjätunnistus ja AMC Banking 365 Fundamentals -laajennuspalvelun URL-osoite, joka vaaditaan, jotta pankkitiedostot voidaan muuttaa pankkisi vaatimaan muotoon.|[Käytä AMC Banking 365 Fundamentals -laajennusta](ui-extensions-amc-banking.md)|  
|Määritä ja ota käyttöön ulkoinen palvelu, jonka avulla voit tuoda pankin tiliotteet suoraan pankkisyötteinä.|[Pankin tiliotepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Kun tiliotepalvelu on otettu käyttöön, linkitä pankkitilit [!INCLUDE[prod_short](includes/prod_short.md)]issa.|[Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md)|  
|Määritä tietojen vienti [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa Intrastat-raportointia varten.|[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md)|
|Valmistele datatiedoston tai tietovirran uuden tietojenvaihtomäärityksen luonti käyttämällä tiedoston XML-rakennetta. Se esitäyttää **Sarakkeen määritykset** -pikalomakkeen **Kirjauksen tiedonsiirtomääritykset** -sivulla.|[XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Määritä tietojen vaihtokehys, jotta käyttäjät voivat vastaanottaa ja lähettää tietoja uudessa ostoasiakirjamuodossa, tuoda uuden pankkitiedoston tai vaihtaa muita tietoja.|[Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)|  

## Katso myös

[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
