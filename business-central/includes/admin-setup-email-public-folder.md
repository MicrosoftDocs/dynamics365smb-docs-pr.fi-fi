---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528008"
---
<span data-ttu-id="1b2e8-101">Ennen sähköpostin lokiinkirjauksen määrittämistä Exchange Onlineen on valmisteltava [yleiset kansiot](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span></span> <span data-ttu-id="1b2e8-102">Se voidaan tehdä [Exchangen hallintakeskuksessa](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019) tai käyttämällä [Exchange-palvelimen hallintaliittymää](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span></span>  

> [!TIP]
> <span data-ttu-id="1b2e8-103">Jos haluat käyttää [Exchange-palvelimen hallintaliittymää](/powershell/exchange/exchange-management-shell?view=exchange-ps), [BCTech-säilöön](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging) on julkaistu mallikomentosarja, joka voi toimia mallina komentosarjan määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="1b2e8-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="1b2e8-104">Seuraavassa on luettelossa keskeiset vaiheet sekä linkkejä lisätietoihin.</span><span class="sxs-lookup"><span data-stu-id="1b2e8-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="1b2e8-105">Yleisten kansioiden järjestelmänvalvojan roolin luonti seuraavan taulukon tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="1b2e8-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="1b2e8-106">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="1b2e8-106">Property</span></span>        |<span data-ttu-id="1b2e8-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="1b2e8-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="1b2e8-108">Name</span><span class="sxs-lookup"><span data-stu-id="1b2e8-108">Name</span></span>            |<span data-ttu-id="1b2e8-109">Yleisten kansioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="1b2e8-109">Public Folders Management</span></span> |
  |<span data-ttu-id="1b2e8-110">Valitut roolit</span><span class="sxs-lookup"><span data-stu-id="1b2e8-110">Selected roles</span></span>  |<span data-ttu-id="1b2e8-111">Yleiset kansiot</span><span class="sxs-lookup"><span data-stu-id="1b2e8-111">Public Folders</span></span>            |
  |<span data-ttu-id="1b2e8-112">Valitut jäsenet</span><span class="sxs-lookup"><span data-stu-id="1b2e8-112">Selected members</span></span>|<span data-ttu-id="1b2e8-113">Sen käyttäjätilin sähköposti, jota Business Central käyttää sähköpostin lokiinkirjaustyön suorittamiseen</span><span class="sxs-lookup"><span data-stu-id="1b2e8-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="1b2e8-114">Lisätietoja on kohdassa [Rooliryhmien hallinta](/exchange/permissions/role-groups?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019).</span></span>

- <span data-ttu-id="1b2e8-115">Uuden yleisen kansioin postilaatikon luonti seuraavan taulukon tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="1b2e8-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="1b2e8-116">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="1b2e8-116">Property</span></span>        |<span data-ttu-id="1b2e8-117">Arvo</span><span class="sxs-lookup"><span data-stu-id="1b2e8-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="1b2e8-118">Name</span><span class="sxs-lookup"><span data-stu-id="1b2e8-118">Name</span></span>            |<span data-ttu-id="1b2e8-119">Julkinen postilaatikko</span><span class="sxs-lookup"><span data-stu-id="1b2e8-119">Public MailBox</span></span>            |

  <span data-ttu-id="1b2e8-120">Lisätietoja on kohdassa [Yleisen kansion postilaatikon luonti Exchange Serverissa](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="1b2e8-121">Uusien yleisten kansioiden luominen</span><span class="sxs-lookup"><span data-stu-id="1b2e8-121">Create new public folders</span></span>

  - <span data-ttu-id="1b2e8-122">Luo juuritasolle uusi yleinen kansio, jonka nimi on *Email Logging*, jolloin kansion täydellinen polku on ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="1b2e8-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="1b2e8-123">Luo kaksi alikansiota, jolloin kansioiden täydelliseksi poluksi tulee</span><span class="sxs-lookup"><span data-stu-id="1b2e8-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="1b2e8-124">Lisätietoja on kohdassa [Yleisen kansion luonti](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span></span>

- <span data-ttu-id="1b2e8-125">Sähköpostin käyttöönotto yleisessä *Queue*-kansiossa</span><span class="sxs-lookup"><span data-stu-id="1b2e8-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="1b2e8-126">Lisätietoja on kohdassa [Sähköpostin käyttöönotto tai käytöstäpoistaminen yleisessä kansiossa](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="1b2e8-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span></span>

- <span data-ttu-id="1b2e8-127">Sähköpostin käyttöönoton sähköpostien lähettämiseen yleiseen *Queue*-kansioon käyttämällä Outlookia tai Exchange-palvelimen hallintaliittymää</span><span class="sxs-lookup"><span data-stu-id="1b2e8-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="1b2e8-128">Lisätietoja on kohdassa [Luvan antaminen anonyymeille käyttäjille sähköpostin lähettämiseen yleiseen kansioon, jossa sähköposti on otettu käyttöön](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span><span class="sxs-lookup"><span data-stu-id="1b2e8-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span></span>

- <span data-ttu-id="1b2e8-129">Määritä sähköpostin lokiinkirjauksen käyttäjä kummankin yleisen kansion, *Queue* ja *Storage*, omistajaksi käyttämällä Outlookia tai Exchange-palvelimen hallintaliittymää seuraavan taulukon tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="1b2e8-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="1b2e8-130">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="1b2e8-130">Property</span></span>        |<span data-ttu-id="1b2e8-131">Arvo</span><span class="sxs-lookup"><span data-stu-id="1b2e8-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="1b2e8-132">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="1b2e8-132">User</span></span>            |<span data-ttu-id="1b2e8-133">Sen käyttäjätilin sähköposti, jota Business Central käyttää sähköpostin lokiinkirjaustyön suorittamiseen</span><span class="sxs-lookup"><span data-stu-id="1b2e8-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="1b2e8-134">Käyttöoikeustaso</span><span class="sxs-lookup"><span data-stu-id="1b2e8-134">Permission level</span></span>|<span data-ttu-id="1b2e8-135">Omistaja</span><span class="sxs-lookup"><span data-stu-id="1b2e8-135">Owner</span></span>                     |

  <span data-ttu-id="1b2e8-136">Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen yleiseen kansioon](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="1b2e8-137">Kahden postityönkulkusäännön luonti seuraavan taulukon tietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="1b2e8-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="1b2e8-138">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="1b2e8-138">Purpose</span></span>  |<span data-ttu-id="1b2e8-139">Name</span><span class="sxs-lookup"><span data-stu-id="1b2e8-139">Name</span></span> |<span data-ttu-id="1b2e8-140">Ehdot</span><span class="sxs-lookup"><span data-stu-id="1b2e8-140">Conditions</span></span>                        |<span data-ttu-id="1b2e8-141">Toiminto</span><span class="sxs-lookup"><span data-stu-id="1b2e8-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="1b2e8-142">Saapuvan sähköpostin sääntö</span><span class="sxs-lookup"><span data-stu-id="1b2e8-142">A rule for incoming email</span></span> |<span data-ttu-id="1b2e8-143">Lokin sähköposti lähetetty tälle organisaatiolle</span><span class="sxs-lookup"><span data-stu-id="1b2e8-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="1b2e8-144">*Lähettäjä* sijaitsee *organisaation ulkopuolella* ja *vastaanottaja* sijaitsee *organisaation sisäpuolella*</span><span class="sxs-lookup"><span data-stu-id="1b2e8-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="1b2e8-145">Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille</span><span class="sxs-lookup"><span data-stu-id="1b2e8-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="1b2e8-146">Lähtevän sähköpostin sääntö</span><span class="sxs-lookup"><span data-stu-id="1b2e8-146">A rule for outgoing email</span></span> | <span data-ttu-id="1b2e8-147">Lokin sähköposti lähetetty tästä organisaatiosta</span><span class="sxs-lookup"><span data-stu-id="1b2e8-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="1b2e8-148">*Lähettäjä* sijaitsee *organisaation sisäpuolella* ja *vastaanottaja* sijaitsee *organisaation ulkopuolella*</span><span class="sxs-lookup"><span data-stu-id="1b2e8-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="1b2e8-149">Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille</span><span class="sxs-lookup"><span data-stu-id="1b2e8-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="1b2e8-150">Lisätietoja on kohdassa [Postityönkulkusääntöjen hallinta Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) ja [Postityönkulkusäännön toiminnot Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span><span class="sxs-lookup"><span data-stu-id="1b2e8-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span></span>

> [!NOTE]
> <span data-ttu-id="1b2e8-151">Jos Exchange-palvelimen hallintaliittymään tehdään muutoksia, muutokset tulevat näkyviin Exchangen hallintakeskuksessa viiveen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1b2e8-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="1b2e8-152">Myös Exchangeen tehdyt muutokset ovat käytettävissä [!INCLUDE[prodshort](prodshort.md)]issa viiveen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1b2e8-152">Also, the changes made in Exchange will be available in [!INCLUDE[prodshort](prodshort.md)] after a delay.</span></span>
