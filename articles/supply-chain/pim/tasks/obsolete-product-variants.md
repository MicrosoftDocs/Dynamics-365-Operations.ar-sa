--- 
title: "البحث عن متغيرات المنتجات القديمة"
description: "يوضح هذا الإجراء كيفية البحث عن المنتجات القديمة الصادرة أو متغيرات المنتجات، وكيفية إقران حالة دورة حياة منتج بالمنتجات القديمة."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: ar-sa
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="359f4-103">البحث عن متغيرات المنتجات القديمة</span><span class="sxs-lookup"><span data-stu-id="359f4-103">Find obsolete product variants</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="359f4-104">يوضح هذا الإجراء كيفية البحث عن المنتجات القديمة الصادرة أو متغيرات المنتجات، وكيفية إقران حالة دورة حياة منتج بالمنتجات القديمة.</span><span class="sxs-lookup"><span data-stu-id="359f4-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="359f4-105">المتطلبات الأساسية: يجب تحديد حالة دورة حياة منتج واحدة على الأقل تكون غير نشطة للتخطيط قبل أن تتمكن من قراءة دليل المهام هذا.</span><span class="sxs-lookup"><span data-stu-id="359f4-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="359f4-106">تشغيل محاكاة</span><span class="sxs-lookup"><span data-stu-id="359f4-106">Run a simulation</span></span>
1. <span data-ttu-id="359f4-107">انتقل إلى إدارة معلومات المنتج > المهام الدورية > تغيير حالة دورة حياة المنتجات المهملة‬.</span><span class="sxs-lookup"><span data-stu-id="359f4-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="359f4-108">في الحقل "حالة دورة حياة المنتج الجديدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="359f4-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="359f4-109">حدد "نعم" في الحقل "تشغيل المحاكاة بدون تحديث بيانات المنتج".</span><span class="sxs-lookup"><span data-stu-id="359f4-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="359f4-110">في الحقل "استثناء المنتجات التي تم إنشاؤها خلال هذا العدد من الأيام"، أدخل عددًا.</span><span class="sxs-lookup"><span data-stu-id="359f4-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="359f4-111">في الحقل "استثناء المنتجات المستخدمة في الحركات (بعدد الأيام)‬"، أدخل عددًا.</span><span class="sxs-lookup"><span data-stu-id="359f4-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="359f4-112">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="359f4-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="359f4-113">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="359f4-113">Click Filter.</span></span>
8. <span data-ttu-id="359f4-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="359f4-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="359f4-115">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="359f4-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="359f4-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="359f4-116">Click OK.</span></span>
11. <span data-ttu-id="359f4-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="359f4-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="359f4-118">من المستحسن تشغيل المحاكاة كوظيفة دُفعية إذا كنت تتوقع البحث عن عدد كبير من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="359f4-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="359f4-119">تأكد أيضًا من عدم تم تشغيل المحاكاة خلال الوقت الذي يكون فيه العمل في الشركة كثير النشاط.</span><span class="sxs-lookup"><span data-stu-id="359f4-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="359f4-120">مراجعة نتائج المحاكاة</span><span class="sxs-lookup"><span data-stu-id="359f4-120">Review the simulation results</span></span>
1. <span data-ttu-id="359f4-121">انتقل إلى إدارة معلومات المنتج > الاستعلامات والتقارير‬ > سجل صيانة حالة دورة حياة المنتج‬.</span><span class="sxs-lookup"><span data-stu-id="359f4-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="359f4-122">في هذه الصفحة، يمكنك مراجعة نتائج المحاكاة وإجراء تقييم لعدد المنتجات ومتغيرات المنتجات التي سيتم إقرانها بحالة دورة حياة منتج جديدة عند تشغيل التحديث بدون محاكاة.</span><span class="sxs-lookup"><span data-stu-id="359f4-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="359f4-123">تشغيل تحديث حالة دورة حياة المنتج للمنتجات القديمة</span><span class="sxs-lookup"><span data-stu-id="359f4-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="359f4-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="359f4-124">Close the page.</span></span>
2. <span data-ttu-id="359f4-125">انتقل إلى إدارة معلومات المنتج > المهام الدورية > تغيير حالة دورة حياة المنتجات المهملة‬.</span><span class="sxs-lookup"><span data-stu-id="359f4-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="359f4-126">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="359f4-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="359f4-127">لاحظ أنه تم حفظ التحديد الأخير.</span><span class="sxs-lookup"><span data-stu-id="359f4-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="359f4-128">حدد "لا" في الحقل "تشغيل المحاكاة بدون تحديث بيانات المنتج".</span><span class="sxs-lookup"><span data-stu-id="359f4-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="359f4-129">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="359f4-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="359f4-130">بالاستناد إلى عدد المنتجات ومتغيرات المنتجات المتأثرة، خذ بعين الاعتبار تشغيل هذه الوظيفة كوظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="359f4-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="359f4-131">تأكد من عدم تشغيل وظيفة تحديث كبيرة أثناء ساعات العمل الكثيرة النشاط في الشركة.</span><span class="sxs-lookup"><span data-stu-id="359f4-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="359f4-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="359f4-132">Click OK.</span></span>
7. <span data-ttu-id="359f4-133">انتقل إلى إدارة معلومات المنتج > الاستعلامات والتقارير‬ > سجل صيانة حالة دورة حياة المنتج‬.</span><span class="sxs-lookup"><span data-stu-id="359f4-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="359f4-134">راجع المنتجات ومتغيرات المنتجات الصادرة التي تم إدخال تغييرات عليها.</span><span class="sxs-lookup"><span data-stu-id="359f4-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="359f4-135">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="359f4-135">In the list, find and select the desired record.</span></span>


