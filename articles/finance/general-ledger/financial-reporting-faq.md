---
title: الأسئلة المتداولة حول إعداد التقارير المالية
description: يوفر هذا الموضوع إجابات عن بعض الاسئلة المتداولة حول إعداد التقارير المالية.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266623"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="8c9b3-103">الأسئلة المتداولة حول إعداد التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="8c9b3-103">Financial reporting FAQ</span></span>

<span data-ttu-id="8c9b3-104">يوفر هذا الموضوع إجابات عن الاسئلة المتداولة حول إعداد التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="8c9b3-105">كيف يمكن تقييد الوصول إلى تقرير باستخدام أمان الشجرة؟</span><span class="sxs-lookup"><span data-stu-id="8c9b3-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="8c9b3-106">يوضح المثال التالي كيفية تقييد الوصول إلى تقرير باستخدام أمان الشجرة.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="8c9b3-107">لدى شركه العرض التوضيحي USMF تقرير **ميزانية عمومية** لا يجب أن يكون لدى جميع مستخدمي التقارير المالية حق الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="8c9b3-108">يمكنك استخدام أمان الشجرة لتقييد الوصول إلى تقرير واحد بحيث يتمكن بعض المستخدمين فقط من الوصول إلى إليه.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="8c9b3-109">سجل دخولك إلى Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="8c9b3-110">حدد **ملف \> جديد \> تعريف الشجرة** لإنشاء تعريف شجرة جديد.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="8c9b3-111">اضغط مرتين (أو انقر نقرًا مزدوجًا) على بند **الملخص** في العمود **أمان الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="8c9b3-112">حدد **المستخدمون والمجموعات**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="8c9b3-113">حدد المستخدمين أو المجموعات التي تحتاج إلى الوصول إلى التقرير.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="8c9b3-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-114">Select **Save**.</span></span>
7. <span data-ttu-id="8c9b3-115">في تعريف التقرير، أضف تعريف الشجرة الجديد.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="8c9b3-116">في تعريف الشجرة، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="8c9b3-117">بعد ذلك، ضمن **تحديد وحدة التقارير**، حدد **تضمين كل الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="8c9b3-118">كيف أحدد الحسابات التي لا تتطابق مع أرصدتي؟</span><span class="sxs-lookup"><span data-stu-id="8c9b3-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="8c9b3-119">إذا كان لديك تقرير لا يحتوي على أرصدة متطابقة، فاستخدم الإجراءات التالية لتحديد كل حساب وفرق.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="8c9b3-120">في Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="8c9b3-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="8c9b3-121">أنشئ تعريف صف جديدًا.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-121">Create a new row definition.</span></span>
2. <span data-ttu-id="8c9b3-122">حدد **تحرير \> إدراج الصفوف من الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="8c9b3-123">حدد **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="8c9b3-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-124">Select **OK**.</span></span>
5. <span data-ttu-id="8c9b3-125">احفظ تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-125">Save the row definition.</span></span>
6. <span data-ttu-id="8c9b3-126">أنشئ تعريف عمود جديدًا.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-126">Create a new column definition.</span></span>
7. <span data-ttu-id="8c9b3-127">أنشئ تعريف تقرير جديدًا.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-127">Create a new report definition.</span></span>
8. <span data-ttu-id="8c9b3-128">حدد **الإعدادات** وقم بإلغاء تحديد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="8c9b3-129">أنشئ التقرير.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-129">Generate the report.</span></span> 
10. <span data-ttu-id="8c9b3-130">قم بتصدير التقرير إلى Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="8c9b3-131">في Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8c9b3-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="8c9b3-132">انتقل إلى **دفتر الأستاذ العام \> الاستعلامات والتقارير \> ميزان المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="8c9b3-133">قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9b3-133">Set the following fields:</span></span>

    - <span data-ttu-id="8c9b3-134">**من تاريخ** - أدخل تاريخ بدء السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="8c9b3-135">**إلى تاريخ** - أدخل التاريخ الذي تنشئ التقرير له.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="8c9b3-136">**البُعد المالي** - قم بتعيين هذا الحقل إلى **مجموعة الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="8c9b3-137">حدد **حساب**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="8c9b3-138">قم بتصدير التقرير إلى Excel.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-138">Export the report to Excel.</span></span>

<span data-ttu-id="8c9b3-139">يجب أن تتمكن الآن من نسخ البيانات من تقرير Financial Reporter Excel إلى تقرير **ميزان المراجعة**، حتى تتمكن من مقارنة أعمدة **رصيد الإقفال**.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="8c9b3-140">أثناء قيامي بتصميم تقرير في Report Designer، أو عند قيامي بإنشاء تقرير مالي، تلقيت الرسالة التالية: "تعذر إكمال العملية بسبب مشكلة في اطار عمل موفر البيانات."</span><span class="sxs-lookup"><span data-stu-id="8c9b3-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="8c9b3-141">كيف يمكنني الرد على هذه المشكلة؟</span><span class="sxs-lookup"><span data-stu-id="8c9b3-141">How should I respond?</span></span>

<span data-ttu-id="8c9b3-142">تشير الرسالة إلى حدوث مشكلة عندما حاول النظام استرداد بيانات التعريف المالية من متجر البيانات بينما كنت تستخدم التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="8c9b3-143">هناك طريقتان للرد على هذه المشكلة:</span><span class="sxs-lookup"><span data-stu-id="8c9b3-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="8c9b3-144">راجع حالة تكامل البيانات عن طريق الانتقال إلى **أدوات \> حالة التكامل** في Report Designer.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="8c9b3-145">إذا لم يكن التكامل مكتملاً، فانتظر ريثما يكتمل.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="8c9b3-146">ثم حاول من جديد تنفيذ الإجراء الذي كنت تعمل على تنفيذه عندما تلقيت الرسالة.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="8c9b3-147">اتصل بالدعم لتحديد المشكلة والتعامل معها.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="8c9b3-148">يُحتمل وجود بيانات غير متناسقة في النظام.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="8c9b3-149">بإمكان مهندسي الدعم مساعدتك في تحديد المشكلة الموجودة على الخادم والبحث عن بيانات معينة قد تحتاج إلى تحديث.</span><span class="sxs-lookup"><span data-stu-id="8c9b3-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
