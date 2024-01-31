---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -laajennuksella
description: 'Tässä ohjeaiheessa käsitellään pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, stream, bank account link'
ms.search.form: '1450, 1451, 1452, 1453, 1454, 1458, 1460,'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Envestnet Yodlee Bank Feeds -laajennus

Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin. Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.

Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.

> [!NOTE]
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Business Central -sovelluksen online-versiossa. Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.<br /><br />
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.
> Vain näissä maissa ja näillä alueilla sijaitsevia pankkeja tuetaan, vaikka muiden maiden tai alueiden pankit voivat näkyä Envestnet Yodlee Bank Feeds -pankin valintaikkunassa [!INCLUDE[prod_short](includes/prod_short.md)]issa.

> [!IMPORTANT]
> Uuden eurooppalaisen maksupalveludirektiivin vuoksi (PSD2), 4.9.2019 jälkeen tiliotteita ei voi enää tuoda automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)] brittiläisistä pankeista. Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.

Envestnet Yodlee Bank Feeds -palvelun edut:

* poistaa manuaalisyöttämisen tarpeen
* parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana
* tukee suuria määriä pankkeja
* tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[prod_short](includes/prod_short.md)]issa
* tukee manuaalisia ja automaattisia pankkisyötteitä
* mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.

## Käytettävissä olevat pankkisyötteet

Voit tarkistaa, tuetaanko pankkia määrittämällä ja muodostamalla yhteyden Envestnet Yodlee Bank Feeds -palveluun. Pankki näkyy luettelossa, jos sitä tukee Envestnet Yodlee.

Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

## Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
