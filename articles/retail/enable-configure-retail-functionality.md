---
title: "تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة"
description: "توضح هذه المقالة البيانات التي تم إنشاؤها كجزء من عملية تهيئة Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d3c81aaa675352eb679c1e1540f947c1d1da804b
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="bbd27-103">تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة</span><span class="sxs-lookup"><span data-stu-id="bbd27-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bbd27-104">توضح هذه المقالة البيانات التي تم إنشاؤها كجزء من عملية تهيئة Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bbd27-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bbd27-105">بعد أنه تم نشر حل البيع بالتجزئة من خلال Microsoft Dynamics Lifecycle Services ‏(LCS)، يجب عليك تهيئة تكوين البيع بالتجزئة لإنشاء بيانات التكوين الأساسية.</span><span class="sxs-lookup"><span data-stu-id="bbd27-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="bbd27-106">**هام:** قبل تهيئة تكوين البيع بالتجزئة، تأكد من أنك حددت لغة وعنوان بريدي لكل كيان قانوني حيث ستقوم بإعداد متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="bbd27-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="bbd27-107">ويجب إكمال هذه الخطوة لكل كيان قانوني تستخدمه للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="bbd27-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="bbd27-108">وتهيئة تكوين البيع بالتجزئة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bbd27-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="bbd27-109">بدء عميل Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bbd27-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="bbd27-110">انقر فوق **البيع بالتجزئة** &gt; **إعداد المقر الرئيسي** &gt; **المعلمات** &gt; **معلمات البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="bbd27-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="bbd27-111">انقر فوق **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="bbd27-111">Click **Initialize**.</span></span>

<span data-ttu-id="bbd27-112">تقوم التهيئة بإنشاء بيانات التكوين الافتراضية التالية:</span><span class="sxs-lookup"><span data-stu-id="bbd27-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="bbd27-113">الوظائف والوظائف الفرعية لمجدول البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="bbd27-114">مخطط قنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-114">Retail channel schema</span></span>
-   <span data-ttu-id="bbd27-115">جداول توزيع البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="bbd27-116">تخطيطات الشاشة الافتراضية التي تتضمن شبكات الأزرار والصور والسمات</span><span class="sxs-lookup"><span data-stu-id="bbd27-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="bbd27-117">معلومات المنطقة الزمنية</span><span class="sxs-lookup"><span data-stu-id="bbd27-117">Time zone information</span></span>
-   <span data-ttu-id="bbd27-118">عمليات نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="bbd27-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="bbd27-119">أذونات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="bbd27-119">POS permissions</span></span>
-   <span data-ttu-id="bbd27-120">تقارير القناة</span><span class="sxs-lookup"><span data-stu-id="bbd27-120">Channel reports</span></span>
-   <span data-ttu-id="bbd27-121">بيانات تعريف السمة</span><span class="sxs-lookup"><span data-stu-id="bbd27-121">Attribute metadata</span></span>
-   <span data-ttu-id="bbd27-122">قوالب التحقق من صحة الكيان</span><span class="sxs-lookup"><span data-stu-id="bbd27-122">Entity validation templates</span></span>
-   <span data-ttu-id="bbd27-123">الوظيفة الدُفعية لإزالة محفوظات جلسات Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="bbd27-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="bbd27-124">بالإضافة إلى ذلك، يتم تمكين التسجيل المتعلق بصناعة بطاقات الدفع (PCI) لقاعدة بيانات Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bbd27-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="bbd27-125">**ملاحظة:** هناك خيار لتكوين مجدول البيع بالتجزئة بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="bbd27-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="bbd27-126">يتيح لك هذا الخيار إعادة تعيين تكوين مجدول البيع بالتجزئة إلى الإعدادات الافتراضية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="bbd27-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="bbd27-127">وبعد إتمام عملية التهيئة، يجب عليك تكوين البيانات الإضافية للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="bbd27-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="bbd27-128">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="bbd27-128">Here are some examples:</span></span>

-   <span data-ttu-id="bbd27-129">معلمات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-129">Retail parameters</span></span>
-   <span data-ttu-id="bbd27-130">معلمات مجدول البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="bbd27-131">قنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bbd27-131">Retail channels</span></span>
-   <span data-ttu-id="bbd27-132">السجلات والأجهزة</span><span class="sxs-lookup"><span data-stu-id="bbd27-132">Registers and devices</span></span>
-   <span data-ttu-id="bbd27-133">عمليات الفرز</span><span class="sxs-lookup"><span data-stu-id="bbd27-133">Assortments</span></span>





