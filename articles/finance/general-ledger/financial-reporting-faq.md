---
title: الأسئلة الشائعة حول إعداد التقارير المالية
description: يسرد هذا الموضوع الأسئلة المتعلقة بالتقارير المالية التي قام بها مستخدمون آخرون.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070208"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="a896f-103">الأسئلة الشائعة حول إعداد التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="a896f-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="a896f-104">يسرد هذا الموضوع الأسئلة المتعلقة بالتقارير المالية التي قام بها مستخدمون آخرون.</span><span class="sxs-lookup"><span data-stu-id="a896f-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="a896f-105">كيف يمكن تقييد الوصول إلى تقرير باستخدام "أمان الشجرة"؟</span><span class="sxs-lookup"><span data-stu-id="a896f-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="a896f-106">السيناريو: تحتوي الشركة التجريبية USMF على تقرير الميزانية العمومية التي لا ترغب في أن يتمكن كافة مستخدمي التقارير المالية من عرضها في D365.</span><span class="sxs-lookup"><span data-stu-id="a896f-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="a896f-107">الحل: يمكنك استخدام أمان الشجرة لتقييد الوصول إلى تقرير واحد بحيث يتمكن بعض المستخدمين فقط من الوصول إلى التقرير.</span><span class="sxs-lookup"><span data-stu-id="a896f-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="a896f-108">التسجيل في مصمم تقرير التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="a896f-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="a896f-109">إنشاء تعريف شجرة جديد (الملف | جديد | تعريف الشجرة) ا.</span><span class="sxs-lookup"><span data-stu-id="a896f-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="a896f-110">انقر نقرًا مزدوجًا فوق بند **الملخص** في العمود **أمان الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="a896f-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="a896f-111">i</span><span class="sxs-lookup"><span data-stu-id="a896f-111">i.</span></span>    <span data-ttu-id="a896f-112">انقر فوق "المستخدمون والمجموعات".</span><span class="sxs-lookup"><span data-stu-id="a896f-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="a896f-113">1. حدد المستخدمين أو المجموعة التي ترغب في الوصول إلى هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="a896f-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="a896f-114">[![شاشة المستخدم](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="a896f-115">[![شاشة الأمان](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="a896f-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="a896f-116">b.</span><span class="sxs-lookup"><span data-stu-id="a896f-116">b.</span></span>    <span data-ttu-id="a896f-117">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a896f-117">Click **Save**.</span></span>
  
<span data-ttu-id="a896f-118">[![الزر حفظ](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="a896f-119">في تعريف التقرير قم بإضافة تعريف الشجرة الجديد</span><span class="sxs-lookup"><span data-stu-id="a896f-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="a896f-120">[![نموذج تعريف الشجرة](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="a896f-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="a896f-121">A.</span><span class="sxs-lookup"><span data-stu-id="a896f-121">A.</span></span>  <span data-ttu-id="a896f-122">في "تعريف الشجرة" انقر فوق "الإعداد" وضمن "تحديد وحدة التقرير" حدد "تضمين كل الوحدات"</span><span class="sxs-lookup"><span data-stu-id="a896f-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="a896f-123">[![نموذج تحديد وحدة التقارير](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="a896f-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="a896f-124">**قبل:** [![قبل لقطة الشاشة](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="a896f-125">**بعد:** [![بعد لقطة الشاشة](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="a896f-126">ملاحظة: سبب الرسالة أعلاه ليس لدى المستخدم حق الوصول إلى هذا التقرير بعد تطبيق أمان الوحدة</span><span class="sxs-lookup"><span data-stu-id="a896f-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="a896f-127">كيف يمكنني تحديد الحسابات التي لا تطابق الأرصدة الخاصة بي في الـ D365؟</span><span class="sxs-lookup"><span data-stu-id="a896f-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="a896f-128">عندما يكون لديك تقرير لا يطابق ما تتوقعه في D365، ففيما يلي بعض الخطوات التي يمكنك اتخاذها لتحديد هذه الحسابات والتباينات.</span><span class="sxs-lookup"><span data-stu-id="a896f-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="a896f-129">في مصمم تقرير التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="a896f-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="a896f-130">إنشاء تعريف صف جديد a.</span><span class="sxs-lookup"><span data-stu-id="a896f-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="a896f-131">انقر فوق "تحرير" | ، ‬‏‫إدراج الصفوف من الأبعاد i.</span><span class="sxs-lookup"><span data-stu-id="a896f-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="a896f-132">حدد الحساب الرئيسي [![تحديد الشاشة الرئيسية_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="a896f-133">ii.</span><span class="sxs-lookup"><span data-stu-id="a896f-133">ii.</span></span> <span data-ttu-id="a896f-134">انقر فوق "موافق" b.</span><span class="sxs-lookup"><span data-stu-id="a896f-134">Click Ok b.</span></span>    <span data-ttu-id="a896f-135">احفظ "تعريف الصف".</span><span class="sxs-lookup"><span data-stu-id="a896f-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="a896f-136">إنشاء تعريف عمود جديد     [![إنشاء تعريف عمود جديد](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="a896f-137">إنشاء تعريف تقرير جديد a.</span><span class="sxs-lookup"><span data-stu-id="a896f-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="a896f-138">انقر فوق "الإعدادات" وقم بإلغاء تحديد [![نموذج الإعدادات](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="a896f-139">قم بإنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="a896f-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="a896f-140">قم بتصدير التقرير إلى Excel.</span><span class="sxs-lookup"><span data-stu-id="a896f-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="a896f-141">في D365:</span><span class="sxs-lookup"><span data-stu-id="a896f-141">In D365:</span></span> 
1.  <span data-ttu-id="a896f-142">انقر فوق دفتر الأستاذ العام | الاستعلامات والتقارير | ميزان المراجعة a.</span><span class="sxs-lookup"><span data-stu-id="a896f-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="a896f-143">محددات i.</span><span class="sxs-lookup"><span data-stu-id="a896f-143">Parameters i.</span></span>  <span data-ttu-id="a896f-144">من "التاريخ": بدء السنة المالية ii.</span><span class="sxs-lookup"><span data-stu-id="a896f-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="a896f-145">إلى تاريخ: التاريخ الذي أنشأت فيه التقرير لـ iii.</span><span class="sxs-lookup"><span data-stu-id="a896f-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="a896f-146">مجموعة الأبعاد المالية "مجموعة الحساب الرئيسي"، [![نموذج الحساب الرئيسي](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="a896f-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="a896f-147">b.</span><span class="sxs-lookup"><span data-stu-id="a896f-147">b.</span></span>    <span data-ttu-id="a896f-148">انقر فوق "حساب".</span><span class="sxs-lookup"><span data-stu-id="a896f-148">Click Calculate</span></span>

2.  <span data-ttu-id="a896f-149">تصدير التقرير إلى Excel</span><span class="sxs-lookup"><span data-stu-id="a896f-149">Export the report to Excel</span></span>

<span data-ttu-id="a896f-150">الآن يمكنك نسخ البيانات من تقرير FR Excel والي تقرير ميزان مراجعة D365 ومقارنة الأعمدة "رصيد الاقفال".</span><span class="sxs-lookup"><span data-stu-id="a896f-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>
