---
title: 'Muutokset codeunitissa 12: Yleisten muuttujien yhdistäminen kirjaukselle'
description: Aiemmissa versioissa codeunitia 12 muutettiin yleisen päiväkirjan kirjaamisen suorituskyvyn parantamiseksi. Lue lisää globaalien muuttujien muutoksista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: bb041e7be2a0c644d1c19e34b892bd9480123734
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390522"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Codeunitin 12 historialliset muutokset: Yleisten muuttujien linkitys yleisen päiväkirjan kirjausriviin

Seuraavat muutokset on toteutettu [!INCLUDE [navnow_md](includes/navnow_md.md)] -versioissa.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentti**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Muuttumaton|  
|SalesSetup@1010 : Record 311;||Puutettu paikalliseksi|  
|PurchSetup@1011 : Record 312;||Puutettu paikalliseksi|  
|AccountingPeriod@1012 : Record 50;||Puutettu paikalliseksi|  
|GLAcc@1013 : Record 15;||Puutettu paikalliseksi|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Nimetty uudelleen|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Nimetty uudelleen|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Muuttumaton|  
|OrigGLEntry@1017 : Record 17;||Poistettu|  
|VATPostingSetup@1019 : Record 325;||Puutettu paikalliseksi|  
|Cust@1020 : Record 18;||Puutettu paikalliseksi|  
|Vend@1021 : Record 23;||Puutettu paikalliseksi|  
|GenJnlLine@1022 : Record 81;||Puutettu paikalliseksi|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Muuttumaton|  
|CustPostingGr@1030 : Record 92;||Puutettu paikalliseksi|  
|VendPostingGr@1031 : Record 93;||Puutettu paikalliseksi|  
|Currency@1032 : Record 4;||Puutettu paikalliseksi|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Muuttumaton|  
|ApplnCurrency@1034 : Record 4;||Puutettu paikalliseksi|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Muuttumaton|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Muuttumaton|  
|BankAcc@1039 : Record 270;||Puutettu paikalliseksi|  
|BankAccLedgEntry@1040 : Record 271;||Puutettu paikalliseksi|  
|CheckLedgEntry@1041 : Record 272;||Puutettu paikalliseksi|  
|CheckLedgEntry2@1042 : Record 272;||Puutettu paikalliseksi|  
|BankAccPostingGr@1043 : Record 277;||Puutettu paikalliseksi|  
|GenJnlTemplate@1044 : Record 80;||Puutettu paikalliseksi|  
|TaxJurisdiction@1045 : Record 320;||Puutettu paikalliseksi|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Muuttumaton|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Puutettu paikalliseksi|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Muuttumaton|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Muuttumaton|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Muuttumaton|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Muuttumaton|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Siirretty codeunit17:ään|  
|CostAccSetup@1092 : Record 1108;||Puutettu paikalliseksi|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Muuttumaton|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Puutettu paikalliseksi|  
|FAJnlPostLine@1050 : Codeunit 5632;||Puutettu paikalliseksi|  
|SalesTaxCalculate@1051 : Codeunit 398;||Puutettu paikalliseksi|  
|GenJnlApply@1052 : Codeunit 225;||Puutettu paikalliseksi|  
|DimMgt@1053 : Codeunit 408;||Puutettu paikalliseksi|  
|JobPostLine@1028 : Codeunit 1001;||Puutettu paikalliseksi|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Puutettu paikalliseksi|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Lisätty|  
||AddCurrencyCode@1117 : Code[10];|Lisätty|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Muuttumaton|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Muuttumaton|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Muuttumaton|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Muuttumaton|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Muuttumaton|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Muuttumaton|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Muuttumaton|  
|SalesTaxBaseAmount@1061 : Decimal;||Puutettu paikalliseksi|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Muuttumaton|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Muuttumaton|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Muuttumaton|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Muuttumaton|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Muuttumaton|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Muuttumaton|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Muuttumaton|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Muuttumaton|  
|InsertedTempGLEntryVAT@1068 : kokonaisluku;|InsertedTempGLEntryVAT@1027 : Integer;|Muuttumaton|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Muuttumaton|  
|LastLineNo@1070 : Integer;||Poistettu|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Muuttumaton|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Muuttumaton|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Muuttumaton|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Muuttumaton|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Muuttumaton|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Muuttumaton|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Muuttumaton|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Muuttumaton|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Muuttumaton|  
|AllApplied@1081 : Boolean;||Puutettu paikalliseksi|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Muuttumaton|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Muuttumaton|  
|Prepayment@1037 : Boolean;||Poistettu|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Muuttumaton|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Muuttumaton|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Muuttumaton|  
||GLSetupRead@1015 : Boolean;|Lisätty|  
||AmountRoundingPrecision@1012 : Decimal;|Lisätty|  
||CrCardTransactionEntryNo@1013 : Integer;|Lisätty|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Codeunitin 12 muutokset: Päiväkirjakirjausten menettelytapojen muutokset](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]