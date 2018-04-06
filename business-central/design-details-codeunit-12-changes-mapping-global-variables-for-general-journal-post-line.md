---
title: "Rakennetiedot – Koodiyksikön 12 muutokset: Yleisten muuttujien linkitys yleisen päiväkirjan kirjausriviin | Microsoft Docs"
description: "Seuraavat muutokset on toteutettu tässä Business Central -versiossa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: aae8b02b95d3e385030610533f4b1b7f04602d5e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Koodiyksikön 12 muutokset: Yleisten muuttujien linkitys yleisen päiväkirjan kirjausriviin
Seuraavat muutokset on toteutettu tässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentti**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009: Tietue 98;|GLSetup@1009: Tietue 98;|Muuttumaton|  
|SalesSetup@1010: Tietue 311;||Puutettu paikalliseksi|  
|PurchSetup@1011: Tietue 312;||Puutettu paikalliseksi|  
|AccountingPeriod@1012: Tietue 50;||Puutettu paikalliseksi|  
|GLAcc@1013: Tietue 15;||Puutettu paikalliseksi|  
|GLEntry@1014: Tietue 17;|GlobalGLEntry@1014: Tietue 17;|Nimetty uudelleen|  
|GLEntryTmp@1015: TILAPÄINEN Tietue 17;|TempGLEntryBuf@1010: TILAPÄINEN Tietue 17;|Nimetty uudelleen|  
|TempGLEntryVAT@1016: TILAPÄINEN Tietue 17;|TempGLEntryVAT@1016: TILAPÄINEN Tietue 17;|Muuttumaton|  
|OrigGLEntry@1017: Tietue 17;||Poistettu|  
|VATPostingSetup@1019: Tietue 325;||Puutettu paikalliseksi|  
|Cust@1020: Tietue 18;||Puutettu paikalliseksi|  
|Vend@1021: Tietue 23;||Puutettu paikalliseksi|  
|GenJnlLine@1022: Tietue 81;||Puutettu paikalliseksi|  
|GLReg@1029: Tietue 45;|GLReg@1029: Tietue 45;|Muuttumaton|  
|CustPostingGr@1030: Tietue 92;||Puutettu paikalliseksi|  
|VendPostingGr@1031: Tietue 93;||Puutettu paikalliseksi|  
|Currency@1032: Tietue 4;||Puutettu paikalliseksi|  
|AddCurrency@1033: Tietue 4;|AddCurrency@1033: Tietue 4;|Muuttumaton|  
|ApplnCurrency@1034: Tietue 4;||Puutettu paikalliseksi|  
|CurrExchRate@1035: Tietue 330;|CurrExchRate@1035: Tietue 330;|Muuttumaton|  
|VATEntry@1038: Tietue 254;|VATEntry@1038: Tietue 254;|Muuttumaton|  
|BankAcc@1039: Tietue 270;||Puutettu paikalliseksi|  
|BankAccLedgEntry@1040: Tietue 271;||Puutettu paikalliseksi|  
|CheckLedgEntry@1041: Tietue 272;||Puutettu paikalliseksi|  
|CheckLedgEntry2@1042: Tietue 272;||Puutettu paikalliseksi|  
|BankAccPostingGr@1043: Tietue 277;||Puutettu paikalliseksi|  
|GenJnlTemplate@1044: Tietue 80;||Puutettu paikalliseksi|  
|TaxJurisdiction@1045: Tietue 320;||Puutettu paikalliseksi|  
|TaxDetail@1046: Tietue 322;|TaxDetail@1046: Tietue 322;|Muuttumaton|  
|FAGLPostBuf@1047: TILAPÄINEN Tietue 5637;||Puutettu paikalliseksi|  
|UnrealizedCustLedgEntry@1084: Tietue 21;|UnrealizedCustLedgEntry@1084: Tietue 21;|Muuttumaton|  
|UnrealizedVendLedgEntry@1085: Tietue 25;|UnrealizedVendLedgEntry@1085: Tietue 25;|Muuttumaton|  
|GLEntryVATEntryLink@1087: Tietue 253;|GLEntryVATEntryLink@1087: Tietue 253;|Muuttumaton|  
|TempVATEntry@1088: TILAPÄINEN Tietue 254;|TempVATEntry@1088: TILAPÄINEN Tietue 254;|Muuttumaton|  
|ReversedGLEntryTemp@1089: TILAPÄINEN Tietue 17;||Siirretty koodiyksikkö17:ään|  
|CostAccSetup@1092: Tietue 1108;||Puutettu paikalliseksi|  
|GenJnlCheckLine@1048: Koodiyksikkö 11;|GenJnlCheckLine@1001: Koodiyksikkö 11;|Muuttumaton|  
|ExchAccGLJnlLine@1049 : Koodiyksikkö 366;||Puutettu paikalliseksi|  
|FAJnlPostLine@1050: Koodiyksikkö 5632;||Puutettu paikalliseksi|  
|SalesTaxCalculate@1051: Koodiyksikkö 398;||Puutettu paikalliseksi|  
|GenJnlApply@1052: Koodiyksikkö 225;||Puutettu paikalliseksi|  
|DimMgt@1053: Koodiyksikkö 408;||Puutettu paikalliseksi|  
|JobPostLine@1028: Koodiyksikkö 1001;||Puutettu paikalliseksi|  
|TransferGlEntriesToCA@1091: Koodiyksikkö 1105;||Puutettu paikalliseksi|  
||PaymentToleranceMgt@1002: Koodiyksikkö 426;|Lisätty|  
||AddCurrencyCode@1117: Koodi[10];|Lisätty|  
|FiscalYearStartDate@1054 : Pvm;|FiscalYearStartDate@1011 : Pvm;|Muuttumaton|  
|NextEntryNo@1055 : Kokonaisluku;|NextEntryNo@1022 : Kokonaisluku;|Muuttumaton|  
|BalanceCheckAmount@1056 : Desimaali;|BalanceCheckAmount@1056 : Desimaali;|Muuttumaton|  
|BalanceCheckAmount2@1057 : Desimaali;|BalanceCheckAmount2@1057 : Desimaali;|Muuttumaton|  
|BalanceCheckAddCurrAmount@1058 : Desimaali;|BalanceCheckAddCurrAmount@1058 : Desimaali;|Muuttumaton|  
|BalanceCheckAddCurrAmount2@1059 : Desimaali;|BalanceCheckAddCurrAmount2@1059 : Desimaali;|Muuttumaton|  
|CurrentBalance@1060 : Desimaali;|CurrentBalance@1060 : Desimaali;|Muuttumaton|  
|SalesTaxBaseAmount@1061 : Desimaali;||Puutettu paikalliseksi|  
|TotalAddCurrAmount@1062 : Desimaali;|TotalAddCurrAmount@1062 : Desimaali;|Muuttumaton|  
|TotalAmount@1063 : Desimaali;|TotalAmount@1063 : Desimaali;|Muuttumaton|  
|UnrealizedRemainingAmountCust@1086 : Desimaali;|UnrealizedRemainingAmountCust@1086 : Desimaali;|Muuttumaton|  
|UnrealizedRemainingAmountVend@1074 : Desimaali;|UnrealizedRemainingAmountVend@1074 : Desimaali;|Muuttumaton|  
|NextVATEntryNo@1064 : Kokonaisluku;|NextVATEntryNo@1064 : Kokonaisluku;|Muuttumaton|  
|FirstNewVATEntryNo@1065 : Kokonaisluku;|FirstNewVATEntryNo@1065 : Kokonaisluku;|Muuttumaton|  
|NextTransactionNo@1066 : Kokonaisluku;|NextTransactionNo@1066 : Kokonaisluku;|Muuttumaton|  
|NextConnectionNo@1067 : Kokonaisluku;|NextConnectionNo@1067 : Kokonaisluku;|Muuttumaton|  
|InsertedTempGLEntryVAT@1068 : Kokonaisluku;|InsertedTempGLEntryVAT@1027 : Kokonaisluku;|Muuttumaton|  
|LastDocNo@1069: Koodi[20];|LastDocNo@1023: Koodi[20];|Muuttumaton|  
|LastLineNo@1070 : Kokonaisluku;||Poistettu|  
|LastDate@1071 : Pvm;|LastDate@1021 : Pvm;|Muuttumaton|  
|LastDocType@1072 : ' ,lasku, maksu, hyvityslasku, viivästyskululasku, muistutus';|LastDocType@1025 : ' ,lasku, maksu, hyvityslasku, viivästyskululasku, muistutus';|Muuttumaton|  
|NextCheckEntryNo@1073 : Kokonaisluku;|NextCheckEntryNo@1028 : Kokonaisluku;|Muuttumaton|  
|AddCurrGLEntryVATAmt@1075 : Desimaali;|AddCurrGLEntryVATAmt@1017 : Desimaali;|Muuttumaton|  
|CurrencyDate@1076 : Pvm;|CurrencyDate@1020 : Pvm;|Muuttumaton|  
|CurrencyFactor@1077 : Desimaali;|CurrencyFactor@1019 : Desimaali;|Muuttumaton|  
|UseCurrFactorOnly@1078 : Totuusarvo;|UseCurrFactorOnly@1078 : Totuusarvo;|Muuttumaton|  
|NonAddCurrCodeOccured@1079 : Totuusarvo;|NonAddCurrCodeOccured@1079 : Totuusarvo;|Muuttumaton|  
|FADimAlreadyChecked@1080 : Totuusarvo;|FADimAlreadyChecked@1080 : Totuusarvo;|Muuttumaton|  
|AllApplied@1081 : Totuusarvo;||Puutettu paikalliseksi|  
|OverrideDimErr@1018 : Totuusarvo;|OverrideDimErr@1018 : Totuusarvo;|Muuttumaton|  
|JobLine@1036 : Totuusarvo;|JobLine@1036 : Totuusarvo;|Muuttumaton|  
|Prepayment@1037 : Totuusarvo;||Poistettu|  
|CheckUnrealizedCust@1082 : Totuusarvo;|CheckUnrealizedCust@1082 : Totuusarvo;|Muuttumaton|  
|CheckUnrealizedVend@1083 : Totuusarvo;|CheckUnrealizedVend@1083 : Totuusarvo;|Muuttumaton|  
|GLEntryNo@1090 : Kokonaisluku;|GLEntryNo@1026 : Kokonaisluku;|Muuttumaton|  
||GLSetupRead@1015 : Totuusarvo;|Lisätty|  
||AmountRoundingPrecision@1012 : Desimaali;|Lisätty|  
||CrCardTransactionEntryNo@1013 : Kokonaisluku;|Lisätty|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Koodiyksikön 12 muutokset: Päiväkirjakirjausten menettelytapojen muutokset](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

