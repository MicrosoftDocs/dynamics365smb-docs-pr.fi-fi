---
title: Integroinnin päivittäminen Dynamics 365 Salesissa
description: Opi siirtämään Dynamics 365 Business Centralin ja Dynamics 365 Salesin välinen integrointi uusimpaan versioon.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922365"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="e9c3d-103">Integroinnin päivittäminen Dynamics 365 Salesissa</span><span class="sxs-lookup"><span data-stu-id="e9c3d-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e9c3d-104">voidaan integroida [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="e9c3d-105">Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="e9c3d-106">Lisätietoja on kohdassa [Integroiminen Common Data Service -palvelun kanssa](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="e9c3d-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="e9c3d-107">Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="e9c3d-108">Jos päivität [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tai poistat [!INCLUDE[crm_md](includes/crm_md.md)]-integroinnin käytöstä, voit ottaa sen uudelleen käyttöön muodostamalla yhteyden [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="e9c3d-109">Jos uudelleenyhdistämisessä käytetään [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="e9c3d-110">Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="e9c3d-111">Yhteyden päivittäminen niin, että se käyttää Common Data Service -sovellusta</span><span class="sxs-lookup"><span data-stu-id="e9c3d-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="e9c3d-112">Avaa **Microsoft Dynamics 365 -yhteyden määritys** -sivu, valitse **Ota käyttöön** -valitsin ja poista käytöstä olemassa oleva [!INCLUDE[crm_md](includes/crm_md.md)]-yhteys.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="e9c3d-113">Avaa **Common Data Service -yhteyden määritys** -sivu ja valitse **Ota käyttöön** -valitsin, jos haluat ottaa yhteyden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="e9c3d-114">Kun olet ottanut CDS-yhteyden käyttöön, Business Centralin CDS-perusintegrointiratkaisu otetaan käyttöön Common Data Service -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="e9c3d-115">Microsoft Dynamics 365 Business Centralin integrointiratkaisun asennuksen poistaminen Dynamics 365 Salesista.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales.</span></span> <span data-ttu-id="e9c3d-116">Lisätietoja on kohdassa [Ratkaisun asennuksen poistaminen tai sen poistaminen kokonaan](/powerapps/developer/common-data-service/uninstall-delete-solution).</span><span class="sxs-lookup"><span data-stu-id="e9c3d-116">For more information, see [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution).</span></span> 

4. <span data-ttu-id="e9c3d-117">Valitse **Microsoft Dynamics 365 -yhteyden määritys** -sivulla **Ota käyttöön** -valitsin, jos haluat ottaa käyttöön[!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-117">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enable** toggle to connect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="e9c3d-118">Kun olet ottanut Sales-yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön Salesissa.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-118">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="e9c3d-119">Tämä mahdollistaa integroinnin [!INCLUDE[crm_md](includes/crm_md.md)]-kohtaisten entiteettien kanssa. Näitä ovat esimerkiksi myyntitilaukset, tarjoukset ja laskut.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-119">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="e9c3d-120">Valitse **Sales-yhteyden määritys** -sivulla **Käytä oletussynkronoinnin määritystä**, jos haluat käynnistää integrointitaulukon yhdistämismääritykset [!INCLUDE[crm_md](includes/crm_md.md)]-sovellusta varten.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="e9c3d-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e9c3d-121">See Also</span></span>
[<span data-ttu-id="e9c3d-122">Dynamics 365 Sales -integrointi</span><span class="sxs-lookup"><span data-stu-id="e9c3d-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="e9c3d-123">Integrointi Common Data Servicein kanssa</span><span class="sxs-lookup"><span data-stu-id="e9c3d-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)