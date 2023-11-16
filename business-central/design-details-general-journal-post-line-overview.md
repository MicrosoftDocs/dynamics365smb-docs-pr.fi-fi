---
title: Yleisen päiväkirjan kirjausrivin yleiskuva
description: 'Tässä aiheessa on tietoja muutoksista Codeunit 12, Gen. Jnl.-Post -riviin, ja se on ainoa paikka, jossa voidaan lisätä kirjanpito-, ALV- sekä asiakas- ja toimittajatapahtumia.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, general ledger, post'
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="general-journal-post-line-overview"></a>Yleisen päiväkirjan kirjausrivin yleiskuva

Codeunit 12, **Yleinen päiväkirja - rivin kirjaus**, on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV- sekä asiakkaan ja toimittajan reskontratapahtumia. Tätä codeunitia käytetään myös Käytä-, Peruuta kohdistus- ja Peruuta-toiminnoissa.  
  
Microsoft Dynamics NAV 2013 R2:n codeunit uusittiin, koska siitä oli tullut hyvin suuri, noin 7 600 koodiriviä. Arkkitehtuuri muutettiin ja codeunitista tehtiin yksinkertaisempi ja ylläpidettävämpi. Tässä ohjeessa kuvaillaan muutokset ja tiedot, joita tarvitset päivitystä varten.  
  
## <a name="old-architecture"></a>Vanha arkkitehtuuri
Vanhassa arkkitehtuurissa oli seuraavat ominaisuudet:  
  
* Yleisten muuttujien käyttö oli laajaa, mikä lisäsi piilotettujen virheiden mahdollisuutta, jos muuttujia käytettiin väärässä laajuudessa.  
* Moni proseduuri oli pitkä (yli 100 riviä), mikä lisäsi myös ns. Cyclomatic Complexityn suuruutta (paljon CASE, REPEAT, IF -lauseita) ja teki koodista erittäin vaikean lukea ja ylläpitää.  
* Useita proseduureja, joita käytettiin vain paikallisesti ja jotka oli tarkoitettu vain paikallisesti käytettäviksi, ei ollut merkitty paikallisiksi.  
* Suurimmalla osalla proseduureista ei ole parametreja eikä käytettyjä yleisiä muuttujia. Osa käytti parametreja ja korvasi yleisiä muuttujia paikallisilla.  
* Kirjanpitotilien hakujen koodikuvioita ja kirjanpito- ja ALV-tapahtumien luontia ei ole standardoitu ja ne vaihtelevat paikasta toiseen. Lisäksi oli paljon päällekkäisiä koodeja sekä asiakas- ja toimittajakoodien välisiä symmetriakatkoksia.  
* Suuri osa codeunitin 12 koodista, noin 30 prosenttia, liittyy maksualennus- ja toleranssilaskelmiin, vaikka useissa maissa tai alueilla näitä ominaisuuksia ei tarvita.  
* Kirjaus, kohdista, peruuta kohdistus, peruuta, maksualennus ja toleranssi sekä vaihtokurssin muutos on liitetty yhteen codeunitissa 12 yleisten muuttujien pitkää listaa käyttäen.  
  
### <a name="new-architecture"></a>Uusi arkkitehtuuri
[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa codeunit 12 on saanut seuraavia parannuksia:  
  
* Codeunit 12 on jaettu pienempiin osiin (kaikissa alle 100 koodiriviä).  
* Kirjanpitotilien hakujen vakiomallit on toteutettu käyttämällä kirjausryhmä-taulukoiden apufunktioita.  
* Kirjausohjelmakehys on toteutettu tapahtumien aloituksen ja lopetuksen hallintaan sekä eristämään luonti kirjanpidosta ja ALV-tapahtumista, ALV-muutosten keräämiseen ja lisävaluutan summien laskemista varten.  
* Koodin kopiointi on poistettu.  
* Monet aputoiminnot on siirretty vastaaviin asiakkaan ja toimittajan tapahtumataulukoihin.  
* Yleisten muuttujien käyttö on minimoitu, jotta jokainen toimintosarja käyttää parametreja ja kapseloi oman sovelluslogiikkansa.  
  
## <a name="see-also"></a>Katso myös

[Rakenteen tiedot: Kirjausliittymän rakenne](design-details-posting-interface-structure.md)  
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)  
[Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
