---
title: تغيير قواعد الإهلاك للأصول الثابتة المتعددة
description: تقوم هذه المهمة بتحديث قواعد الإهلاك لمجموعة من الأصول الثابتة المحددة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39930134782b40de05a92a6ad51c4f628f304a78
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142882"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="4b717-103">تغيير قواعد الإهلاك للأصول الثابتة المتعددة</span><span class="sxs-lookup"><span data-stu-id="4b717-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b717-104">تقوم هذه المهمة بتحديث قواعد الإهلاك لمجموعة من الأصول الثابتة المحددة.</span><span class="sxs-lookup"><span data-stu-id="4b717-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="4b717-105">يستخدم دليل المهمة هذا شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="4b717-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="4b717-106">انتقل إلى الأصول الثابتة > المهام الدورية > تحديث شامل</span><span class="sxs-lookup"><span data-stu-id="4b717-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="4b717-107">في الحقل "دفتر الإهلاك"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4b717-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4b717-108">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4b717-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4b717-109">في الحقل "بداية التضمين بالخدمة‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="4b717-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="4b717-110">في الحقل "نهاية التضمين بالخدمة‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="4b717-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="4b717-111">سيتم تحديث فقط الأصول التي تُعد جزءًا من دفتر الإهلاك المحدد والتي تم وضعها في الخدمة بين هذه التواريخ.</span><span class="sxs-lookup"><span data-stu-id="4b717-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="4b717-112">في الحقل "قواعد الإهلاك الحالية‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="4b717-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="4b717-113">سيتم تحديث فقط الأصول التي لها قواعد إهلاك حالية.</span><span class="sxs-lookup"><span data-stu-id="4b717-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="4b717-114">في الحقل "قواعد إهلاك جديدة‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="4b717-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="4b717-115">تحقق من طباعة التقرير في الوجهة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="4b717-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="4b717-116">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="4b717-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="4b717-117">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="4b717-117">Click Filter.</span></span>
10. <span data-ttu-id="4b717-118">في القائمة، حدد "مجموعة الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="4b717-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="4b717-119">في الحقل "المعايير"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4b717-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4b717-120">حدد مجموعة الأصول الثابتة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="4b717-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="4b717-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4b717-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4b717-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4b717-122">Click OK.</span></span>
15. <span data-ttu-id="4b717-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4b717-123">Click OK.</span></span>
    *  <span data-ttu-id="4b717-124">تظهر نتائج العملية على تقرير التحديث الشامل.</span><span class="sxs-lookup"><span data-stu-id="4b717-124">Results of the process are shown on the Mass update report.</span></span>     

