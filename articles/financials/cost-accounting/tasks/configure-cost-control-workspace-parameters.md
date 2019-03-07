---
title: تكوين معلمات مساحة عمل مراقبة التكلفة
description: استخدم هذا الإجراء لتكوين مساحة عمل التحكم في التكلفة لتمكين المدراء من مستويات مختلفة في المؤسسة من الحصول على نظرة أعمق على كائنات التكلفة، مثل مراكز التكلفة ومجموعات المنتجات.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f9c50bb0ab7f1b0afadfabb687932f96ab6e689
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "308565"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="0b064-103">تكوين معلمات مساحة عمل مراقبة التكلفة</span><span class="sxs-lookup"><span data-stu-id="0b064-103">Configure cost control workspace parameters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b064-104">استخدم هذا الإجراء لتكوين مساحة عمل التحكم في التكلفة لتمكين المدراء من مستويات مختلفة في المؤسسة من الحصول على نظرة أعمق على كائنات التكلفة، مثل مراكز التكلفة ومجموعات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="0b064-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="0b064-105">تم استخدام شركة العرض التوضيحي USP2 لإنشاء هذا التسجيل.</span><span class="sxs-lookup"><span data-stu-id="0b064-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="0b064-106">انتقل إلى محاسبة التكاليف > الإعداد > تكوين مساحة عمل مراقبة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0b064-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="0b064-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b064-107">Click New.</span></span>
3. <span data-ttu-id="0b064-108">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b064-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0b064-109">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b064-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b064-110">حدد "نعم" في الحقل "منشور".</span><span class="sxs-lookup"><span data-stu-id="0b064-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="0b064-111">إذا قمت بتعيين هذا الخيار إلى "نعم"، سيتمكن المستخدمون الذين تم تعيين أحد هذه الأدوار لهم من مشاهدة التقرير في مساحة عمل التحكم في التكلفة: مدير محاسبة التكاليف أو محاسب التكاليف أو موظف محاسبة التكاليف أو مراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="0b064-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="0b064-112">إذا قمت بتعيين هذا الخيار إلى "لا"، فلن يتمكن من مشاهدة التقرير في مساحة عمل التحكم في التكلفة‬ سوى الموظفين الذين تم تعيين أحد هذه الأدوار لهم‬: مدير محاسبة التكاليف أو محاسب التكاليف أو موظف محاسبة التكاليف أو مراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="0b064-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="0b064-113">قم بتوسيع مقطع "تصفية البيانات‬".</span><span class="sxs-lookup"><span data-stu-id="0b064-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="0b064-114">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="0b064-115">في حقل "الإصدار الأصلي للموازنة‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="0b064-116">في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="0b064-117">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="0b064-118">قم بتوسيع المقطع "تعيين سجلات الحساب".</span><span class="sxs-lookup"><span data-stu-id="0b064-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="0b064-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b064-119">Click New.</span></span>
13. <span data-ttu-id="0b064-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b064-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0b064-121">في حقل "فترة التقويم المالي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="0b064-122">في حقل "الإصدار الفعلي‬"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b064-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="0b064-123">قم بتوسيع المقطع "الفترات المالية لكل عمود‬".</span><span class="sxs-lookup"><span data-stu-id="0b064-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="0b064-124">حدد "نعم" في حقل "الفترة الحالية‬‬".</span><span class="sxs-lookup"><span data-stu-id="0b064-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="0b064-125">قم بتوسيع المقطع "الأعمدة المراد عرضها للتكاليف".</span><span class="sxs-lookup"><span data-stu-id="0b064-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="0b064-126">حدد "نعم" في حقل "التكلفة الثابتة".</span><span class="sxs-lookup"><span data-stu-id="0b064-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="0b064-127">حدد "نعم" في حقل "التكلفة المتغيرة".</span><span class="sxs-lookup"><span data-stu-id="0b064-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="0b064-128">حدد "نعم" في حقل "إجمالي التكلفة".</span><span class="sxs-lookup"><span data-stu-id="0b064-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="0b064-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0b064-129">Click Save.</span></span>
23. <span data-ttu-id="0b064-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0b064-130">Close the page.</span></span>
24. <span data-ttu-id="0b064-131">انتقل إلى محاسبة التكاليف > مساحات العمل > مراقبة التكاليف‬.</span><span class="sxs-lookup"><span data-stu-id="0b064-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="0b064-132">حدد كشف حساب لمعرفة التكاليف الثابتة والمتغيرة والإجمالية وغير المصنف للفترات المالية المحددة.</span><span class="sxs-lookup"><span data-stu-id="0b064-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="0b064-133">في حقل "فترة التقويم المالي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="0b064-134">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0b064-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0b064-135">بعد تحديد التدرج الهرمي لبعد كائن تكلفة، قم بتوسيع التدرج الهرمي لبعد عنصر التكلفة لعرض قيم التكلفة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0b064-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="0b064-136">على سبيل المثال، يمكنك توسيع التدرج الهرمي إلى تكاليف التصنيع لرؤية القيمة.</span><span class="sxs-lookup"><span data-stu-id="0b064-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

