---
title: Rakenteen tiedot – Kirjausohjelman rakenne | Microsoft Docs
description: Kirjausliittymä ja tietyt muut funktiot koodiyksikkö 12:ssa käyttävät kirjausohjelman toimintoja pääkirjanpidon tapahtumien ja ALV-tapahtumatietueiden valmisteluun ja lisäykseen. Kirjausohjelma vastaa myös kirjanpitorekisterin luomisesta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 80482301e9a6a5c30c631ffa936517919bbeb848
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214926"
---
# <a name="design-details-posting-engine-structure"></a>Rakenteen tiedot: Kirjausohjelman rakenne
Kirjausliittymä ja tietyt muut funktiot koodiyksikkö 12:ssa käyttävät kirjausohjelman toimintoja pääkirjanpidon tapahtumien ja ALV-tapahtumatietueiden valmisteluun ja lisäykseen. Kirjausohjelma vastaa myös kirjanpitorekisterin luomisesta.  
  
 Seuraavan taulukon toiminnot muodostavat vakioalustan, jonka pohjalta suunnitellaan kirjausproseduureja (esimerkiksi Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry ja Reverse). Lisäksi ne tarjoavat yksinomaisen käyttöoikeuden taulukkoon 17, KP-tapahtuma.  
  
|Rutiini|Description|  
|-------------|---------------------------------------|  
|StartPosting|Alustaa kirjauspuskurin TempGLEntryBuf, lukitsee G/L Entry- ja VAT Entry -taulukot ja alustaa kirjanpitojakson, KP-rekisterin ja vaihtokurssin. Tulisi kutsua vain kerran, sitten NextEntryNo on 0.|  
|ContinuePosting|Tarkistaa ja kirjaa edellisen tapahtuman lisäysksen ei-realisoitununeen ALV:n (NextTransactionNo) ja valmistelee seuraavan rivin kirjauksen.|  
|FinishPosting|Päättää kirjauksen lisäämällä kirjanpitotapahtumat väliaikaisesta puskurista tietokantataulukkoon. Käytetään aina StartPosting-rutiinin kanssa. Tarkistaa mahdolliset epäyhtenäisyydet.|  
|InitGLEntry|Käytetään alustamaan uusi KP-tapahtuma yleisen päiväkirjan riville. Palauttaa GLEntry:n parametrina.|  
|InitGLEntryVAT|Sama kuin InitGLEntry, mutta määrittää myös vastatilin numeron ja SummarizeVAT-tiedon.|  
|InitGLEntryVATCopy|Samanlainen kuin InitGLEntryVAT, mutta myös kopioi kirjausryhmien tiedot ALV-tapahtumista ennen SummarizeVAT-toimintoa.|  
|InsertGLEntry|Ainoa toiminto, joka lisää KP-tapahtuman yleiseen TempGLEntryBuf-taulukkoon. Käytä aina tätä toimintoa lisäämiseen.|  
|CreateGLEntry|Suorittaa InitGLEntry-funktion, määrittää lisävaluutan summan ja sitten suorittaa InsertGLEntry-funktion. Korvaa useita koodirivejä yhdellä funktiokutsulla.|  
|CreateGLEntryBalAcc|Sama kuin CreateGLEntry, mutta myös määrittää Vastatilin tyyppi- ja Vastatilin nro-kentät.|  
|CreateGLEntryVAT|Sama kuin CreateGLEntry, mutta kirjausryhmien lisäkäsittely ja tallennus väliaikaiseen ALV-puskuriin:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Sama kuin CreateGLEntry, mutta muutosten lisäkokoelmalla ja tallennus väliaikaiseen ALV-puskuriin:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Sama kuin CreateGLEntry, mutta myös kopioi kirjausryhmät ALV-tapahtumasta.|  
  
## <a name="see-also"></a>Katso myös  
 [Rakenteen tiedot: Kirjausliittymän rakenne](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]