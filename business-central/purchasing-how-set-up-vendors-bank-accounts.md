---
title: Toimittajan pankkitilin määrittäminen
description: Tutustu pankkitilien (yhteystiedot ja SWIFT- ja IBAN-koodit mukaan luettuna) määrittämiseen toimittajakorteille Business Centralissa.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: a-reishima
ms.openlocfilehash: 1839f54de2382ad5b7d8b6b936181e105a56e06b
ms.sourcegitcommit: 5560a49ca4ce85fa12e50ed9e14de6d5cba5f5c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2022
ms.locfileid: "9144404"
---
# <a name="set-up-vendor-bank-accounts"></a>Toimittajien pankkitilien määrittäminen

Samalla tavalla kuin voit seurata yrityksesi pankkitapahtumia käyttämällä pankkitietoja [!INCLUDE [prod_short](includes/prod_short.md)]issa voit myös määrittää pankkitietoja toimittajille. Toimittajien pankkitilitiedot voivat yksinkertaistaa maksuja toimittajille, kun niitä käytetään esimeriksi yhdessä [AMC Banking 365 Fundamentals -laajennuksen](ui-extensions-amc-banking.md) tai [Vie maksut pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md) -toiminnon kanssa.

## <a name="add-or-edit-a-vendor-bank-account"></a>Toimittajan pankkitilin lisääminen tai muokkaaminen

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Voit määrittää lisää toimittajan pankkitilejä **Toimittajan pankkitililuettelo** -sivulla.

## <a name="set-up-a-preferred-vendor-bank-account"></a>Ensisijaisen pankkitilin määrittäminen toimittajalle

Jos toimittajalla on vähintään yksi pankkitili ja haluat määrittää ensisijaisen vaihtoehdon maksukirjauskansioriveille, noudata seuraavia ohjeita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Avaa toimittajan kortti.
3. Valitse **Maksut**-pikavälilehden **Ensisijaisen pankkitilin koodi** -kentässä toimittajan oletusarvoinen pankkitili.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md)  
[Käytä AMC Banking 365 Fundamentals -laajennusta](ui-extensions-amc-banking.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
