---
title: 'Vian etsintä: kameran ja sijainnin käyttäminen'
description: Tässä artikkelissa kuvataan, miten voidaan tehdä vianmääritys kameran ja sijaintitietojen käyttämiseen Business Centralin avulla.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: b44044b9ec2c71ad3b99f25b4a941a3ab473ca4f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912019"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="386e9-103">Vian etsintä: kameran ja sijainnin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="386e9-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="386e9-104">Saatat törmätä joihinkin ongelmiin, kun yrität käyttää laitteen kameraa ja sijaintitietoja kohteesta [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="386e9-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="386e9-105">Löydät mahdolliset syyt näiden ongelmien takana ja voit kiertää ne alla olevien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="386e9-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="386e9-106">Laitteessa on oltava kamera- ja sijaintiominaisuudet</span><span class="sxs-lookup"><span data-stu-id="386e9-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="386e9-107">Jotta voisit käyttää kameraa tai käyttäjän sijaintia laitteesta, laitteessa on oltava fyysinen kamera tai mahdollisuus hakea sijaintitietoja.</span><span class="sxs-lookup"><span data-stu-id="386e9-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="386e9-108">Jos laitteessa on kamera ja sijaintiominaisuudet, mutta ongelmia ilmenee edelleen, jotkin ohjaimet on ehkä päivitettävä tai asennettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="386e9-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="386e9-109">Vaikka et olisikaan varma, suosittelemme aina, että päivität laitteesi käyttöjärjestelmän, ohjaimet ja selaimen uusimpaan versioon saadaksesi parhaan käyttökokemuksen.</span><span class="sxs-lookup"><span data-stu-id="386e9-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="386e9-110">Käyttöoikeuksia ei ole otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="386e9-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="386e9-111">Sinun on otettava käyttöön kameran ja sijainnin yleinen käyttöoikeus laitteesi tietosuoja-asetuksista ja annettava niille eksplisiittisesti käyttöoikeus kohteeseen [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="386e9-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="386e9-112">Jos haluat esimerkiksi tarkastella tai muuttaa Windowsissa suoritettavan laitteen käyttöoikeuksia, valitse **Asetukset**, valitse **Yksityisyys** ja valitse sitten **Sovelluksen käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="386e9-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="386e9-113">Mobiililaitteissa on annettava kameran ja sijainnin käyttöoikeudet [!INCLUDE[prodshort](includes/prodshort.md)] -mobiilisovellukselle.</span><span class="sxs-lookup"><span data-stu-id="386e9-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="386e9-114">Voit tehdä tämän iOS-laitteessa siirtymällä kohtaan **Asetukset**, valitsemalla **Yksityisyys** ja sitten **Kamera** tai **Sijainti**.</span><span class="sxs-lookup"><span data-stu-id="386e9-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="386e9-115">Jos kyseessä on Android-laite, siirry kohtaan **Asetukset**, valitse **Sovellukset & ilmoitukset**, **Lisäasetukset**, **Käyttöoikeuksien hallinta** ja sitten **Kamera** tai **Sijainti**.</span><span class="sxs-lookup"><span data-stu-id="386e9-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="386e9-116">Lisäksi jos käytät [!INCLUDE[prodshort](includes/prodshort.md)] -sivustoa selaimessa, sinun täytyy myös myöntää [!INCLUDE[prodshort](includes/prodshort.md)] -sivustolle oikeus käyttää kameraa tai sijaintitietojasi.</span><span class="sxs-lookup"><span data-stu-id="386e9-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="386e9-117">Jos haluat tarkastella tai muuttaa sivustojen käyttö oikeuksia Microsoft Edge -selaimessa, mene kohtaan **Asetukset**, valitse **Sivustojen käyttöoikeudet** ja valitse sitten **Kamera** tai **Sijainti**.</span><span class="sxs-lookup"><span data-stu-id="386e9-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="386e9-118">Huomaa, että tämä voi olla erilainen muissa selaimissa.</span><span class="sxs-lookup"><span data-stu-id="386e9-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="386e9-119">Oletusarvon mukaan laite tai selain näyttää pyynnön käyttää näitä ominaisuuksia, kun käyttäjä aktivoi ne ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="386e9-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="386e9-120">Jotkin vanhat selaimet eivät salli kameran ja sijainnin käyttöä.</span><span class="sxs-lookup"><span data-stu-id="386e9-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="386e9-121">Kamera ei ole käytettävissä esimerkiksi Internet Explorerissa tai vanhassa Edge-selaimessa.</span><span class="sxs-lookup"><span data-stu-id="386e9-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="386e9-122">WWW-asiakasohjelman yhteys ei ole suojattu</span><span class="sxs-lookup"><span data-stu-id="386e9-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="386e9-123">Kamera- ja sijaintiominaisuudet ovat käytettävissä vain, kun WWW-asiakasohjelmaa käytetään SSL-suojattujen HTTP-yhteyksien avulla `https://`-URI-mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="386e9-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="386e9-124">Ainoa poikkeus on yhteyden muodostus kohteeseen `http://localhost`, jota käytetään kehitys- ja testitarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="386e9-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="386e9-125">Virtualisointitekniikoiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="386e9-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="386e9-126">Kun muodostat yhteyden kohteeseen [!INCLUDE[prodshort](includes/prodshort.md)] etätyöpöydän tai muun virtualisoinnin kautta, kameran tai sijainnin käyttö ei välttämättä ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="386e9-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="386e9-127">Käytä tässä tapauksessa fyysistä järjestelmää sen sijaan.</span><span class="sxs-lookup"><span data-stu-id="386e9-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="386e9-128">Virustentorjuntaohjelmisto</span><span class="sxs-lookup"><span data-stu-id="386e9-128">Antivirus Software</span></span>
<span data-ttu-id="386e9-129">Jotkin virustentorjuntaohjelmat estävät oletusarvoisesti kameran ja sijainnin käytön.</span><span class="sxs-lookup"><span data-stu-id="386e9-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="386e9-130">Muista tarkistaa virustentorjuntaohjelman asetukset.</span><span class="sxs-lookup"><span data-stu-id="386e9-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="386e9-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="386e9-131">See Also</span></span>
[<span data-ttu-id="386e9-132">Kameran käyttöönotto AL:ssä</span><span class="sxs-lookup"><span data-stu-id="386e9-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="386e9-133">Sijainnin käyttöönotto AL:ssä</span><span class="sxs-lookup"><span data-stu-id="386e9-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
