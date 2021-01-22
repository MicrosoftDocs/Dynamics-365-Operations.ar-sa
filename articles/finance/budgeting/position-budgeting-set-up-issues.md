---
title: اكتشاف مشكلات إعداد موازنة المنصب‬ وإصلاحها
description: توفر هذه المقالة أجوبة على الأسئلة التي قد تواجهك عند تكوين موازنة المنصب‬. وهو يتناول الأسئلة المتداولة حول كيفية إنشاء عناصر تكلفة الموازنة ومجموعات التعويض وشبكات التعويض.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afddc9815ee3864236f93c8400bcf116d5b6cc89
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188500"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="2050a-104">اكتشاف مشكلات إعداد موازنة المنصب‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="2050a-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2050a-105">توفر هذه المقالة أجوبة على الأسئلة التي قد تواجهك عند تكوين موازنة المنصب‬.</span><span class="sxs-lookup"><span data-stu-id="2050a-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="2050a-106">وهو يتناول الأسئلة المتداولة حول كيفية إنشاء عناصر تكلفة الموازنة ومجموعات التعويض وشبكات التعويض.</span><span class="sxs-lookup"><span data-stu-id="2050a-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="2050a-107">لماذا يتعذر عليّ العثور على صفحة منصب التنبؤ‬ في الموارد البشرية؟</span><span class="sxs-lookup"><span data-stu-id="2050a-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="2050a-108">تم نقل مناصب التنبؤ إلى إعداد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="2050a-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="2050a-109">لماذا لا يمكنني حذف عنصر تكلفة موازنة؟</span><span class="sxs-lookup"><span data-stu-id="2050a-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="2050a-110">لا يمكنك حذف عنصر تكلفة الموازنة لأنه تم تعيينه لمنصب تنبؤ واحد.</span><span class="sxs-lookup"><span data-stu-id="2050a-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="2050a-111">قبل أن تتمكن من حذف عنصر تكلفة الموازنة، يجب إزالته من كل مناصب التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="2050a-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="2050a-112">**تلميح:** للعثور عن كافة المناصب التي تم تعيين عنصر تكلفة موازنة لها، حدد عنصر التكلفة في صفحة **عناصر تكلفة الموازنة**، ثم انقر فوق **تحديث المناصب**.</span><span class="sxs-lookup"><span data-stu-id="2050a-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="2050a-113">يتم سرد المناصب التي تستخدم عنصر التكلفة في الشبكة العلوية.</span><span class="sxs-lookup"><span data-stu-id="2050a-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="2050a-114">كيف يمكنني إزالة عنصر تكلفة من مناصب تنبؤ متعددة من دون فتح كل واحد منها؟</span><span class="sxs-lookup"><span data-stu-id="2050a-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="2050a-115">لا يمكنك إزالة عنصر تكلفة.</span><span class="sxs-lookup"><span data-stu-id="2050a-115">You can’t remove a cost element.</span></span> <span data-ttu-id="2050a-116">ولكن إذا قمت بتغيير تاريخي البدء والانتهاء بحيث يقعان خارج تواريخ دورة تخطيط الموازنة، فلن يعود عنصر التكلفة معينًا إلى مناصب التنبؤ في دورة تخطيط الموازنة هذه.</span><span class="sxs-lookup"><span data-stu-id="2050a-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="2050a-117">لإجراء هذا التغيير، افتح عنصر تكلفة الموازنة، ثم، علامة التبويب السريعة **حساب التكلفة**، انقر فوق **تغيير التواريخ**، وغيّر تاريخ السريان أو تاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="2050a-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="2050a-118">ثم انقر فوق **موافق** لكي يتم تلقائيًا تحديث كل مناصب التنبؤ التي تم تعيين عنصر التكلفة لها.</span><span class="sxs-lookup"><span data-stu-id="2050a-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="2050a-119">**تلميح:** إذا استخدمت هذا الأسلوب، فيجب أن تدرك أنه يزيل **كل** مناصب التنبؤ حيث لم تعد تواريخ البدء والانتهاء الموجودة ضمن النطاق المناسب.</span><span class="sxs-lookup"><span data-stu-id="2050a-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="2050a-120">إذا لم يكن هذا التأثير ما ترغب في الحصول عليه، فستحتاج إلى فتح كل منصب تنبؤ تريد إزالة عنصر تكلفة الموازنة منه وإجراء التغيير يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2050a-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="2050a-121">لماذا لا يمكنني إدخال مبلغ سنوي على علامة التبويب السريعة "حساب التكلفة" لعنصر تكلفة الموازنة؟</span><span class="sxs-lookup"><span data-stu-id="2050a-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="2050a-122">لا يمكنك إدخال مبلغ سنوي إذا تضمنت علامة التبويب السريعة **أساس الحساب‬** عناصر تكلفة الموازنة، لأن النظام يحتاج إلى نسبة مئوية لكي يتمكن من حساب القيمة.</span><span class="sxs-lookup"><span data-stu-id="2050a-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="2050a-123">لتغيير القيمة، يجب إزالة كل عناصر تكلفة الموازنة من علامة التبويب السريعة **أساس الحساب**.</span><span class="sxs-lookup"><span data-stu-id="2050a-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="2050a-124">لماذا لا يمكنني تغيير نوع تكلفة الموازنة من الأرباح إلى نوع تكلفة موازنة آخر؟</span><span class="sxs-lookup"><span data-stu-id="2050a-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="2050a-125">تستخدم بعض عناصر تكلفة الموازنة عنصر تكلفة الأرباح كأساس حساب.</span><span class="sxs-lookup"><span data-stu-id="2050a-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="2050a-126">لتغيير حقل **نوع تكلفة الموازنة**، أزل عنصر تكلفة الأرباح من علامة التبويب السريعة **أساس الحساب** لجميع عناصر تكلفة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="2050a-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="2050a-127">لماذا يتعذر تغيير التاريخ في بنود عنصر تكلفة الموازنة لعنصر تكلفة موازنة؟</span><span class="sxs-lookup"><span data-stu-id="2050a-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="2050a-128">لا يمكنك تغيير التاريخ على بند عنصر تكلفة الموازنة عند استخدام عنصر تكلفة موازنة بواسطة منصب تنبؤ.</span><span class="sxs-lookup"><span data-stu-id="2050a-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="2050a-129">من شأن هذا القيد أن يساعد على ضمان وجود مناصب التنبؤ دائمًا ضمن إرشادات عنصر تكلفة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="2050a-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="2050a-130">لتغيير التاريخ، على علامة التبويب السريعة **حساب التكلفة**، انقر فوق **تغيير التواريخ**، وأدخل التواريخ الجديدة.</span><span class="sxs-lookup"><span data-stu-id="2050a-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="2050a-131">ثم انقر فوق **موافق** لتحديث المناصب التي تم تعيين عنصر التكلفة لها.</span><span class="sxs-lookup"><span data-stu-id="2050a-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="2050a-132">لماذا لا يمكنني تغيير تكاليف عنصر تكلفة الموازنة في صفحة مجموعة التعويض؟</span><span class="sxs-lookup"><span data-stu-id="2050a-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="2050a-133">يمكنك إنشاء عناصر تكلفة الموازنة وتغييرها فقط في صفحة **عناصر تكلفة الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="2050a-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="2050a-134">لماذا أتلقى رسالة خطأ عند تغيير التواريخ لعنصر تكلفة في منصب تنبؤ؟</span><span class="sxs-lookup"><span data-stu-id="2050a-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="2050a-135">يجب أن تقع التواريخ في بند عنصر تكلفة منصب التنبؤ ضمن النطاقات التالية:</span><span class="sxs-lookup"><span data-stu-id="2050a-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="2050a-136">تواريخ التنشيط والتقاعد للمنصب.</span><span class="sxs-lookup"><span data-stu-id="2050a-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="2050a-137">تواريخ انتهاء الصلاحية وتنشيط عنصر تكلفة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="2050a-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="2050a-138">تواريخ بدء وانتهاء دورة الموازنة المرتبطة بعملية تخطيط الموازنة لمنصب التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="2050a-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>



