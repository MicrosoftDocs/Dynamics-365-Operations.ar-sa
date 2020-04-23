---
title: دورة حياة أمر الدُفعة من الإنشاء حتى بدء التشغيل
description: يأخذك هذا الإجراء من خلال الجزء الأول من دورة حياة أمر الدفعة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16b55726fdb9ab15e74a9f752cac972b80a98de2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210975"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="b5f3c-103">دورة حياة أمر الدُفعة من الإنشاء حتى بدء التشغيل</span><span class="sxs-lookup"><span data-stu-id="b5f3c-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5f3c-104">يأخذك هذا الإجراء من خلال الجزء الأول من دورة حياة أمر الدفعة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="b5f3c-105">من الإنشاء وتقدير التكلفة، ثم عبر جدولة وظيفة الإنتاج إلى البدء الفعلي لأمر الدفعة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="b5f3c-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="b5f3c-107">المتطلبات المسبقة لتشغيل الإجراء بواسطة مجموعة بيانات أخرى هي منتج صادر مع معادلة نشطة وإصدار المسار.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="b5f3c-108">إنشاء أمر دفعة</span><span class="sxs-lookup"><span data-stu-id="b5f3c-108">Create a batch order</span></span>
1. <span data-ttu-id="b5f3c-109">انتقل إلى "كافة أوامر الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-109">Go to All production orders.</span></span>
2. <span data-ttu-id="b5f3c-110">انقر فوق أمر دُفعة جديد.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-110">Click New batch order.</span></span>
3. <span data-ttu-id="b5f3c-111">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="b5f3c-112">انقر فوق إنشاء.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-112">Click Create.</span></span>
5. <span data-ttu-id="b5f3c-113">استخدم "عامل التصفية السريع" لتصفية حقل "الإنتاج" باستخدام القيمة ''b".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="b5f3c-114">عرض معادلة الإنتاج والمنتجات المساعدة المتوقعة</span><span class="sxs-lookup"><span data-stu-id="b5f3c-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="b5f3c-115">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b5f3c-116">انقر فوق المعادلة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-116">Click Formula.</span></span>
3. <span data-ttu-id="b5f3c-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-117">Close the page.</span></span>
4. <span data-ttu-id="b5f3c-118">انقر فوق "‏‫المنتجات المساعدة‬".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-118">Click Co-products.</span></span>
5. <span data-ttu-id="b5f3c-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="b5f3c-120">تقدير أمر الدُفعة</span><span class="sxs-lookup"><span data-stu-id="b5f3c-120">Estimate the batch order</span></span>
1. <span data-ttu-id="b5f3c-121">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-121">Click Estimate.</span></span>
2. <span data-ttu-id="b5f3c-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-122">Click OK.</span></span>
3. <span data-ttu-id="b5f3c-123">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="b5f3c-124">انقر فوق "عرض تفاصيل الحساب"ز</span><span class="sxs-lookup"><span data-stu-id="b5f3c-124">Click View calculation details.</span></span>
5. <span data-ttu-id="b5f3c-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="b5f3c-126">إصدار أمر الدُفعة</span><span class="sxs-lookup"><span data-stu-id="b5f3c-126">Release the batch order</span></span>
1. <span data-ttu-id="b5f3c-127">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b5f3c-128">انقر فوق "إصدار".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-128">Click Release.</span></span>
3. <span data-ttu-id="b5f3c-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="b5f3c-130">جدولة وظائف الإنتاج</span><span class="sxs-lookup"><span data-stu-id="b5f3c-130">Schedule production jobs</span></span>
1. <span data-ttu-id="b5f3c-131">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="b5f3c-132">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="b5f3c-133">حدد "لا" في حقل "القدرة المحدودة‬".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="b5f3c-134">حدد "لا" في حقل "المواد المحدودة‬".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="b5f3c-135">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-135">Click OK.</span></span>
6. <span data-ttu-id="b5f3c-136">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="b5f3c-137">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-137">Click All jobs.</span></span>
8. <span data-ttu-id="b5f3c-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="b5f3c-139">بدء تشغيل أمر الدفعة</span><span class="sxs-lookup"><span data-stu-id="b5f3c-139">Start the batch order</span></span>
1. <span data-ttu-id="b5f3c-140">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-140">Click Start.</span></span>
2. <span data-ttu-id="b5f3c-141">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-141">Click the General tab.</span></span>
3. <span data-ttu-id="b5f3c-142">حدد "لا" في حقل ترحيل قائمة الانتقاء الآن.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="b5f3c-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-143">Click OK.</span></span>
5. <span data-ttu-id="b5f3c-144">في جزء "الإجراءات"، انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="b5f3c-145">انقر فوق "قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-145">Click Picking list.</span></span>
7. <span data-ttu-id="b5f3c-146">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b5f3c-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-147">Close the page.</span></span>
9. <span data-ttu-id="b5f3c-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-148">Close the page.</span></span>
10. <span data-ttu-id="b5f3c-149">انقر فوق "بطاقة المسار".</span><span class="sxs-lookup"><span data-stu-id="b5f3c-149">Click Route card.</span></span>
11. <span data-ttu-id="b5f3c-150">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b5f3c-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-151">Close the page.</span></span>
13. <span data-ttu-id="b5f3c-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-152">Close the page.</span></span>

