---
title: الاحتفاظ بمسار لنموذج منتج
description: يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567689"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="98096-103">الاحتفاظ بمسار لنموذج منتج</span><span class="sxs-lookup"><span data-stu-id="98096-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98096-104">يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود.</span><span class="sxs-lookup"><span data-stu-id="98096-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="98096-105">يستخدم هذا الإجراء نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF خلال العملية.</span><span class="sxs-lookup"><span data-stu-id="98096-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="98096-106">إضافة مسار عملية</span><span class="sxs-lookup"><span data-stu-id="98096-106">Add a route operation</span></span>
1. <span data-ttu-id="98096-107">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="98096-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="98096-108">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="98096-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="98096-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98096-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98096-110">حدد نموذج مكبر الصوت المتطور لهذا التمرين.</span><span class="sxs-lookup"><span data-stu-id="98096-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="98096-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="98096-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98096-112">قم بتوسيع القسم "عمليات المسار".</span><span class="sxs-lookup"><span data-stu-id="98096-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="98096-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="98096-113">Click Add.</span></span>
7. <span data-ttu-id="98096-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="98096-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="98096-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="98096-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="98096-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="98096-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="98096-117">إدخال تفاصيل مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="98096-117">Enter route operation details</span></span>
1. <span data-ttu-id="98096-118">انقر فوق "تفاصيل عملية المسار".</span><span class="sxs-lookup"><span data-stu-id="98096-118">Click Route operation details.</span></span>
2. <span data-ttu-id="98096-119">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="98096-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="98096-120">في حقل رقم</span><span class="sxs-lookup"><span data-stu-id="98096-120">In the Oper.</span></span> <span data-ttu-id="98096-121">العملية</span><span class="sxs-lookup"><span data-stu-id="98096-121">No.</span></span> <span data-ttu-id="98096-122">، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="98096-122">field, enter a number.</span></span>
    * <span data-ttu-id="98096-123">تحدد أرقام العملية تسلسل المسار.</span><span class="sxs-lookup"><span data-stu-id="98096-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="98096-124">قد تحصل كل خاصية بعملية مسار على قيمة ثابتة أو يتم تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="98096-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="98096-125">يؤدي التعيين إلى سمة إلى تعيين القيمة كجزء من التكوين.</span><span class="sxs-lookup"><span data-stu-id="98096-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="98096-126">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="98096-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="98096-127">تحدد مجموعة المسارات السلوك الأساسي للتكاليف والاستهلاك والإعداد.</span><span class="sxs-lookup"><span data-stu-id="98096-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="98096-128">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="98096-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="98096-129">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="98096-129">Click the Times tab.</span></span>
7. <span data-ttu-id="98096-130">في الحقل "كمية العمليات‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="98096-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="98096-131">حدد العدد الذي سوف تتم معالجته أثناء عملية واحدة.</span><span class="sxs-lookup"><span data-stu-id="98096-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="98096-132">في الحقل "الساعات/الوقت" أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="98096-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="98096-133">أدخل نسبة الوقت.</span><span class="sxs-lookup"><span data-stu-id="98096-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="98096-134">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="98096-134">Select the Set check box.</span></span>
10. <span data-ttu-id="98096-135">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="98096-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="98096-136">حدد وقت المعالجة للكمية التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="98096-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="98096-137">انقر فوق علامة التبويب "متطلبات المورد".</span><span class="sxs-lookup"><span data-stu-id="98096-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="98096-138">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="98096-138">Click Add.</span></span>
13. <span data-ttu-id="98096-139">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="98096-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="98096-140">في الحقل "نوع المتطلب"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="98096-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="98096-141">حدد ما إذا كنت تريد تحديد موارد أو قدرات معينة يجب أن تتوفر لدى الموارد.</span><span class="sxs-lookup"><span data-stu-id="98096-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="98096-142">في الحقل "المتطلب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="98096-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="98096-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="98096-143">Click OK.</span></span>

