---
title: البحث عن متغيرات المنتجات القديمة
description: يوضح هذا الإجراء كيفية البحث عن المنتجات القديمة الصادرة أو متغيرات المنتجات، وكيفية إقران حالة دورة حياة منتج بالمنتجات القديمة.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4641d24cfa24722f5411da8943bfe4095a9546a4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567620"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="6907e-103">البحث عن متغيرات المنتجات القديمة</span><span class="sxs-lookup"><span data-stu-id="6907e-103">Find obsolete product variants</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6907e-104">يوضح هذا الإجراء كيفية البحث عن المنتجات القديمة الصادرة أو متغيرات المنتجات، وكيفية إقران حالة دورة حياة منتج بالمنتجات القديمة.</span><span class="sxs-lookup"><span data-stu-id="6907e-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="6907e-105">المتطلبات الأساسية: يجب تحديد حالة دورة حياة منتج واحدة على الأقل تكون غير نشطة للتخطيط قبل أن تتمكن من قراءة دليل المهام هذا.</span><span class="sxs-lookup"><span data-stu-id="6907e-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="6907e-106">تشغيل محاكاة</span><span class="sxs-lookup"><span data-stu-id="6907e-106">Run a simulation</span></span>
1. <span data-ttu-id="6907e-107">انتقل إلى إدارة معلومات المنتج > المهام الدورية > تغيير حالة دورة حياة المنتجات المهملة‬.</span><span class="sxs-lookup"><span data-stu-id="6907e-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="6907e-108">في الحقل "حالة دورة حياة المنتج الجديدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6907e-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="6907e-109">حدد "نعم" في الحقل "تشغيل المحاكاة بدون تحديث بيانات المنتج".</span><span class="sxs-lookup"><span data-stu-id="6907e-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="6907e-110">في الحقل "استثناء المنتجات التي تم إنشاؤها خلال هذا العدد من الأيام"، أدخل عددًا.</span><span class="sxs-lookup"><span data-stu-id="6907e-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="6907e-111">في الحقل "استثناء المنتجات المستخدمة في الحركات (بعدد الأيام)‬"، أدخل عددًا.</span><span class="sxs-lookup"><span data-stu-id="6907e-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="6907e-112">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="6907e-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="6907e-113">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="6907e-113">Click Filter.</span></span>
8. <span data-ttu-id="6907e-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6907e-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6907e-115">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6907e-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="6907e-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6907e-116">Click OK.</span></span>
11. <span data-ttu-id="6907e-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6907e-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="6907e-118">من المستحسن تشغيل المحاكاة كوظيفة دُفعية إذا كنت تتوقع البحث عن عدد كبير من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6907e-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="6907e-119">تأكد أيضًا من عدم تم تشغيل المحاكاة خلال الوقت الذي يكون فيه العمل في الشركة كثير النشاط.</span><span class="sxs-lookup"><span data-stu-id="6907e-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="6907e-120">مراجعة نتائج المحاكاة</span><span class="sxs-lookup"><span data-stu-id="6907e-120">Review the simulation results</span></span>
1. <span data-ttu-id="6907e-121">انتقل إلى إدارة معلومات المنتج > الاستعلامات والتقارير‬ > سجل صيانة حالة دورة حياة المنتج‬.</span><span class="sxs-lookup"><span data-stu-id="6907e-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="6907e-122">في هذه الصفحة، يمكنك مراجعة نتائج المحاكاة وإجراء تقييم لعدد المنتجات ومتغيرات المنتجات التي سيتم إقرانها بحالة دورة حياة منتج جديدة عند تشغيل التحديث بدون محاكاة.</span><span class="sxs-lookup"><span data-stu-id="6907e-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="6907e-123">تشغيل تحديث حالة دورة حياة المنتج للمنتجات القديمة</span><span class="sxs-lookup"><span data-stu-id="6907e-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="6907e-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6907e-124">Close the page.</span></span>
2. <span data-ttu-id="6907e-125">انتقل إلى إدارة معلومات المنتج > المهام الدورية > تغيير حالة دورة حياة المنتجات المهملة‬.</span><span class="sxs-lookup"><span data-stu-id="6907e-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="6907e-126">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="6907e-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="6907e-127">لاحظ أنه تم حفظ التحديد الأخير.</span><span class="sxs-lookup"><span data-stu-id="6907e-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="6907e-128">حدد "لا" في الحقل "تشغيل المحاكاة بدون تحديث بيانات المنتج".</span><span class="sxs-lookup"><span data-stu-id="6907e-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="6907e-129">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="6907e-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="6907e-130">بالاستناد إلى عدد المنتجات ومتغيرات المنتجات المتأثرة، خذ بعين الاعتبار تشغيل هذه الوظيفة كوظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="6907e-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="6907e-131">تأكد من عدم تشغيل وظيفة تحديث كبيرة أثناء ساعات العمل الكثيرة النشاط في الشركة.</span><span class="sxs-lookup"><span data-stu-id="6907e-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="6907e-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6907e-132">Click OK.</span></span>
7. <span data-ttu-id="6907e-133">انتقل إلى إدارة معلومات المنتج > الاستعلامات والتقارير‬ > سجل صيانة حالة دورة حياة المنتج‬.</span><span class="sxs-lookup"><span data-stu-id="6907e-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="6907e-134">راجع المنتجات ومتغيرات المنتجات الصادرة التي تم إدخال تغييرات عليها.</span><span class="sxs-lookup"><span data-stu-id="6907e-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="6907e-135">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6907e-135">In the list, find and select the desired record.</span></span>

