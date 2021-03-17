---
title: Integroinnin päivittäminen Dynamics 365 Salesissa
description: Opi siirtämään Dynamics 365 Business Centralin ja Dynamics 365 Salesin välinen integrointi uusimpaan versioon.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 69ffe6cea05cc28d1950481a07b064a3365f404e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386697"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="534a3-103">Integroinnin päivittäminen Dynamics 365 Salesissa</span><span class="sxs-lookup"><span data-stu-id="534a3-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="534a3-104">voidaan integroida [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="534a3-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="534a3-105">Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="534a3-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="534a3-106">Lisätietoja on kohdassa [Integroiminen Dataverse -palvelun kanssa](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="534a3-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="534a3-107">Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="534a3-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="534a3-108">Jos päivität [!INCLUDE[prod_short](includes/prod_short.md)]:n tai poistat [!INCLUDE[crm_md](includes/crm_md.md)]-integroinnin käytöstä, voit ottaa sen uudelleen käyttöön muodostamalla yhteyden [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="534a3-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="534a3-109">Jos uudelleenyhdistämisessä käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan.</span><span class="sxs-lookup"><span data-stu-id="534a3-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="534a3-110">Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="534a3-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="534a3-111">Yhteyden päivittäminen niin, että se käyttää Dataverse -sovellusta</span><span class="sxs-lookup"><span data-stu-id="534a3-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="534a3-112">Avaa **Microsoft Dynamics 365 -yhteyden määritys** -sivu ja ota pois käytöstä **Käytössä**-valitsin , jotta voit katkaista [!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden.</span><span class="sxs-lookup"><span data-stu-id="534a3-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="534a3-113">Avaa **Dataverse -yhteyden määritys** -sivu ja valitse **Käytössä**-valitsin, jos haluat ottaa [!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteyden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="534a3-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="534a3-114">Kun olet ottanut yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön Dataversessa.</span><span class="sxs-lookup"><span data-stu-id="534a3-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="534a3-115">Valitse **Ota integraatioratkaisu uudelleen käyttöön**, jos haluat asentaa Business Centralin integrointiratkaisun uudelleen.</span><span class="sxs-lookup"><span data-stu-id="534a3-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="534a3-116">Valitse **Microsoft Dynamics 365 -yhteyden määritys** -sivulla **Käytössä** -valitsin, jos haluat muodostaa [!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden uudelleen.</span><span class="sxs-lookup"><span data-stu-id="534a3-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="534a3-117">Kun olet ottanut yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]ssa.</span><span class="sxs-lookup"><span data-stu-id="534a3-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="534a3-118">Tämä mahdollistaa integroinnin [!INCLUDE[crm_md](includes/crm_md.md)]-kohtaisten taulukoiden kanssa. Näitä ovat esimerkiksi myyntitilaukset, tarjoukset ja laskut.</span><span class="sxs-lookup"><span data-stu-id="534a3-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="534a3-119">Valitse **Ota integraatioratkaisu uudelleen käyttöön**, jos haluat asentaa Business Centralin integrointiratkaisun uudelleen.</span><span class="sxs-lookup"><span data-stu-id="534a3-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="534a3-120">Valitse **Sales-yhteyden määritys** -sivulla **Käytä oletussynkronoinnin määritystä**, jos haluat käynnistää integrointitaulukon yhdistämismääritykset [!INCLUDE[crm_md](includes/crm_md.md)]-sovellusta varten.</span><span class="sxs-lookup"><span data-stu-id="534a3-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="534a3-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="534a3-121">See Also</span></span>
[<span data-ttu-id="534a3-122">Dynamics 365 Sales -integrointi</span><span class="sxs-lookup"><span data-stu-id="534a3-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="534a3-123">Integrointi Microsoft Dataversein kanssa</span><span class="sxs-lookup"><span data-stu-id="534a3-123">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]