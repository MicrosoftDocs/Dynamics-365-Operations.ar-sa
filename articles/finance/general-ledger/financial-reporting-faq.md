---
title: الأسئلة الشائعة حول إعداد التقارير المالية
description: يسرد هذا الموضوع الأسئلة المتعلقة بالتقارير المالية التي قام بها مستخدمون آخرون.
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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923015"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d8a1a-103">الأسئلة الشائعة حول إعداد التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="d8a1a-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="d8a1a-104">يوفر هذا الموضوع إجابات للأسئلة المتداولة حول التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="d8a1a-105">كيف يمكن تقييد الوصول إلى تقرير باستخدام أمان الشجرة؟</span><span class="sxs-lookup"><span data-stu-id="d8a1a-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="d8a1a-106">يوضح المثال التالي كيفية تقييد الوصول إلى تقرير باستخدام أمان الشجرة.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="d8a1a-107">لدى شركة USMF التجريبية تقرير ميزانية عمومية لا يجب أن يكون لدى جميع مستخدمي Financial Reporting حق الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d8a1a-108">لتقييد الوصول، يمكنك استخدام أمان الشجرة لتقييد الوصول إلى تقرير واحد بحيث لا يتمكن سوى مستخدمين معينين من الوصول إلى التقرير.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="d8a1a-109">اتبع الخطوات التالية لتقييد الوصول:</span><span class="sxs-lookup"><span data-stu-id="d8a1a-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="d8a1a-110">قم بتسجيل الدخول إلى Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d8a1a-111">أنشئ تعريف شجرة جديدًا.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-111">Create a new tree definition.</span></span> <span data-ttu-id="d8a1a-112">انتقل إلى **ملف > جديد > تعريف الشجرة**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="d8a1a-113">انقر نقرًا مزدوجًا فوق بند **الملخص** في العمود **أمان الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d8a1a-114">حدد **المستخدمون والمجموعات**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="d8a1a-115">حدد المستخدمين أو المجموعات التي تحتاج إلى الوصول إلى هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="d8a1a-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-116">Select **Save**.</span></span>
7. <span data-ttu-id="d8a1a-117">في تعريف التقرير، أضف تعريف الشجرة الجديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d8a1a-118">في تعريف الشجرة، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d8a1a-119">ضمن **تحديد وحدة التقارير**، حدد **تضمين كل الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="d8a1a-120">كيف أحدد الحسابات التي لا تتطابق مع أرصدتي؟</span><span class="sxs-lookup"><span data-stu-id="d8a1a-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="d8a1a-121">إذا كان لديك تقرير لا يحتوي على أرصدة متطابقة، فإليك بعض الخطوات التي يمكنك اتخاذها لتحديد كل من الحسابات والفروق.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="d8a1a-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="d8a1a-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="d8a1a-123">في Financial Reporter Report Designer، أنشئ تعريف صف جديدًا.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="d8a1a-124">حدد **تحرير > إدراج الصفوف من الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d8a1a-125">حدد **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="d8a1a-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-126">Select **OK**.</span></span>
5. <span data-ttu-id="d8a1a-127">احفظ تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-127">Save the row definition.</span></span>
6. <span data-ttu-id="d8a1a-128">إنشاء تعريف عمود جديد</span><span class="sxs-lookup"><span data-stu-id="d8a1a-128">Create a new column definition</span></span>
7. <span data-ttu-id="d8a1a-129">أنشئ تعريف تقرير جديدًا.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-129">Create a new report definition.</span></span>
8. <span data-ttu-id="d8a1a-130">حدد **الإعدادات** وقم بإلغاء تحديد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="d8a1a-131">أنشئ التقرير.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-131">Generate the report.</span></span> 
10. <span data-ttu-id="d8a1a-132">قم بتصدير التقرير إلى Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d8a1a-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="d8a1a-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="d8a1a-134">في Dynamics 365 Finance، انتقل إلى **دفتر الأستاذ العام > الاستفسارات والتقارير > ميزان المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="d8a1a-135">إعداد المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="d8a1a-135">Set the following parameters:</span></span>
   - <span data-ttu-id="d8a1a-136">**من تاريخ** - أدخل بداية السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="d8a1a-137">**إلى تاريخ** - أدخل التاريخ الذي تنشئ التقرير له.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="d8a1a-138">**البعد المالي** - قم بتعيين هذا الحقل إلى **مجموعة الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="d8a1a-139">حدد **حساب**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="d8a1a-140">قم بتصدير التقرير إلى Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d8a1a-141">يجب أن تكون الآن قادرًا على نسخ البيانات من تقرير Financial Reporter Excel إلى تقرير ميزان المراجعة، حتى تتمكن من مقارنة أعمدة **إقفال الرصيد**.</span><span class="sxs-lookup"><span data-stu-id="d8a1a-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]