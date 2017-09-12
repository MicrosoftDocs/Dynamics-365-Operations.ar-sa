--- 
title: "إنشاء خطة للموقع"
description: "يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="73108-103">إنشاء خطة للموقع</span><span class="sxs-lookup"><span data-stu-id="73108-103">Create a plan for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73108-104">يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين.</span><span class="sxs-lookup"><span data-stu-id="73108-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="73108-105">بعد أن يتم إنشاء اقتراحات التوريد، فإنه يجد الطلبات في الموقع الذي يتم به التخطيط للطلبات وتأكيدها، بدءاً من الطلبات العاجلة.</span><span class="sxs-lookup"><span data-stu-id="73108-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="73108-106">وتكون الطلبات الأكثر إلحاحًا هي تلك التي يجب تأكيدها في التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="73108-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="73108-107">استخدم شركة بيانات العرض التوضيحي USMF لتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="73108-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="73108-108">إنشاء مواد وخطة القدرة لصنف ما</span><span class="sxs-lookup"><span data-stu-id="73108-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="73108-109">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="73108-109">Click Master planning.</span></span>
    * <span data-ttu-id="73108-110">أنت بحاجة إلى الانتقال إلى لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="73108-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="73108-111">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="73108-111">Click Run.</span></span>
3. <span data-ttu-id="73108-112">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="73108-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="73108-113">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="73108-113">Click Filter.</span></span>
5. <span data-ttu-id="73108-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="73108-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="73108-115">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73108-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="73108-116">على سبيل المثال: D0001</span><span class="sxs-lookup"><span data-stu-id="73108-116">Example: D0001</span></span>  
7. <span data-ttu-id="73108-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73108-117">Click OK.</span></span>
8. <span data-ttu-id="73108-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73108-118">Click OK.</span></span>
    * <span data-ttu-id="73108-119">قد تستغرق بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="73108-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="73108-120">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="73108-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="73108-121">تعريف الطلبات العاجلة المخططة للصنف</span><span class="sxs-lookup"><span data-stu-id="73108-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="73108-122">افتح عامل تصفية عمود "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="73108-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="73108-123">طبّق عامل تصفية على الحقل "رقم الصنف" بقيمة "D0001"، باستخدام عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="73108-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="73108-124">افتح عامل تصفية تاريخ الطلب.</span><span class="sxs-lookup"><span data-stu-id="73108-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="73108-125">استخدم عامل تصفية في حقل "تاريخ الطلب"، بقيمة التاريخ الحالي، باستخدام مشغل عامل التصفية "تمامًا مثل".</span><span class="sxs-lookup"><span data-stu-id="73108-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="73108-126">تأكيد كل الطلبات العاجلة للصنف</span><span class="sxs-lookup"><span data-stu-id="73108-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="73108-127">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="73108-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="73108-128">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="73108-128">Click Firm.</span></span>
3. <span data-ttu-id="73108-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73108-129">Click OK.</span></span>


