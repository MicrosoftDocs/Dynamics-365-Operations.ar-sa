---
title: مناطق العزل لحالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه إنشاء مناطق العزل لحالات عدم التوافق واستخدامها.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956538"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="d396e-103">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d396e-104">يوضح هذا الموضوع كيفيه إنشاء مناطق العزل لحالات عدم التوافق واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="d396e-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="d396e-105">يمكنك استخدام **مناطق العزل** لتحديد المناطق التي يمكن تعيينها لحالات عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="d396e-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="d396e-106">عند إنشاء حالة عدم توافق، يمكنك تعيين حقلي **منطقة العزل** و **نوع العزل** في علامة التبويب **عام** في صفحة **حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="d396e-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="d396e-107">يشير حقل **منطقة العزل** يشير عادةً إلى المنطقة أو الموقع حيث يوجد العنصر.</span><span class="sxs-lookup"><span data-stu-id="d396e-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="d396e-108">يحدد حقل **نوع العزل** العنصر كإما *استخدام مقيد* أو *لا يمكن استخدامه*.</span><span class="sxs-lookup"><span data-stu-id="d396e-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="d396e-109">عند طباعه تقرير عدم التوافق أو التصحيحات لعدم التوافق، يمكنك عرض منطقه الفحص التي يوجد بها الصنف.</span><span class="sxs-lookup"><span data-stu-id="d396e-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="d396e-110">يمكنك أيضا طباعه علامة عدم توافق لعدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="d396e-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="d396e-111">يعرض هذا التقرير منطقة العزل المعينة ومعلومات حول الاستخدام لتقديم إرشادات حول كيفية معالجة المواد المعيبة.</span><span class="sxs-lookup"><span data-stu-id="d396e-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="d396e-112">وقد تتطابق مناطق العزل مع مواقع المخزون أو موارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="d396e-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="d396e-113">أمثلة لمناطق العزل</span><span class="sxs-lookup"><span data-stu-id="d396e-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="d396e-114">مثال1</span><span class="sxs-lookup"><span data-stu-id="d396e-114">Example 1</span></span>

<span data-ttu-id="d396e-115">أنت تعمل في شركه تصنيع الكترونيات التي تقوم بإنتاج أجهزه التلفزيون ومكبرات الصوت ومشغلات الوسائط وتوزيعها.</span><span class="sxs-lookup"><span data-stu-id="d396e-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="d396e-116">في هذه الحالة، يمكنك تكوين منطقه فحص لتمثل كل نوع من أنواع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="d396e-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="d396e-117">مثال2</span><span class="sxs-lookup"><span data-stu-id="d396e-117">Example 2</span></span>

<span data-ttu-id="d396e-118">يتم استخدام ثلاثه حاويات والحاملين لتخزين الأصناف غير المتوافقة.</span><span class="sxs-lookup"><span data-stu-id="d396e-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="d396e-119">في هذه الحالة، يمكنك تكوين خمسه مناطق فحص، واحده لكل حاويه وكل حامل.</span><span class="sxs-lookup"><span data-stu-id="d396e-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="d396e-120">إنشاء منطقة عزل</span><span class="sxs-lookup"><span data-stu-id="d396e-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="d396e-121">انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> مناطق العزل**.</span><span class="sxs-lookup"><span data-stu-id="d396e-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="d396e-122">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d396e-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d396e-123">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="d396e-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d396e-124">**منطقة العزل** – أدخل معرفا فريدا أو اسما فريدا لمنطقة العزل.</span><span class="sxs-lookup"><span data-stu-id="d396e-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="d396e-125">**الوصف** - أدخل وصفًا مفصلاً لمنطقة العزل.</span><span class="sxs-lookup"><span data-stu-id="d396e-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="d396e-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d396e-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d396e-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d396e-127">Additional resources</span></span>

- [<span data-ttu-id="d396e-128">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="d396e-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d396e-129">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="d396e-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d396e-130">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="d396e-131">أنواع المشكلات لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="d396e-132">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="d396e-133">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="d396e-134">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d396e-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="d396e-135">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="d396e-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
