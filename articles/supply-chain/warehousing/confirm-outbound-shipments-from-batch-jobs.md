---
title: تأكيد الشحنات الخارجية من الوظائف الدفعية
description: يوضح هذا الموضوع كيفية إعداد وظيفة دُفعية تقوم بشكل تلقائي بتأكيد شحنات أوامر التحويل الصادرة للأحمال الجاهزة للشحن.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996291"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="a1ac0-103">تأكيد الشحنات الخارجية من الوظائف الدفعية</span><span class="sxs-lookup"><span data-stu-id="a1ac0-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1ac0-104">يوضح هذا الموضوع كيفية إعداد وظيفة دُفعية تقوم بشكل تلقائي بتأكيد شحنات أوامر التحويل الصادرة للأحمال الجاهزة للشحن.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="a1ac0-105">تنطبق الوظيفة الدُفعية التي ورد وصفها هنا على شحنات أوامر التحويل وليس على أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="a1ac0-106">تمكين ميزة تأكيد الشحنات الصادرة من الوظائف الدُفعية</span><span class="sxs-lookup"><span data-stu-id="a1ac0-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="a1ac0-107">قبل أن تتمكن من استخدام هذه الميزة، يجب تمكينها على النظام.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="a1ac0-108">بإمكان المسؤولين استخدام صفحة [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتمكينها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="a1ac0-109">يتم إدراج الميزة على أنها:</span><span class="sxs-lookup"><span data-stu-id="a1ac0-109">The feature is listed as:</span></span>

- <span data-ttu-id="a1ac0-110">**الوحدة** - *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="a1ac0-111">**اسم الميزة** - *تأكيد الشحنات الصادرة من الوظائف الدُفعية*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="a1ac0-112">معالجة الشحنات الصادرة</span><span class="sxs-lookup"><span data-stu-id="a1ac0-112">Process outbound shipments</span></span>

<span data-ttu-id="a1ac0-113">لإعداد وظيفة دُفعية لتشغيل تأكيد الشحنات الصادرة للأحمال الجاهزة للشحن:</span><span class="sxs-lookup"><span data-stu-id="a1ac0-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="a1ac0-114">انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> معالجة الشحنات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="a1ac0-115">يظهر مربع الحوار **تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="a1ac0-116">في علامة التبويب السريعة **السجلات المُراد تضمينها**، حدد **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="a1ac0-117">يفتح مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-117">The query editor dialog box opens.</span></span> <span data-ttu-id="a1ac0-118">على علامة تبويب **النطاق**، أضف صفًا يتضمن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a1ac0-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="a1ac0-119">**الجدول** - *الأحمال*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="a1ac0-120">**الجدول المشتق** - *الأحمال*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="a1ac0-121">**الحقل** - *حالة الحِمل*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="a1ac0-122">**المعايير** - *محمل‬*</span><span class="sxs-lookup"><span data-stu-id="a1ac0-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="a1ac0-123">حدد **موافق** للعودة إلى مربع الحوار **تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="a1ac0-124">على علامة التبويب السريعة **التشغيل في الخلفية**، قم بتعيين **المعالجة الدُفعية‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="a1ac0-125">على علامة التبويب السريعة **التشغيل في الخلفية** حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="a1ac0-126">يفتح مربع الحوار **تحديد التكرار**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="a1ac0-127">قم بتعيين جدول التشغيل الملائم لعملك.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="a1ac0-128">حدد **موافق** للعودة إلى مربع الحوار **تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="a1ac0-129">حدد **موافق** في مربع الحوار **تأكيد الشحن** لإضافة الوظيفة الدُفعية إلى قائمة الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="a1ac0-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="a1ac0-130">لمزيد من المعلومات، راجع [نظرة عامة على المعالجة الدُفعية](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1ac0-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
