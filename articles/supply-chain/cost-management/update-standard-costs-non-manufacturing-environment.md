---
title: تحديث التكاليف المعيارية في بيئة غير مصنعة
description: توفر هذه المقالة إرشادات لتحديث التكاليف المعيارية في بيئة غير مصنعة.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421316"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="56b91-103">تحديث التكاليف المعيارية في بيئة غير مصنعة</span><span class="sxs-lookup"><span data-stu-id="56b91-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56b91-104">توفر هذه المقالة إرشادات لتحديث التكاليف المعيارية في بيئة غير مصنعة.</span><span class="sxs-lookup"><span data-stu-id="56b91-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="56b91-105">تفترض الإرشادات التالية استخدام نهج ثنائي الإصدار لتحديث التكلفة المعيارية.</span><span class="sxs-lookup"><span data-stu-id="56b91-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="56b91-106">في هذا النهج، يحتوي إصدار تكاليف على التكاليف المعيارية التي تم تحديدها أصلاً للفترة المجمدة، ويحتوي إصدار التكاليف الثاني على التحديثات التزايدية.</span><span class="sxs-lookup"><span data-stu-id="56b91-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="56b91-107">يتم إدخال كل تحديث كسجل تكلفة مضمّن في إصدار التكاليف الثاني، وهو في نهاية الأمر ممكّن.</span><span class="sxs-lookup"><span data-stu-id="56b91-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="56b91-108">هناك حل بديل، حيث يستخدم نهج أحادي المصدر مجموعة التكاليف المعيارية التي تم تعريفها في الأصل.</span><span class="sxs-lookup"><span data-stu-id="56b91-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="56b91-109">يتطلب النهج الثنائي المصدر أن تقوم بتعريف إصدار تكاليف آخر.</span><span class="sxs-lookup"><span data-stu-id="56b91-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="56b91-110">فيما يلي الإرشادات المتعلقة بتعريف إصدار التكاليف هذا:</span><span class="sxs-lookup"><span data-stu-id="56b91-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="56b91-111">تعيين نوع التكلفة إلى **التكاليف القياسية**.</span><span class="sxs-lookup"><span data-stu-id="56b91-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="56b91-112">تعيين معرّف ذي معنىً يشير إلى محتويات إصدار التكاليف، مثل **2016-UPDATES**.</span><span class="sxs-lookup"><span data-stu-id="56b91-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="56b91-113">التأكد من أن المحتوى يتضمن سجلات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="56b91-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="56b91-114">السماح بإدخال سجلات التكلفة لكافة المواقع.</span><span class="sxs-lookup"><span data-stu-id="56b91-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="56b91-115">إذا قمت بتحديد موقع، فيمكن إدخال سجلات التكلفة لهذا الموقع فقط.</span><span class="sxs-lookup"><span data-stu-id="56b91-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="56b91-116">تحديد مبدأ الاحتياطي **بلا**.</span><span class="sxs-lookup"><span data-stu-id="56b91-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="56b91-117">ينطبق مبدأ الاحتياطي فقط على حسابات التكلفة للأصناف المصنعة.</span><span class="sxs-lookup"><span data-stu-id="56b91-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="56b91-118">لتصحيح التكاليف المعيارية للأصناف الجديدة أو تسويتها أو تحديثها، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="56b91-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="56b91-119">استخدم صفحة **إعداد** **إصدار التكاليف** لتمكين إدخال بيانات التكلفة في إصدار التكاليف الثاني.</span><span class="sxs-lookup"><span data-stu-id="56b91-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="56b91-120">اختياريًا، امنع تنشيط التكاليف المعلقة، حيث يتم السماح بالتنشيط بعد القيام بتعريف التكاليف المعلقة بالكامل وبدقة.</span><span class="sxs-lookup"><span data-stu-id="56b91-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="56b91-121">يمكنك أيضًا وبشكل اختياري إدخال تاريخ في الحقل **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="56b91-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="56b91-122">بصفة عامة، استخدم التاريخ الذي تريد تنشيط التحديثات التزايدية فيه.</span><span class="sxs-lookup"><span data-stu-id="56b91-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="56b91-123">أو، اترك الحقل **من تاريخ** فارغًا لإصدار التكاليف، ثم أدخل تاريخًا في الحقل **من تاريخ** لكل سجل تكلفة.</span><span class="sxs-lookup"><span data-stu-id="56b91-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="56b91-124">استخدم صفحة **سعر الصنف** لإدخال التحديثات كسجلات تكلفة الصنف المضمنة في إصدار التكاليف الثاني.</span><span class="sxs-lookup"><span data-stu-id="56b91-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="56b91-125">استخدم تقرير **أسعار الأصناف‬** للتحقق من اكتمال سجلات تكلفة الأصناف المضمنة في إصدار التكاليف الثاني ودقتها.</span><span class="sxs-lookup"><span data-stu-id="56b91-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="56b91-126">استخدم صفحة **صيانة إصدار حساب التكلفة‬** لتغيير علامة الحظر للسماح بتنشيط سجلات التكلفة المعلقة المضمنة في إصدار التكاليف الثاني.</span><span class="sxs-lookup"><span data-stu-id="56b91-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="56b91-127">استخدم صفحة **تنشيط الأسعار** (التي تفتحها من صفحة **صيانة إصدار حساب التكلفة**) لتنشيط كل سجلات تكلفة الأصناف المعلقة المضمنة في إصدار التكاليف الثاني.</span><span class="sxs-lookup"><span data-stu-id="56b91-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="56b91-128">يمكنك أيضًا تنشيط سجلات التكاليف المعلقة الخاصة بالأصناف الفردية بالنقر فوق الزر **تنشيط السعر المعلق‬** في صفحة **سعر الصنف**.</span><span class="sxs-lookup"><span data-stu-id="56b91-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="56b91-129">لمنع صيانة بيانات إضافية، استخدم صفحة **صيانة إصدار حساب التكلفة‬** لتغيير علامات الحظر المضمنة في إصدار التكاليف الثاني.</span><span class="sxs-lookup"><span data-stu-id="56b91-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="56b91-130">ستقوم نهج التأمين بمنع إدخال التكاليف المعلقة الجديدة وتنشيط التكاليف المعلقة.</span><span class="sxs-lookup"><span data-stu-id="56b91-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>




