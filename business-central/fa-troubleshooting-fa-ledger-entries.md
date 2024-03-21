---
title: KO-kirjausten laajennuksen vianetsintä
description: Kokonaisnumeroiden käsitteleminen on helpompaa. Käytä tätä laajennusta käyttöomaisuuden pyöristyksessä KO-kirjauksiin.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="the-troubleshooting-fa-ledger-entries-extension"></a>KO-kirjausten laajennuksen vianetsintä
Käytä vianetsinnän KO-kirjaustapahtumien laajennusta, kun haluat pyöristää käyttöomaisuustapahtumien poisto- ja hankintamäärät kokonaisluvuiksi. Voit esimerkiksi pyöristää arvon 30 000,44 30 000:ksi. Tyypillisiä pyöristysongelmien syitä ovat tietojen siirto, summien äkillinen kirjaaminen pääkirjanpitoon tai mukautukset, jotka olet tehnyt [!INCLUDE[prod_short](includes/prod_short.md)] -kohtaan.

KO-tapahtumien vianetsintälaajennus on esiasennettu ja valmis käytettäväksi. Jos poistat laajennuksen, mutta haluat asentaa sen uudelleen, voit etsiä sen AppSourcesta.

## <a name="troubleshooting-fixed-asset-ledger-entries"></a>Käyttöomaisuustapahtumien vianetsintä
Kun **käyttöomaisuuskortti** -sivu avataan ensimmäisen kerran, **KO-tapahtumien tarkistuksen** työjonotapahtuma on ajoitettu seuraamaan summia joka sunnuntai. Jos se löytää summan, jonka haluat ehkä pyöristää, ilmoitus tulee näkyviin, kun seuraavan kerran avaat käyttöomaisuuskorttisivun. Ilmoituksessa on **lisätietoja**-valintaikkuna , jossa voit avata **KO-tapahtumat, joissa on pyöristystapa** -sivu, jossa näkyvät ne tapahtumat, joiden summien haluat ehkä pyöristää. Voit pyöristää summan valitsemalla tapahtumat ja valitsemalla sitten **Hyväksy valinta** -toiminnon. Voit käyttää **Etsi tapahtumia, joilla on ongelmia** -toimintoa, kun haluat päivittää luettelon uusilla ongelmilla, jotka tapahtuivat sen jälkeen, kun työjonotapahtuma suoritettiin edellisenä sunnuntaina.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden hallinta](fa-manage.md)  
[Käyttöomaisuuden ylläpito](fa-how-maintain.md)  
[Business Central Onlinen mukauttaminen laajennusten avulla](ui-extensions.md)  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



