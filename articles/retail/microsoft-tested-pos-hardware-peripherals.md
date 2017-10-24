---
title: "‏‫الأجهزة الطرفية لنقطة البيع"
description: "باستطاعة نقطة البيع بالتجزئة الحديثة (POS) ونقطة بيع المجموعة استخدام مجموعة واسعة من الأجهزة الطرفية، مع واجهات وخيارات نشر متعددة لتحقيق سيناريوهات أعمال مختلفة لبائع التجزئة."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17738e794f18fddc7320b1b40ef55376fba0de24
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="1b717-103">‏‫الأجهزة الطرفية لنقطة البيع</span><span class="sxs-lookup"><span data-stu-id="1b717-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1b717-104">باستطاعة نقطة البيع بالتجزئة الحديثة (POS) ونقطة بيع المجموعة استخدام مجموعة واسعة من الأجهزة الطرفية، مع واجهات وخيارات نشر متعددة لتحقيق سيناريوهات أعمال مختلفة لبائع التجزئة.</span><span class="sxs-lookup"><span data-stu-id="1b717-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="1b717-105">لدعم أوسع مجموعة من الأجهزة عبر النماذج والشركات المصنعة، تستخدم نقاط البيع واجهات قياسية مثل OLE for Retail POS (OPOS) وبرامج تشغيل الأجهزة من Windows وواجهة البرامج التطبيقية (API) لنقطة الخدمة من Windows.</span><span class="sxs-lookup"><span data-stu-id="1b717-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="1b717-106">بشكل عام، ستعمل نقطة البيع على هذه الأجهزة شريطة أن يتم توفير برنامج التشغيل المناسب.</span><span class="sxs-lookup"><span data-stu-id="1b717-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="1b717-107">ومع ذلك، ونظرًا لوجود اختلافات على صعيد تطبيق هذه المعايير باختلاف الشركة المصنعة ومطور البرامج، هناك اختلافات في الكثير من الأحيان من ناحية القدرات أو السلوكيات المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="1b717-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="1b717-108">تتضمن القائمة التالية طُرز الأجهزة، في كل فئة، التي تم اختبارها داخليًا بواسطة Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1b717-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="1b717-109">**أجهزة OPOS**</span><span class="sxs-lookup"><span data-stu-id="1b717-109">**OPOS devices**</span></span>

-   <span data-ttu-id="1b717-110">الكود الشريطي – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="1b717-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="1b717-111">قارئ الشريط المغناطيسي – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="1b717-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="1b717-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="1b717-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="1b717-113">جهاز إدخال Pin (رقم التعريف الشخصي) – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="1b717-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="1b717-114">لوح التوقيع – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="1b717-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="1b717-115">الطابعة – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="1b717-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="1b717-116">درج الأوراق النقدية – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="1b717-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="1b717-117">المقياس – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="1b717-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="1b717-118">**قارئ الشريط المغناطيسي (MSR) على جهاز Keyboard Wedge**</span><span class="sxs-lookup"><span data-stu-id="1b717-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="1b717-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="1b717-119">Magtek USB</span></span>

<span data-ttu-id="1b717-120">**وحدة الدفع الطرفية**</span><span class="sxs-lookup"><span data-stu-id="1b717-120">**Payment terminal**</span></span>

-   <span data-ttu-id="1b717-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="1b717-121">Equinox L3500</span></span>
-   <span data-ttu-id="1b717-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="1b717-122">Verifone MX925</span></span>

<span data-ttu-id="1b717-123">**أجهزة الشبكة**</span><span class="sxs-lookup"><span data-stu-id="1b717-123">**Network devices**</span></span>

-   <span data-ttu-id="1b717-124">الطابعة – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="1b717-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="1b717-125">درج الأوراق النقدية – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="1b717-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="1b717-126">وحدة الدفع الطرفية – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="1b717-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="1b717-127">**تكاليف الإنتاج غير المباشرة (IPC) لنقطة بيع التجزئة الحديثة (MPOS) المباشرة فقط**</span><span class="sxs-lookup"><span data-stu-id="1b717-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="1b717-128">الكود الشريطي – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="1b717-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="1b717-129">قارئ الشريط المغناطيسي – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="1b717-129">MSR – Magtek PN - 21073075</span></span>





