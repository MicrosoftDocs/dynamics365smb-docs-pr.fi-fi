---
title: 'Rakennetiedot – Koodiyksikön 12 muutokset: Päiväkirjakirjausten menettelytapojen muutokset | Microsoft Docs'
description: Seuraavat muutokset on toteutettu tässä Business Central -versiossa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 99df25e15422755b66ec5b8be7388c9677f7b374
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917474"
---
# <a name="codeunit-12-changes-changes-in-general-journal-post-procedures"></a>Koodiyksikön 12 muutokset: Päiväkirjakirjausten menettelytapojen muutokset
Seuraavat muutokset on toteutettu tässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentti**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Päivitetty|  
|RunWithCheck|RunWithCheck|Päivitetty|  
|RunWithoutCheck|RunWithoutCheck|Päivitetty|  
|Code|Code|Päivitetty|  
||PostGenJnlLine|Lisätty|  
||InitAmounts|Lisätty|  
||InitLastDocDate|Lisätty|  
|InitVAT|InitVAT|Päivitetty|  
|PostVAT|PostVAT|Päivitetty|  
|InsertVAT|InsertVAT|Päivitetty|  
|SummarizeVAT|SummarizeVAT|Päivitetty|  
|InsertSummarizedVAT|InsertSummarizedVAT|Päivitetty|  
|PostGLAcc|PostGLAcc|Päivitetty|  
|PostCust|PostCust|Päivitetty|  
|PostVend|PostVend|Päivitetty|  
|PostBankAcc|PostBankAcc|Päivitetty|  
|PostFixedAsset|PostFixedAsset|Päivitetty|  
|PostICPartner|PostICPartner|Päivitetty|  
|InitCodeUnit|StartPosting|Päivitetty|  
||ContinuePosting|Lisätty|  
|FinishCodeunit|FinishPosting|Päivitetty|  
||PostUnrealizedVAT|Lisätty|  
||CheckPostUnrealizedVAT|Lisätty|  
||ExchangeAccounts|Lisätty|  
|InitGLEntry|InitGLEntry|Päivitetty|  
||InitGLEntryVAT|Lisätty|  
||InitGLEntryVATCopy|Lisätty|  
|InsertGLEntry|InsertGLEntry|Päivitetty|  
||CreateGLEntry|Lisätty|  
||CreateGLEntryBalAcc|Lisätty|  
||CreateGLEntryVAT|Lisätty|  
||CreateGLEntryVATCollectAdj|Lisätty|  
||CreateGLEntryFromVATEntry|Lisätty|  
||UpdateCheckAmounts|Lisätty|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Päivitetty|  
||CalcPmtDiscPossible|Lisätty|  
||CalcPmtTolerancePossible|Lisätty|  
|CalcPmtTolerance|CalcPmtTolerance|Päivitetty|  
|CalcPmtDisc|CalcPmtDisc|Päivitetty|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Päivitetty|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Päivitetty|  
||CalcPmtDiscVATBases|Lisätty|  
||CalcPmtDiscVATAmounts|Lisätty|  
||InsertPmtDiscVATForGLEntry|Lisätty|  
||InsertPmtDiscVATForGLEntry|Lisätty|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Päivitetty|  
|FindAmtForAppln|FindAmtForAppln|Päivitetty|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Päivitetty|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Päivitetty|  
|CalcApplication|CalcApplication|Päivitetty|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Lisätty|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Siirretty taulukkoon 383 Yks.koht. CV-tapaht. puskuri|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Siirretty taulukkoon 383 Yks.koht. CV-tapaht. puskuri|  
|InsertDtldCustLedgEntry|InsertDtldCustLedgEntry|Siirretty taulukkoon 383 Yks.koht. CV-tapaht. puskuri|  
||InitBankAccLedgEntry|Lisätty|  
||InitCheckLedgEntry|Lisätty|  
||InitCustLedgEntry|Lisätty|  
||InitVendLedgEntry|Lisätty|  
||InsertDtldCustLedgEntry|Lisätty|  
||InsertDtldVendLedgEntry|Lisätty|  
|CustUnrealizedVAT|CustUnrealizedVAT|Päivitetty|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Päivitetty|  
||PrepareTempCustLedgEntry|Lisätty|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Päivitetty|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Siirretty taulukkoon 21 Asiakastapahtuma|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Päivitetty|  
||PostDtldCustLedgEntry|Lisätty|  
||PostDtldCustLedgEntryUnapply|Lisätty|  
||GetDtldCustLedgEntryAccNo|Lisätty|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Siirretty taulukkoon 379 Yksit.kohtainen as.tapahtuma|  
|AutoEntrForDtldCustLedgEntries||Refaktoroitu kohteeseen PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Siirretty taulukkoon 379 Yksit.kohtainen as.tapahtuma|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Päivitetty|  
||PrepareTempVendLedgEntry|Lisätty|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Päivitetty|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Päivitetty|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Siirretty taulukkoon 25 Toimittajatapahtuma|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Päivitetty|  
||PostDtldVendLedgEntry|Lisätty|  
||PostDtldVendLedgEntryUnapply|Lisätty|  
||GetDtldVendLedgEntryAccNo|Lisätty|  
||PostDtldCVLedgEntry|Lisätty|  
||PostDtldCustVATAdjustment|Lisätty|  
||PostDtldVendVATAdjustment|Lisätty|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Siirretty taulukkoon 380 Yks.koht. toimit. tapahtuma|  
|AutoEntrForDtldVendLedgEntries||Refaktoroitu kohteeseen PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Siirretty taulukkoon 380 Yks.koht. toimit. tapahtuma|  
|VendUnrealizedVAT|VendUnrealizedVAT|Päivitetty|  
||PostUnrealVATEntry|Lisätty|  
||PostApply|Lisätty|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Päivitetty|  
||PostUnapply|Lisätty|  
||InsertDtldCustLedgEntry|Lisätty|  
||InsertDtldVendLedgEntryUnapply|Lisätty|  
||InsertTempVATEntry|Lisätty|  
||ProcessTempVATEntry|Lisätty|  
||UpdateCustLedgEntry|Lisätty|  
||UpdateVendLedgEntry|Lisätty|  
|UpdateCalcInterest|UpdateCalcInterest|Päivitetty|  
|UpdateCalcInterest2|UpdateCalcInterest2|Päivitetty|  
|GLCalcAddCurrency|GLCalcAddCurrency|Päivitetty|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Päivitetty|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Päivitetty|  
|CalcAddCurrFactor||Poistettu|  
|GetCurrencyExchRate|GetCurrencyExchRate|Päivitetty|  
|ExchAmount|ExchangeAmount|Siirretty taulukkoon 330 Valuutan vaihtokurssi|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Päivitetty|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Päivitetty|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Päivitetty|  
|CheckCalcPmtDisc||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscCVCust||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscCust||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscGenJnlCust||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscCVVend||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscVend||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|CheckCalcPmtDiscGenJnlVend||Siirretty koodiyksikön 426 maksutoleranssin hallinta|  
|Reverse|Reverse|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ReverseVAT|ReverseVAT|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|SetReversalDescription|SetReversalDescription|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Siirretty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
||CheckDimComb|Lisätty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
||CopyCustLedgEntry|Lisätty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
||CopyVendLedgEntry|Lisätty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
||CopyBankAccLedgEntry|Lisätty Codeunitiin 17 yleinen päiväkirja - käänteinen kirjaus|  
|HandlDtlAddjustment|HandleDtldAdjustment|Päivitetty|  
|CollectAddjustment|CollectAdjustment|Päivitetty|  
|SetOverDimErr|SetOverDimErr|Päivitetty|  
|PostJob|PostJob|Päivitetty|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Päivitetty|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Päivitetty|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Päivitetty|  
|ABSMin|ABSMin|Päivitetty|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Päivitetty|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Päivitetty|  
|CalculateCurrentBalance|CalculateCurrentBalance|Päivitetty|  
|IncludeVATAmount||Siirretty taulukkoon 81 yleinen päiväkirjan rivi|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Päivitetty|  
||TotalVATAmountOnJnlLines|Lisätty|  
||SetGLRegReverse|Lisätty|  
||GetGLSetup|Lisätty|  
||ReadGLSetup|Lisätty|  
||CheckSalesExtDocNo|Lisätty|  
||CheckPurchExtDocNo|Lisätty|  
||CheckGLAccDimError|Lisätty|  
||GetCurrency|Lisätty|  
||PostDtldAdjustment|Lisätty|  
||GetNextEntryNo|Lisätty|  
||GetNextTransactionNo|Lisätty|  
||GetNextVATEntryNo|Lisätty|  
||IncrNextVATEntryNo|Lisätty|  
||IsNotPayment|Lisätty|  
||IsTempGLEntryBufEmpty|Lisätty|  
||IsVATAdjustment|Lisätty|  
||IsVATExcluded|Lisätty|  
||UpdateDimensions|Lisätty|  
||UpdateDimensionsFromCustLedgEntry|Lisätty|  
||UpdateDimensionsFromVendLedgEntry|Lisätty|  
||UpdateTotalAmounts|Lisätty|  
||CreateGLEntriesForTotalAmounts|Lisätty|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Koodiyksikön 12 muutokset: Yleisten muuttujien linkitys yleisen päiväkirjan kirjausriviin](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)
