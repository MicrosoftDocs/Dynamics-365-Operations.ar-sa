---
title: تهيئة بيانات أولية في بيئات Commerce الجديدة
description: تصف هذه المقالة البيانات التي يتم إنشاؤها كجزء من عملية تهيئة Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 24d4d49c51738203bb89a9844d57f644b8afd4b7
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284369"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="41da0-103">تهيئة بيانات أولية في بيئات Commerce الجديدة</span><span class="sxs-lookup"><span data-stu-id="41da0-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41da0-104">تصف هذه المقالة البيانات التي يتم إنشاؤها كجزء من عملية تهيئة Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="41da0-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="41da0-105">بعد نشر حل التجارة من خلال Microsoft Dynamics Lifecycle Services (LCS)، يجب تهيئة تكوين التجارة لإنشاء بيانات التكوين الأساسية.</span><span class="sxs-lookup"><span data-stu-id="41da0-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41da0-106">قبل تهيئة تكوين التجارة، تأكد من تحديد لغة وعنوان بريدي لكل كيان قانوني حيث ستقوم بإعداد المتاجر.</span><span class="sxs-lookup"><span data-stu-id="41da0-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="41da0-107">يجب إكمال هذه الخطوة لكل كيان قانوني تستخدمه للتجارة.</span><span class="sxs-lookup"><span data-stu-id="41da0-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="41da0-108">لتهيئة التكوين، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="41da0-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="41da0-109">ابدأ تشغيل عميل التجارة.</span><span class="sxs-lookup"><span data-stu-id="41da0-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="41da0-110">انتقل إلى **البيع بالتجزئة والتجارة** &gt; **إعداد المراكز الرئيسية** &gt; **المعلمات** &gt; **معلمات التجارة**.</span><span class="sxs-lookup"><span data-stu-id="41da0-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="41da0-111">انقر فوق **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="41da0-111">Click **Initialize**.</span></span>

<span data-ttu-id="41da0-112">تقوم التهيئة بإنشاء بيانات التكوين الافتراضية التالية:</span><span class="sxs-lookup"><span data-stu-id="41da0-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="41da0-113">الوظائف والوظائف الفرعية لمجدول التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="41da0-114">مخطط قناة التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-114">Commerce channel schema</span></span>
- <span data-ttu-id="41da0-115">جداول توزيعات التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="41da0-116">تخطيطات الشاشة الافتراضية التي تتضمن شبكات الأزرار والصور والسمات</span><span class="sxs-lookup"><span data-stu-id="41da0-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="41da0-117">معلومات المنطقة الزمنية</span><span class="sxs-lookup"><span data-stu-id="41da0-117">Time zone information</span></span>
- <span data-ttu-id="41da0-118">عمليات نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="41da0-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="41da0-119">أذونات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="41da0-119">POS permissions</span></span>
- <span data-ttu-id="41da0-120">تقارير القناة</span><span class="sxs-lookup"><span data-stu-id="41da0-120">Channel reports</span></span>
- <span data-ttu-id="41da0-121">بيانات تعريف السمة</span><span class="sxs-lookup"><span data-stu-id="41da0-121">Attribute metadata</span></span>
- <span data-ttu-id="41da0-122">قوالب التحقق من صحة الكيان</span><span class="sxs-lookup"><span data-stu-id="41da0-122">Entity validation templates</span></span>
- <span data-ttu-id="41da0-123">وظيفة دًفعية لحذف محفوظات جلسات عمل Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="41da0-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="41da0-124">وبالإضافة إلى ذلك، يتم تمكين التسجيل المتعلق بصناعة بطاقات الدفع (PCI) لقاعدة بيانات التجارة.</span><span class="sxs-lookup"><span data-stu-id="41da0-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="41da0-125">يوجد خيار لتكوين مجدول التجارة بصورة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="41da0-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="41da0-126">يتيح لك هذا الخيار إعادة تعيين تكوين مجدول التجارة إلى الإعدادات الافتراضية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="41da0-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="41da0-127">وبعد إتمام عملية التهيئة، يجب تكوين البيانات الإضافية للتجارة.</span><span class="sxs-lookup"><span data-stu-id="41da0-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="41da0-128">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="41da0-128">Here are some examples:</span></span>

- <span data-ttu-id="41da0-129">معلمات التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-129">Commerce parameters</span></span>
- <span data-ttu-id="41da0-130">معلمات مجدول التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="41da0-131">قنوات التجارة</span><span class="sxs-lookup"><span data-stu-id="41da0-131">Commerce channels</span></span>
- <span data-ttu-id="41da0-132">السجلات والأجهزة</span><span class="sxs-lookup"><span data-stu-id="41da0-132">Registers and devices</span></span>
- <span data-ttu-id="41da0-133">عمليات الفرز</span><span class="sxs-lookup"><span data-stu-id="41da0-133">Assortments</span></span>
