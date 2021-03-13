---
title: تحديث موازنات الصيانة
description: يشرح هذا الموضوع كيفية تحديث موازنة الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b04549700b51f73a3629fe9cd67a3e1f6c1bafbb
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021005"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="aa1dc-103">تحديث موازنات الصيانة</span><span class="sxs-lookup"><span data-stu-id="aa1dc-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="aa1dc-104">تعرض صفحة **بنود موازنة الصيانة** جميع بنود الموازنة التي تم إنشاؤها للموازنة المحددة في صفحة **موازنات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="aa1dc-105">(لمزيد من المعلومات، راجع [إنشاء موازنات الصيانة](create-maintenance-budget.md).) يمكنك إعادة حساب بنود موازنة الصيانة وتعديلها حتى يتم اعتماد موازنة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="aa1dc-106">بعد مرور فترة الموازنة وترحيل التكاليف في إدارة الأصول، يمكنك أيضًا تحديث بنود الموازنة بواسطة التكاليف الفعلية.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="aa1dc-107">إعادة حساب موازنة صيانة</span><span class="sxs-lookup"><span data-stu-id="aa1dc-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="aa1dc-108">يمكنك إعادة حساب موازنة صيانة في الصفحة **بنود موازنة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="aa1dc-109">عندما تعيد حساب موازنة الصيانة، تُحذف بنود الموازنة الموجودة، ويتم إجراء عملية حسابية جديدة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="aa1dc-110">في الصفحة **بنود موازنة الصيانة**، حدد **إعادة الحساب**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="aa1dc-111">في مربع الحوار **إعادة حساب الموازنة**، أدخل التغييرات المطلوبة للحساب الجديد، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="aa1dc-112">يتم إنشاء بنود الموازنة الجديدة وفقًا للقيم التي تقوم بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="aa1dc-113">تعديل بنود الموازنة</span><span class="sxs-lookup"><span data-stu-id="aa1dc-113">Adjust budget lines</span></span>

<span data-ttu-id="aa1dc-114">بدلاً من إعادة حساب موازنة الصيانة بأكملها، يمكنك تعديل بنود محددة ترتبط بتكاليف الموازنة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="aa1dc-115">في الصفحة **بنود موازنة الصيانة**، حدد البنود التي تريد تحديث تكلفة الموازنة لها.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="aa1dc-116">حدد **تعديل‬**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="aa1dc-117">لإضافة مبلغ إلى البنود المحددة، حدد خانه الاختيار **إضافة تكلفة**، ثم أدخل القيمة في الحقل **إضافة قيمة**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="aa1dc-118">لضرب تكلفة الموازنة على بنود الموازنة المحددة بواسطة عامل، حدد خانة الاختيار **ضرب التكلفة**، وأدخل العامل في حقل **ضرب القيمة**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="aa1dc-119">على سبيل المثال، إذا قمت بإدخال **1.2** في حقل **ضرب القيمة**، فأنت تزيد تكلفة الموازنة على البنود المحددة بقيمة 20 بالمائة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="aa1dc-120">وإذا أدخلت **0.7**، فأنت تقوم بتقليل تكلفة الموازنة على البنود المحددة بنسبة 30 بالمئة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="aa1dc-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-121">Select **OK**.</span></span>

<span data-ttu-id="aa1dc-122">يتم تحديث بنود الموازنة المحددة وفقًا للقيم التي تقوم بتعيينها في الخطوة 3 أو 4.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="aa1dc-123">تحديث التكاليف الفعلية</span><span class="sxs-lookup"><span data-stu-id="aa1dc-123">Update actual costs</span></span>

<span data-ttu-id="aa1dc-124">بعد مرور التواريخ المذكورة على بنود الموازنة وترحيل التكاليف الفعلية في إدارة الأصول، يمكنك تحديث التكاليف الفعلية على موازنة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="aa1dc-125">في الصفحة **بنود موازنة الصيانة**، حدد **تحديث التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="aa1dc-126">في مربع الحوار **حساب‏‎ التكلفة الفعلية**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="aa1dc-127">يتم تحديث حقول **التكلفة الفعلية** على بنود الموازنة إذا تم ترحيل التكاليف الفعلية.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="aa1dc-128">قد يتم إنشاء بنود موازنة جديدة إذا تم إنشاء أنواع أصول جديدة منذ قيامك بإنشاء الموازنة، وإذا تم استخدام أنواع الأصول هذه على الأصول التي تم إنشاء أوامر عمل لها وتم ترحيل تكاليف ذات صلة لها.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="aa1dc-129">تعرض بنود الموازنة الجديدة التكاليف الفعلية فقط، بسبب عدم حساب تكاليف موازنة لها.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="aa1dc-130">للاطلاع على نظرة عام حول التكاليف الفعلية المقسمة إلى تكاليف وقائية وتصحيحية واستثمارية، يمكنك إجراء حساب للفترة نفسها في صفحة **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="aa1dc-131">إضافة بنود الموازنة يدويًا</span><span class="sxs-lookup"><span data-stu-id="aa1dc-131">Manually add budget lines</span></span>

<span data-ttu-id="aa1dc-132">في الصفحة **بنود موازنة الصيانة**، يمكنك إضافة بند موازنة جديد يدويًا من خلال تحديد **جديد** ثم إجراء التحديدات على البند.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="aa1dc-133">فيما يلي بعض الأمثلة عن حالات يكون فيها هذا الأسلوب مفيدًا:</span><span class="sxs-lookup"><span data-stu-id="aa1dc-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="aa1dc-134">أنت تعلم أن تجديد بعض الأصول هو في مرحلة التخطيط في الوقت الحالي، ولكن لم يتم بعد إنشاء المهام ذات الصلة في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="aa1dc-135">ومع ذلك، فأنت ترغب في تضمين تكاليف الموازنة لهذه المهام في موازنة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="aa1dc-136">تم إنشاء أصول أو أنواع أصول جديدة منذ قيامك بوضع موازنة الصيانة، ولكن لم يتم بعد إعداد خطط الصيانة على هذه الأصول أو أنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="aa1dc-137">ومع ذلك، فأنت ترغب في تضمين تكاليف أنواع الأصول هذه في موازنة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
