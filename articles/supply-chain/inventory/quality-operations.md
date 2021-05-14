---
title: عمليات حالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه إنشاء عمليات عدم التوافق واستخدامها.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956540"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="3512f-103">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3512f-104">يوضح هذا الموضوع كيفيه إنشاء عمليات عدم التوافق واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="3512f-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="3512f-105">يمكنك استخدام صفحة **العمليات** لتحديد تصنيفات العمل الذي قد يمكن تطبيقه لحالة عدم مطابقة معتمدة.</span><span class="sxs-lookup"><span data-stu-id="3512f-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="3512f-106">عند تعيين عملية ذات صلة إلى حالة عدم توافق، يمكنك تقديم تفاصيل مثل المواد المرتبطة وساعات العمل والرسوم المطلوبة لإجراء العملية.</span><span class="sxs-lookup"><span data-stu-id="3512f-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="3512f-107">يستخدم النظام هذه المعلومات لحساب التكلفة المقدرة للعملية.</span><span class="sxs-lookup"><span data-stu-id="3512f-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="3512f-108">وتُستخدم المعلومات المفصلة والتكاليف المقدرة كمرجع.</span><span class="sxs-lookup"><span data-stu-id="3512f-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="3512f-109">كما تختلف العمليات ذات الصلة بالجودة عن تلك التي يمكن تعريفها لمسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3512f-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="3512f-110">علي الرغم من انه يمكنك تتبع التكاليف والوقت والأصناف المستخدمة في عمليه مرتبطة بعدم التوافق، فان البيانات التي تقوم بإدخالها تكون معلوماتية فقط.</span><span class="sxs-lookup"><span data-stu-id="3512f-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="3512f-111">ولا يتم دمجها تلقائيا مع دفتر الأستاذ العام أو المخزون بالأستاذ الفرعي أو وحدة **الوقت والحضور**.</span><span class="sxs-lookup"><span data-stu-id="3512f-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="3512f-112">أمثله علي العمليات</span><span class="sxs-lookup"><span data-stu-id="3512f-112">Examples of operations</span></span>

<span data-ttu-id="3512f-113">أنت تعمل لشركه تصنيع.</span><span class="sxs-lookup"><span data-stu-id="3512f-113">You work for a manufacturing company.</span></span> <span data-ttu-id="3512f-114">تم إنشاء عدم التوافق واعتماده للأصناف التي فشلت في اختبار الجودة.</span><span class="sxs-lookup"><span data-stu-id="3512f-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="3512f-115">تم إنشاء تصحيح للاشاره إلى ان المشكلة تتعلق بعمليه الأسطوانات التالفة علي الجهاز.</span><span class="sxs-lookup"><span data-stu-id="3512f-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="3512f-116">وتكون العديد من الخطوات مطلوبه لاستبدال الأحجار، ويتم تعقب المسؤولية لكل عمليه.</span><span class="sxs-lookup"><span data-stu-id="3512f-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="3512f-117">علي سبيل المثال، قد تكون الخطوات التالية مطلوبه:</span><span class="sxs-lookup"><span data-stu-id="3512f-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="3512f-118">يتم إيقاف بند الإنتاج، ويتم تنفيذ روتين المسح الثلاثي.</span><span class="sxs-lookup"><span data-stu-id="3512f-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="3512f-119">يقوم موظفو الصيانة باستبدال الأحجار.</span><span class="sxs-lookup"><span data-stu-id="3512f-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="3512f-120">تاكيد الجودة يقوم العاملون بفحص الجهاز قبل ان يتم تشغيله مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="3512f-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="3512f-121">بالنسبة لهذا المثال، يمكن إنشاء العمليات التالية لتمثل العمل الذي يجب القيام به:</span><span class="sxs-lookup"><span data-stu-id="3512f-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="3512f-122">إيقاف بند الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3512f-122">Stop the production line.</span></span>
- <span data-ttu-id="3512f-123">مسح بند الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3512f-123">Clean out the production line.</span></span>
- <span data-ttu-id="3512f-124">إجراء صيانة الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="3512f-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="3512f-125">افحص الجهاز.</span><span class="sxs-lookup"><span data-stu-id="3512f-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="3512f-126">إنشاء عملية</span><span class="sxs-lookup"><span data-stu-id="3512f-126">Create an operation</span></span>

1. <span data-ttu-id="3512f-127">انتقل إلى **إدارة المخزون \> إعداد \> إدارة الجودة \> العمليات**.</span><span class="sxs-lookup"><span data-stu-id="3512f-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="3512f-128">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3512f-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3512f-129">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="3512f-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="3512f-130">**العملية** – أدخل معرفا فريدا أو اسما للعملية.</span><span class="sxs-lookup"><span data-stu-id="3512f-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="3512f-131">**الوصف** - أدخل وصفًا مفصلاً للعملية.</span><span class="sxs-lookup"><span data-stu-id="3512f-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="3512f-132">**النوع** - إذا كان يمكن استخدام العملية فقط مع عدم التوافق المرتبطة بنوع معين من الأوامر، حدد نوع الأمر ( *أمر الشراء* أو *أمر المبيعات*).</span><span class="sxs-lookup"><span data-stu-id="3512f-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="3512f-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3512f-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3512f-134">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3512f-134">Additional resources</span></span>

- [<span data-ttu-id="3512f-135">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="3512f-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="3512f-136">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="3512f-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="3512f-137">إنشاء حالات عدم المطابقة ومعالجتها</span><span class="sxs-lookup"><span data-stu-id="3512f-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="3512f-138">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="3512f-139">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="3512f-140">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="3512f-141">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="3512f-142">أنواع المشكلات لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="3512f-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="3512f-143">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="3512f-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
