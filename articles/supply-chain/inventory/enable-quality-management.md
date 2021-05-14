---
title: تمكين إدارة عدم المطابقة والجودة
description: يقدم هذا الموضوع نظرة عامة حول عملية إعداد وتكوين ميزات إدارة الجودة وعدم المطابقة في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956244"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="48743-103">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="48743-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48743-104">يقدم هذا الموضوع نظرة عامة حول عملية إعداد وتكوين ميزات إدارة الجودة وعدم المطابقة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="48743-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="48743-105">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="48743-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="48743-106">اتبع هذه الخطوات لتمكين إدارة الجودة على نظامك.</span><span class="sxs-lookup"><span data-stu-id="48743-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="48743-107">انتقل إلى **إدارة المخزون \> إعداد \> معلمات إدارة المخزون والمستودع**.</span><span class="sxs-lookup"><span data-stu-id="48743-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="48743-108">في علامة التبويب **إدارة الجودة**، قم بتعيين خيار **استخدام إدارة الجودة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="48743-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="48743-109">وفي حقل **الأجر بالساعة**، أدخل أجر عامل بالساعة بالعملة المحلية.</span><span class="sxs-lookup"><span data-stu-id="48743-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="48743-110">ويتم استخدام الأجر بالساعة لحساب تكاليف العمليات المرتبطة بعدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="48743-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="48743-111">ويوفر حقلا الأجر بالساعة والتكاليف المحسوبة معلومات مرجعية لعدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="48743-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="48743-112">ولا يتفاعلا مع الوظائف الأخرى.</span><span class="sxs-lookup"><span data-stu-id="48743-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="48743-113">تحديد **إعداد التقرير**.</span><span class="sxs-lookup"><span data-stu-id="48743-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="48743-114">أضف سطورًا جديدة لأنواع التقارير المختلفة، وحدد نوع المستند المراد استخدامه لكل تقرير.</span><span class="sxs-lookup"><span data-stu-id="48743-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="48743-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="48743-115">Close the page.</span></span>
1. <span data-ttu-id="48743-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="48743-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="48743-117">عملية تكوين إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="48743-117">Quality management configuration process</span></span>

<span data-ttu-id="48743-118">قبل أن تتمكن من البدء في استخدام ميزات إدارة الجودة وإنشاء أوامر الجودة، يجب عليك تكوين النظام والمتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="48743-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="48743-119">فيما يلي قائمة بالخطوات المطلوبة لتكوين إدارة الجودة.</span><span class="sxs-lookup"><span data-stu-id="48743-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="48743-120">[تمكين إدارة عدم المطابقة والجودة](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="48743-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="48743-121">اختياري: [تكوين مستندات الاختبار](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="48743-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="48743-122">[تكوين الاختبارات](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="48743-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="48743-123">[تكوين متغيرات الاختبار ونتائجه](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="48743-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="48743-124">[تكوين مجموعات الاختبار](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="48743-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="48743-125">اختياري: [تكوين مجموعات الجودة والارتباط بالمنتجات](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="48743-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="48743-126">اختياري: [تكوين عمليات إقران الجودة](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="48743-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="48743-127">بعد اكتمال التكوين، يمكنك البدء في إنشاء أوامر الجودة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="48743-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="48743-128">لمزيد من المعلومات حول كيفية إنشاء أوامر الجودة والعمل معها، راجع [أوامر الجودة](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="48743-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="48743-129">عملية تكوين إدارة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="48743-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="48743-130">قبل أن تتمكن من البدء في استخدام ميزات إدارة عدم المطابقة وإنشاء حالات عدم المطابقة، يجب عليك تكوين النظام والمتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="48743-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="48743-131">فيما يلي قائمة بالخطوات المطلوبة لتكوين إدارة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="48743-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="48743-132">[تمكين إدارة عدم المطابقة والجودة](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="48743-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="48743-133">[تكوين العاملين المسؤولين عن الموافقة على حالات عدم المطابقة](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="48743-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="48743-134">[تكوين أنواع المشكلات](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="48743-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="48743-135">[تكوين مناطق العزل](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="48743-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="48743-136">[تكوين أنواع التشخيص](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="48743-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="48743-137">[تكوين العمليات](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="48743-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="48743-138">اختياري: [تكوين تكاليف الجودة](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="48743-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="48743-139">بعد اكتمال التكوين، يمكنك البدء في إنشاء حالات عدم المطابقة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="48743-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="48743-140">لمزيد من المعلومات حول كيفية إنشاء والعمل مع عدم المطابقة، راجع [إنشاء حالات عدم المطابقة ومعالجتها](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="48743-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48743-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="48743-141">Additional resources</span></span>

- [<span data-ttu-id="48743-142">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="48743-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="48743-143">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="48743-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="48743-144">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="48743-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
