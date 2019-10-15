---
title: Yleisen päiväkirjarivin yleiskuvaus | Microsoft Docs
description: Tässä ohjeaiheessa esitellään koodiyksikköön 12, **Yleinen päiväkirja - rivin kirjaus**, tehdyt muutokset. Se on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV-, asiakas- ja toimittajatapahtumia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5589aa476662a9dff69e95d70367ae4c5e45aaba
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303554"
---
# <a name="general-journal-post-line-overview"></a>Yleisen päiväkirjan kirjausrivin yleiskuva
Koodiyksikkö 12, **Yleinen päiväkirja - rivin kirjaus**, on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV- sekä asiakkaan ja toimittajan reskontratapahtumia. Tätä koodiyksikköä käytetään myös Käytä-, Peruuta kohdistus- ja Peruuta-toiminnoissa.  
  
Vaikka koodiyksikköä on parannettu jokaisessa versiossa yli kymmenen vuoden ajan, sen arkkitehtuuri on pysynyt olennaisilta osiltaan samana. Koodiyksiköstä tuli suuri noin 7 600 rivien kanssa. Tässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa arkkitehtuuria on muutettu ja koodiyksiköstä on tehty yksinkertaisempi ja ylläpidettävämpi. Tässä ohjeessa esitellään muutokset ja tiedot, joita tarvitset päivitystä varten.  
  
## <a name="old-architecture"></a>Vanha arkkitehtuuri  
Vanhassa arkkitehtuurissa oli seuraavat ominaisuudet:  
  
* Yleisten muuttujien käyttö oli laajaa, mikä lisäsi piilotettujen virheiden mahdollisuutta, jos muuttujia käytettiin väärässä laajuudessa.  
* Moni proseduuri oli pitkä (yli 100 riviä), mikä lisäsi myös ns. Cyclomatic Complexityn suuruutta (paljon CASE, REPEAT, IF -lauseita) ja teki koodista erittäin vaikean lukea ja ylläpitää.  
* Useita proseduureja, joita käytettiin vain paikallisesti ja jotka oli tarkoitettu vain paikallisesti käytettäviksi, ei ollut merkitty paikallisiksi.  
* Suurimmalla osalla proseduureista ei ole parametreja eikä käytettyjä yleisiä muuttujia. Osa käytti parametreja ja korvasi yleisiä muuttujia paikallisilla.  
* Kirjanpitotilien hakujen koodikuvioita ja kirjanpito- ja ALV-tapahtumien luontia ei ole standardoitu ja ne vaihtelevat paikasta toiseen. Lisäksi oli paljon päällekkäisiä koodeja sekä asiakas- ja toimittajakoodien välisiä symmetriakatkoksia.  
* Suuri osa koodiyksikön 12 koodista, noin 30 prosenttia, liittyy maksualennus- ja toleranssilaskelmiin, vaikka useissa maissa tai alueilla näitä ominaisuuksia ei tarvita.  
* Kirjaus, kohdista, peruuta kohdistus, peruuta, maksualennus ja toleranssi sekä vaihtokurssin muutos on liitetty yhteen koodiyksikössä 12 yleisten muuttujien pitkää listaa käyttäen.  
  
### <a name="new-architecture"></a>Uusi arkkitehtuuri  
[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa koodiyksikkö 12 on saanut seuraavia parannuksia:  
  
* Koodiyksikkö 12 on jaettu pienempiin osiin (kaikissa alle 100 koodiriviä).  
* Kirjanpitotilien hakujen vakiomallit on toteutettu käyttämällä kirjausryhmä-taulukoiden apufunktioita.  
* Kirjausohjelmakehys on toteutettu tapahtumien aloituksen ja lopetuksen hallintaan sekä eristämään luonti kirjanpidosta ja ALV-tapahtumista, ALV-muutosten keräämiseen ja lisävaluutan summien laskemista varten.  
* Koodin kopiointi on poistettu.  
* Monet aputoiminnot on siirretty vastaaviin asiakkaan ja toimittajan tapahtumataulukoihin.  
* Yleisten muuttujien käyttö on minimoitu, jotta jokainen toimintosarja käyttää parametreja ja kapseloi oman sovelluslogiikkansa.  
  
## <a name="see-also"></a>Katso myös  
[Rakenteen tiedot: Kirjausliittymän rakenne](design-details-posting-interface-structure.md)   
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)
