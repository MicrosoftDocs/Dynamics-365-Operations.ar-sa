---
title: أنواع المشكلات لحالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه إنشاء أنواع المشكلات لحالات عدم التوافق واستخدامها.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022146"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="d7dfb-103">أنواع المشكلات لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7dfb-104">يوضح هذا الموضوع كيفيه إنشاء أنواع المشكلات لحالات عدم التوافق واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="d7dfb-105">يمكنك استخدام صفحة **أنواع المشكلات** لتحديد تصنيف مشكلات الجودة التي قد تحدث لأنواع حالات عدم المطابقة المختلفة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="d7dfb-106">بالنسبة لكل نوع مشكله تقوم بإنشاءه، يجب تحديد أنواع عدم التوافق التي يمكن استخدام نوع المشكلة معها.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="d7dfb-107">يمكنك إعداد أنواع عدم المطابقة التالية:</span><span class="sxs-lookup"><span data-stu-id="d7dfb-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="d7dfb-108">**داخلية** - تكون حالات عدم التوافق من هذا النوع مرتبطة بالمخزون الفعلي (علي سبيل المثال، أوامر الجودة أو أوامر إدخال مخزن الفحص).</span><span class="sxs-lookup"><span data-stu-id="d7dfb-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="d7dfb-109">**العميل** - حالات عدم التوافق الخاصة بهذا النوع بأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="d7dfb-110">**المورد** - حالات عدم التوافق الخاصة بهذا النوع بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="d7dfb-111">**طلب الخدمة** - حالات عدم التوافق الخاصة بهذا النوع بأوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="d7dfb-112">**الإنتاج** – ترتبط حالات عدم المطابقة من هذا النوع بأوامر الدُفعة أو أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="d7dfb-113">**إنتاج المنتجات المساعدة** – ترتبط حالات عدم المطابقة من هذا النوع بأوامر الدُفعة للمنتجات المساعدة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="d7dfb-114">عند إنشاء نوع مشكله جديد، حدد **أنواع عدم المطابقة** في جزء الإجراءات لإنشاء قائمه بنوع واحد أو أكثر من أنواع عدم المطابقة التي يتم اعتمادها لنوع المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="d7dfb-115">على سبيل المثال، قد ينطبق نوع المشكلة المرتبط بكود عيب على جميع أنواع عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="d7dfb-116">ومع ذلك، فإن نوع المشكلة المرتبط بشكاوى العملاء قد ينطبق فقط على أنواع حالات عدم المطابقة الخاصة بـ **العميل** و **طلب الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="d7dfb-117">أمثلة على أنواع المشكلات</span><span class="sxs-lookup"><span data-stu-id="d7dfb-117">Examples of problem types</span></span>

<span data-ttu-id="d7dfb-118">فيما يلي بعض الامثله علي السيناريوهات لأنواع المشكلات التي يمكن استخدامها مع أنواع عدم التوافق المختلفة:</span><span class="sxs-lookup"><span data-stu-id="d7dfb-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="d7dfb-119">**العميل:** قام أحد العملاء بتعبئة شكوى أو لم يتم الوفاء بأحد العملاء أو بإرجاع مواصفات الجودة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="d7dfb-120">**المورد**: تم اتلاف المنتج أو لم يتم الوفاء بمواصفات الجودة، أو ان المنتج الخطا قد تم استلامه.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="d7dfb-121">**طلب الخدمة:** لم يتم استيفاء مواصفات الجودة، أو ان العميل قد قم بتعبئة شكوى، أو صيانة اله مطلوبه.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="d7dfb-122">**الإنتاج:** لم يتم استيفاء مواصفات الجودة، أو ان صيانة الجهاز مطلوبه، أو ان المنتج معطوب.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="d7dfb-123">**إنتاج المنتجات المساعدة:** لم يتم استيفاء مواصفات الجودة، أو ان صيانة الجهاز مطلوبه، أو ان المنتج معطوب.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="d7dfb-124">إنشاء نوع مشكله وتعيينه إلى أنواع عدم التوافق</span><span class="sxs-lookup"><span data-stu-id="d7dfb-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="d7dfb-125">انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> أنواع المشكلات**.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="d7dfb-126">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d7dfb-127">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="d7dfb-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d7dfb-128">**نوع المشكلة** – أدخل معرفًا فريدًا أو اسمًا لنوع المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="d7dfb-129">**الوصف** - أدخل وصفًا مفصلاً لنوع المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="d7dfb-130">في حين ان الصف الجديد لا يزال محددا، حدد **أنواع حالات عدم المطابقة** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="d7dfb-131">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d7dfb-132">وبعد ذلك، بالنسبة للصف الجديد، قم بتعيين حقل **نوع عدم المطابقة** إلى نوع عدم المطابقة الذي تريد السماح به لنوع المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="d7dfb-133">كرر الخطوة السابقة لكل نوع عدم توافق إضافي تريد المصادقة عليه لنوع المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="d7dfb-134">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7dfb-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d7dfb-135">Additional resources</span></span>

- [<span data-ttu-id="d7dfb-136">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d7dfb-137">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d7dfb-138">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="d7dfb-139">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="d7dfb-140">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="d7dfb-141">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="d7dfb-142">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7dfb-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="d7dfb-143">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="d7dfb-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
