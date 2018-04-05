---
title: "تخطيط الموازنة"
description: "يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations في مجال تخطيط الموازنة. الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين.  سيركز هذا المعمل على وجه التحديد على العمليات التجارية أو مهام العمل التالية: - إنشاء التدرج الهرمي التنظيمي لتخطيط الموازنة وتكوين أمان المستخدم - تعريف سيناريوهات خطة الموازنة وأعمدة خطة الموازنة وتخطيطات وقوالب Excel - إنشاء عملية تخطيط الموازنة وتنشيطها - إنشاء مستند خطة الموازنة بسحب القيم الفعلية من دفتر الأستاذ العام - استخدام التوزيعات لضبط بيانات مستند خطة الموازنة - تحرير بيانات مستند خطة الموازنة في Excel"
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 59781da7681ece1c0c013f59e0d1a5d7efc51c3a
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning"></a><span data-ttu-id="b46e6-105">تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="b46e6-105">Budget planning</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b46e6-106">يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations في مجال تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-106">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 for Finance and Operations functionality updates in Budget planning area.</span></span> <span data-ttu-id="b46e6-107">الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="b46e6-107">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="b46e6-108">سيركز هذا المعمل على وجه التحديد على العمليات التجارية أو مهام العمل التالية: - إنشاء التدرج الهرمي التنظيمي لتخطيط الموازنة وتكوين أمان المستخدم - تعريف سيناريوهات خطة الموازنة وأعمدة خطة الموازنة وتخطيطات وقوالب Excel - إنشاء عملية تخطيط الموازنة وتنشيطها - إنشاء مستند خطة الموازنة بسحب القيم الفعلية من دفتر الأستاذ العام - استخدام التوزيعات لضبط بيانات مستند خطة الموازنة - تحرير بيانات مستند خطة الموازنة في Excel</span><span class="sxs-lookup"><span data-stu-id="b46e6-108">This lab will focus specifically on the following business processes or tasks -    - Creating organizational hierarchy for budget planning and configuring user security   - Defining budget plan scenarios, budget plan columns, layouts and Excel templates   - Creating and activating budget planning process   - Creating budget plan document by pulling in actuals from General ledger   - Using allocations to adjust budget plan document data   - Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="b46e6-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="b46e6-109">Prerequisites</span></span> 
------------------

<span data-ttu-id="b46e6-110">بالنسبة إلى البرنامج التعليمي، سوف تحتاج إلى الوصول إلى بيئة Finance and Operations مع بيانات تجريبية لشركة التعمير، ويتم توفيرها كمسؤول في المثيل.</span><span class="sxs-lookup"><span data-stu-id="b46e6-110">For this tutorial, you’ll need to access the Finance and Operations environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="b46e6-111">فلا تستخدم المستعرض الخاص لهذا المعمل - قم بتسجيل الخروج من أي حساب آخر في المستعرض إذا لزم الأمر وتسجيل الدخول باستخدام بيانات اعتماد مسؤول Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b46e6-111">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with Finance and Operations administrator credentials.</span></span> <span data-ttu-id="b46e6-112">عند تسجيل الدخول إلى Finance and Operations، **يجب** عليك تحديد خانة اختيار "الاستمرار في تسجيل الدخول".</span><span class="sxs-lookup"><span data-stu-id="b46e6-112">When signing into Finance and Operations, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="b46e6-113">ويؤدي هذا إلى إنشاء ملف تعريف ارتباط دائم يحتاج تطبيق Excel إليه حاليًا.</span><span class="sxs-lookup"><span data-stu-id="b46e6-113">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="b46e6-114">وفي حالة تسجيل الدخول إلى Finance and Operations باستخدام مستعرض غير IE، فستتم مطالبتك بتسجيل الدخول في تطبيق Excel.</span><span class="sxs-lookup"><span data-stu-id="b46e6-114">If you sign in to the Finance and Operations using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="b46e6-115">وعند النقر فوق "تسجيل الدخول" في تطبيق Excel، سيتم فتح نافذة IE المنبثقة وعند تسجيل الدخول، **يجب** عليك تحديد خانة الاختيار "الاستمرار في تسجيل الدخول".</span><span class="sxs-lookup"><span data-stu-id="b46e6-115">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="b46e6-116">إذا كان النقر فوق "تسجيل الدخول" في تطبيق Excel لا يبدو أنه يفعل أي شيء، فيجب مسح ذاكرة التخزين المؤقت لملف تعريف ارتباط مستعرض IE.</span><span class="sxs-lookup"><span data-stu-id="b46e6-116">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="b46e6-117">**نظرة عامة على السيناريو**</span><span class="sxs-lookup"><span data-stu-id="b46e6-117">**Scenario overview**</span></span>
<span data-ttu-id="b46e6-118">تعمل ليلى كمدير مالي في شركة الرشيدي المحدودة في القاهرة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-118">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="b46e6-119">ومع اقتراب العام المالي 2016، تحتاج إلى العمل في إعداد موازنة الشركة للسنة المقبلة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-119">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="b46e6-120">يبدو إعداد الموازنة على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="b46e6-120">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="b46e6-121">تستخدم ليلى المبالغ الفعلية للسنة السابقة كنقطة بداية لإنشاء الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-121">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="b46e6-122">واستناداً إلى المبالغ الفعلية في العام السابق، تقوم بإنشاء تقديرات لمدة 12 شهرًا في السنة المقبلة</span><span class="sxs-lookup"><span data-stu-id="b46e6-122">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="b46e6-123">وتراجع ليلى الموازنة مع المدير المالي.</span><span class="sxs-lookup"><span data-stu-id="b46e6-123">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="b46e6-124">وبمجرد أن تتنهي من المراجعة، تقوم بإجراء التعديلات اللازمة لخطة الموازنة وتتولى الصياغة النهائية لإعداد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-124">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="b46e6-125">يبدو مخطط تكوين التخطيط للموازنة لهذا السيناريو على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="b46e6-125">Budget planning configuration schema for the scenario looks as follows:</span></span>

![مخطط تكوين تخطيط الموازنة](./media/screenshot1-300x152.png)

<span data-ttu-id="b46e6-127">تستخدم جوليا قالب Excel التالي في إعداد الموازنة:</span><span class="sxs-lookup"><span data-stu-id="b46e6-127">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="b46e6-128">[![قالب Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-128">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="b46e6-129">التمرين 1: التكوين</span><span class="sxs-lookup"><span data-stu-id="b46e6-129">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="b46e6-130">**المهمة 1: إنشاء تدرج هرمي للمؤسسات**</span><span class="sxs-lookup"><span data-stu-id="b46e6-130">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="b46e6-131">نظرًا لأن عملية إعداد الموازنة تحدث في إدارة الشؤون المالية، يلزم ليلى إنشاء تدرجي هرمي للمؤسسات بسيطة جداً - يتكون من القسم المالي.</span><span class="sxs-lookup"><span data-stu-id="b46e6-131">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> <span data-ttu-id="b46e6-132">1.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-132">1.1.</span></span> <span data-ttu-id="b46e6-133">الانتقال إلى التدرجات الهرمية للمؤسسات (إدارة المؤسسة &gt; المؤسسات &gt; التدرجات الهرمية للمؤسسات)، وانقر فوق زر جديد</span><span class="sxs-lookup"><span data-stu-id="b46e6-133">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click New button</span></span>

![التدرج الهرمي للمؤسسة](./media/screenshot3.png) 

<span data-ttu-id="b46e6-135">1.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-135">1.2.</span></span> <span data-ttu-id="b46e6-136">اكتب اسم للتدرج الهرمي للمؤسسات، ثم انقر فوق زر تعيين الغرض</span><span class="sxs-lookup"><span data-stu-id="b46e6-136">Type the name for the organizational hierarchy and click button Assign purpose</span></span>

<span data-ttu-id="b46e6-137">[![الاسم](./media/screenshot4.png)](./media/screenshot4.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-137">[![Name](./media/screenshot4.png)](./media/screenshot4.png)</span></span> 

<span data-ttu-id="b46e6-138">1.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-138">1.3.</span></span> <span data-ttu-id="b46e6-139">حدد غرض تخطيط الموازنة، ثم انقر فوق زر "إضافة" وقم بتعيين التدرج الهرمي للمؤسسات الذي تم إنشاؤه حديثًا:</span><span class="sxs-lookup"><span data-stu-id="b46e6-139">Select Budget planning purpose, click button Add and assign newly created organizational hierarchy:</span></span> 

<span data-ttu-id="b46e6-140">[![تعيين غرض](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-140">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="b46e6-141">1.4.</span><span class="sxs-lookup"><span data-stu-id="b46e6-141">1.4.</span></span> <span data-ttu-id="b46e6-142">كرر الخطوة أعلاه للأغراض التنظيمية الأمنية.</span><span class="sxs-lookup"><span data-stu-id="b46e6-142">Repeat the step above for Security organizational purpose.</span></span> <span data-ttu-id="b46e6-143">وأغلق النموذج عند الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="b46e6-143">Close the form when done.</span></span>

<span data-ttu-id="b46e6-144">[![مؤسسة الأمان](./media/screenshot6.png)](./media/screenshot6.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-144">[![Security org](./media/screenshot6.png)](./media/screenshot6.png)</span></span>

<span data-ttu-id="b46e6-145">1.5.</span><span class="sxs-lookup"><span data-stu-id="b46e6-145">1.5.</span></span> <span data-ttu-id="b46e6-146">في نموذج التدرجات الهرمية للمؤسسات، انقر فوق الزر عرض.</span><span class="sxs-lookup"><span data-stu-id="b46e6-146">In the Organizational Hierarchies form click button View.</span></span> <span data-ttu-id="b46e6-147">انقر فوق "تحرير" في مصمم التدرج الهرمي وأنشئ تدرجًا هرميًا بواسطة النقر فوق الزر إدراج.</span><span class="sxs-lookup"><span data-stu-id="b46e6-147">Click Edit in the Hierarchy designer and create a hierarchy by clicking button Insert.</span></span>

<span data-ttu-id="b46e6-148">[![إدراج](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-148">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="b46e6-149">1.6.</span><span class="sxs-lookup"><span data-stu-id="b46e6-149">1.6.</span></span> <span data-ttu-id="b46e6-150">حدد القسم المالي للتدرج الهرمي لإعداد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-150">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="b46e6-151">[![المالية](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-151">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="b46e6-152">1.7.</span><span class="sxs-lookup"><span data-stu-id="b46e6-152">1.7.</span></span> <span data-ttu-id="b46e6-153">عند الانتهاء، انقر فوق الزر نشر وإغلاق.</span><span class="sxs-lookup"><span data-stu-id="b46e6-153">When done, click button Publish and Close.</span></span> <span data-ttu-id="b46e6-154">حدد 1/1/2015 كتاريخ سريان لنشر التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="b46e6-154">Select 1/1/2015 as effective date for hierarchy publishing.</span></span>

<span data-ttu-id="b46e6-155">[![تاريخ السريان](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-155">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="b46e6-156">المهمة 2: تكوين أمان المستخدم</span><span class="sxs-lookup"><span data-stu-id="b46e6-156">Task 2: Configure user security</span></span>
<span data-ttu-id="b46e6-157">يستخدم تخطيط الموازنة سياسات أمان خاصة لتكوين الوصول إلى بيانات خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-157">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="b46e6-158">وتحتاج ليلى إلى منح حق الوصول إلى خطط الموازنة المالية لنفسها.</span><span class="sxs-lookup"><span data-stu-id="b46e6-158">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="b46e6-159">2.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-159">2.1.</span></span> <span data-ttu-id="b46e6-160">التبديل إلى سياق الكيان القانوني لشركة الرشيدي المحدودة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-160">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="b46e6-161">2.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-161">2.2.</span></span> <span data-ttu-id="b46e6-162">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-162">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="b46e6-163">في علامة تبويب "المعلمات"، قم بتعيين قيمة نموذج الأمان إلى "استنادًا إلى مؤسسات الأمان".</span><span class="sxs-lookup"><span data-stu-id="b46e6-163">In Parameters tab, set the Security model value to Based on security organizations</span></span> 

<span data-ttu-id="b46e6-164">[![المعلمات](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-164">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="b46e6-165">2.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-165">2.3.</span></span> <span data-ttu-id="b46e6-166">انتقل إلى إدارة النظام &gt; المستخدمين &gt; المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="b46e6-166">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="b46e6-167">إعطاء مستخدم مسؤول (ليلى فوزي) دور مدير الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-167">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="b46e6-168">[![مدير الموازنة](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-168">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="b46e6-169">2.4.</span><span class="sxs-lookup"><span data-stu-id="b46e6-169">2.4.</span></span> <span data-ttu-id="b46e6-170">اختر دور المستخدم وانقر فوق "تعيين مؤسسات".</span><span class="sxs-lookup"><span data-stu-id="b46e6-170">Pick user role and click Assign organizations</span></span> 

<span data-ttu-id="b46e6-171">[![تعيين مؤسسات](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-171">[![Assign org](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="b46e6-172">2.5.</span><span class="sxs-lookup"><span data-stu-id="b46e6-172">2.5.</span></span> <span data-ttu-id="b46e6-173">حدد "منح الوصول إلى مؤسسات محددة".</span><span class="sxs-lookup"><span data-stu-id="b46e6-173">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="b46e6-174">اختيار التدرج الهرمي للمؤسسات الذي تم إنشاؤه في الخطوة الأولى.</span><span class="sxs-lookup"><span data-stu-id="b46e6-174">Pick Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="b46e6-175">اختر عقدة المالية وانقر فوق الزر "‏‫منح الوصول مع المؤسسات الفرعية‬".</span><span class="sxs-lookup"><span data-stu-id="b46e6-175">Pick Finance node and click Grant with children button</span></span> 

<span data-ttu-id="b46e6-176">***هام!***</span><span class="sxs-lookup"><span data-stu-id="b46e6-176">***Important!***</span></span> <span data-ttu-id="b46e6-177">*تأكد من أنك موجود في سياق الكيان القانوني لشركة الرشيدي المحدودة عند تنفيذ هذه المهمة، إذ يتم تطبيق الأمان التنظيمي لكل كيان قانوني*</span><span class="sxs-lookup"><span data-stu-id="b46e6-177">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

<span data-ttu-id="b46e6-178">[![منح الوصول](./media/screenshot14.png)](./media/screenshot14.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-178">[![Grant access](./media/screenshot14.png)](./media/screenshot14.png)</span></span>

### <a name="task-3-create-scenarios"></a><span data-ttu-id="b46e6-179">المهمة 3: إنشاء السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="b46e6-179">Task 3: Create scenarios</span></span>
<span data-ttu-id="b46e6-180">3.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-180">3.1.</span></span> <span data-ttu-id="b46e6-181">انتقل إلى إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-181">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="b46e6-182">في صفحة السيناريوهات، لاحظ السيناريوهات التي سنقوم باستخدامها في هذا المعمل: القيم الفعلية والقيم المدرجة في الموازنة للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-182">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="b46e6-183">*ملاحظة: يمكنك إنشاء سيناريوهات جديدة لهذه العملية عند الضرورة واستخدامها بدلاً من ذلك.*</span><span class="sxs-lookup"><span data-stu-id="b46e6-183">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="b46e6-184">[![سيناريوهات جديدة](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-184">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="b46e6-185">*ملاحظة: بما أن ليلى لا تستخدم عملية الموافقة الرسمية لإعداد الموازنة، سوف نتخطى إعداد مهام سير العمل، والمراحل ومراحل سير العمل في هذا المعمل، وسنستخدم الإعداد الموجود لسير عمل الاعتماد التلقائي لسير العمل. انظر الملحق لتكوين سير العمل هذا.*</span><span class="sxs-lookup"><span data-stu-id="b46e6-185">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="b46e6-186">المهمة 4: إنشاء أعمدة خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="b46e6-186">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="b46e6-187">وتكون اعمدة خطة الموازنة إما أعمدة مستندة إلى النقد أو الكمية ويمكن استخدامها في تخطيط مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-187">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="b46e6-188">وفي المثال الخاص بنا، نحتاج إلى إنشاء عمود للقيم الفعلية للسنة السابقة و12 عمودًا لتمثيل كل شهر في السنة المدرجة في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-188">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="b46e6-189">ويمكن إنشاء الأعمدة أما بمجرد النقر فوق الزر "إضافة" وتعبئة القيم، أو بمساعدة من وحدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="b46e6-189">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="b46e6-190">في هذا المعمل، سوف نستخدم وحدة بيانات لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="b46e6-190">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="b46e6-191">4.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-191">4.1.</span></span> <span data-ttu-id="b46e6-192">‏‫في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة الأعمدة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-192">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Columns page.</span></span> <span data-ttu-id="b46e6-193">انقر فوق زر Office في الركن العلوي الأيسر من النموذج واختر الأعمدة (غير المصفاة).</span><span class="sxs-lookup"><span data-stu-id="b46e6-193">Click Office button on the top right corner of the form and pick Columns (unfiltered)</span></span> 

<span data-ttu-id="b46e6-194">[![أعمدة غير مصفاة](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-194">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="b46e6-195">4.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-195">4.2.</span></span> <span data-ttu-id="b46e6-196">سيقوم النظام بفتح مصنف Excel لاستخدامه لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="b46e6-196">System will open Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="b46e6-197">انقر فوق "تمكين التحرير والثقة في هذا التطبيق"، عند ظهور المطالبة</span><span class="sxs-lookup"><span data-stu-id="b46e6-197">If prompted, click Enable Editing and Trust this app</span></span> 

<span data-ttu-id="b46e6-198">[![تمكين ‏‏التحرير](./media/screenshot18.png)](./media/screenshot18.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-198">[![Enable editing](./media/screenshot18.png)](./media/screenshot18.png)</span></span> 

<span data-ttu-id="b46e6-199">[![الثقة في هذا التطبيق](./media/screenshot17.png)](./media/screenshot17.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-199">[![Trust this app](./media/screenshot17.png)](./media/screenshot17.png)</span></span>

<span data-ttu-id="b46e6-200">4.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-200">4.3.</span></span> <span data-ttu-id="b46e6-201">‏‫وسنحتاج إلى مزيد من الأعمدة لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="b46e6-201">We will need more columns to fill the values in.</span></span> <span data-ttu-id="b46e6-202">انقر فوق "تصميم" في الجزء الأيسر لإضافة الأعمدة إلى الشبكة:</span><span class="sxs-lookup"><span data-stu-id="b46e6-202">Click Design on the right side pane to add the columns to the grid:</span></span> 

<span data-ttu-id="b46e6-203">[![تصميم](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-203">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="b46e6-204">4.4.</span><span class="sxs-lookup"><span data-stu-id="b46e6-204">4.4.</span></span> <span data-ttu-id="b46e6-205">‏‫انقر فوق زر القلم الصغير بجوار أعمدة الخطة لمشاهدة الأعمدة المتوفرة لإضافتها إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-205">Click little pencil button next to PlanColumns to see available columns to add to the grid</span></span> 

<span data-ttu-id="b46e6-206">[![تحرير](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-206">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="b46e6-207">4.5.</span><span class="sxs-lookup"><span data-stu-id="b46e6-207">4.5.</span></span> <span data-ttu-id="b46e6-208">‏‫انقر نقرًا مزدوجًا فوق كل حقل متوفر لإضافته إلى الحقول المحددة وانقر فوق "تحديث"</span><span class="sxs-lookup"><span data-stu-id="b46e6-208">Double click on each available field to add them to Selected fields and click Update</span></span> 

![تحديث](./media/screenshot21.png)<span data-ttu-id="b46e6-210">](./media/screenshot21.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-210">](./media/screenshot21.png)</span></span> 

<span data-ttu-id="b46e6-211">4.6.</span><span class="sxs-lookup"><span data-stu-id="b46e6-211">4.6.</span></span> <span data-ttu-id="b46e6-212">في جدول Excel، أضف كافة الأعمدة التي يلزم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b46e6-212">In Excel table add all the columns that need to be created.</span></span> <span data-ttu-id="b46e6-213">استخدم ميزة الملء التلقائي في Excel لإضافة البنود بسرعة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-213">Use AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="b46e6-214">‏‫تأكد من إضافة البنود كجزء من الجدول (عند استخدام التمرير العمودي، يجب أن تتمكن من رؤية رؤوس الأعمدة أعلى الشبكة)</span><span class="sxs-lookup"><span data-stu-id="b46e6-214">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid)</span></span> 

<span data-ttu-id="b46e6-215">[![تعبئة تلقائية](./media/screenshot22.png)](./media/screenshot22.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-215">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span></span> 

<span data-ttu-id="b46e6-216">4.7.</span><span class="sxs-lookup"><span data-stu-id="b46e6-216">4.7.</span></span> <span data-ttu-id="b46e6-217">قم بالرجوع إلى Finance and Operations، ثم قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-217">Return to Finance and Operations and refresh the page.</span></span> <span data-ttu-id="b46e6-218">سوف تظهر القيم المنشورة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b46e6-218">Published values will appear in Finance and Operations.</span></span> 

<span data-ttu-id="b46e6-219">[![تحديث](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-219">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="b46e6-220">المهمة 5: إنشاء قوالب وتخطيطات وثيقة خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="b46e6-220">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="b46e6-221">يحدد المخطط كيف ستبدو شبكة بنود وثيقة خطة الموازنة عندما يقوم المستخدم بفتح مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-221">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="b46e6-222">كما أنه من الممكن تبديل تخطيط مستند خطة الموازنة لعرض نفس البيانات الموجودة في زوايا مختلفة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-222">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="b46e6-223">والآن، عندما حصلت ليلى على الأعمدة المحددة لاستخدامها مع مستند خطة الموازنة، فهي تحتاج إلى إنشاء تخطيط مستند خطة موازنة يبدو مماثلاً لجدول Excel يمكنها استخدامه لإنشاء بيانات الموازنة (راجع قسم نظرة عامة على السيناريو في هذا المعمل)</span><span class="sxs-lookup"><span data-stu-id="b46e6-223">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="b46e6-224">5.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-224">5.1.</span></span> <span data-ttu-id="b46e6-225">في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة التخطيطات.</span><span class="sxs-lookup"><span data-stu-id="b46e6-225">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Layouts page.</span></span> <span data-ttu-id="b46e6-226">قم بإنشاء تخطيط جديد لإدخال الموازنة الشهرية:</span><span class="sxs-lookup"><span data-stu-id="b46e6-226">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="b46e6-227">اختر مجموعة الأبعاد MA+BU لتضمين الحسابات الرئيسية ووحدات الأعمال في التخطيط.</span><span class="sxs-lookup"><span data-stu-id="b46e6-227">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="b46e6-228">اسرد كافة أعمدة خطة الموازنة التي تم إنشاؤها في الخطوة السابقة في قسم العناصر.</span><span class="sxs-lookup"><span data-stu-id="b46e6-228">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="b46e6-229">اجعل كافة القيم الفعلية قابلة للتحرير ما عدا القيم الفعلية للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-229">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="b46e6-230">انقر فوق الزر أوصاف لتحديد الأبعاد المالية التي ينبغي أن تعرض الأوصاف في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-230">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="b46e6-231">[![الأوصاف](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-231">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="b46e6-232">استنادًا إلى تعريف تخطيط خطة الموازنة، يمكننا إنشاء قالب Excel لاستخدامه كطريقة بديلة لتحرير بيانات الموازنة.‬</span><span class="sxs-lookup"><span data-stu-id="b46e6-232">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="b46e6-233">ونظرًا لأنه يجب أن يتطابق قالب Excel مع تعريف تخطيط خطة الموازنة، لن تتمكن من تحرير تخطيط خطة الموازنة بعد إنشاء قالب Excel، وبالتالي يجب تنفيذ هذه المهمة بعد أن يتم تحديد كافة مكونات تخطيط.</span><span class="sxs-lookup"><span data-stu-id="b46e6-233">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="b46e6-234">5.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-234">5.2.</span></span> <span data-ttu-id="b46e6-235">بالنسبة للتخطيط الذي تم إنشاؤه في الخطوة 5.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-235">For the layout created in the 5.1.</span></span> <span data-ttu-id="b46e6-236">انقر فوق الزر قالب &gt; إنشاء.</span><span class="sxs-lookup"><span data-stu-id="b46e6-236">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="b46e6-237">تأكيد رسالة التحذير.</span><span class="sxs-lookup"><span data-stu-id="b46e6-237">Confirm the warning message.</span></span> <span data-ttu-id="b46e6-238">لعرض القالب، انقر فوق قالب &gt; عرض.</span><span class="sxs-lookup"><span data-stu-id="b46e6-238">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="b46e6-239">*ملاحظة: تأكد من اختيار "حفظ باسم" وحدد المكان الذي ينبغي تخزين القالب فيه من أجل تحريره. إذا اختار المستخدم "فتح" في مربع الحوار بدون الحفظ، فلن يتم الاحتفاظ بالتغييرات التي أُجريت على الملف عند إغلاق الملف.* 
[![طريقة عرض القالب](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-239">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="b46e6-240">5.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-240">5.3.</span></span> <span data-ttu-id="b46e6-241">&lt; خطوة اختيارية&gt; اعمل على تعديل قالب Excel لكي يكون مألوفًا أكثر بالنسبة إلى المستخدم – أضف المعادلات الإجمالية وحقول الرأس والتنسيقات وغير ذلك. احفظ التغييرات وقم بتحميل الملف إلى تخطيط خطة الموازنة بالنقر فوق تخطيط &gt; تحميل [![تحميل](./media/screenshot26.png)](./media/screenshot26.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-241">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload [![Upload](./media/screenshot26.png)](./media/screenshot26.png)</span></span>

### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="b46e6-242">المهمة 6: إنشاء عملية تخطيط موازنة</span><span class="sxs-lookup"><span data-stu-id="b46e6-242">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="b46e6-243">تحتاج ليلى إلى إنشاء وتنشيط عملية تخطيط موازنة جديدة تجمع كافة خطوات الإعداد السابقة للبدء في إدخال خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-243">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="b46e6-244">تحدد عملية تخطيط الموازنة مؤسسات إعداد الموازنة، وسير العمل، والتخطيطات، والقوالب التي سيتم استخدامها لإنشاء خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-244">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="b46e6-245">6.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-245">6.1.</span></span> <span data-ttu-id="b46e6-246">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; عملية تخطيط الموازنة وإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="b46e6-246">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process and create a new record.</span></span>

-   <span data-ttu-id="b46e6-247">عملية تخطيط الموازنة - إعداد الموازنة لشركة الرشيدي المحدودة للعام المالي 2016</span><span class="sxs-lookup"><span data-stu-id="b46e6-247">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="b46e6-248">دورة الموازنة - العام المالي 2016</span><span class="sxs-lookup"><span data-stu-id="b46e6-248">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="b46e6-249">دفتر الأستاذ - شركة الرشيدي المحدودة</span><span class="sxs-lookup"><span data-stu-id="b46e6-249">Ledger – DEMF</span></span>
-   <span data-ttu-id="b46e6-250">بنية الحساب الافتراضي - أرباح وخسائر التصنيع</span><span class="sxs-lookup"><span data-stu-id="b46e6-250">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="b46e6-251">التدرج الهرمي للمؤسسات – اختيار التدرج الهرمي الذي تم إنشاؤه في بداية المعمل</span><span class="sxs-lookup"><span data-stu-id="b46e6-251">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="b46e6-252">سير عمل تخطيط الموازنة – تعيين تلقائي – اعتماد سير العمل لإدارة الشؤون المالية</span><span class="sxs-lookup"><span data-stu-id="b46e6-252">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="b46e6-253">في قوالب وقواعد مرحلة تخطيط الموازنة، بالنسبة لكل مرحلة تخطيط موازنة سير عمل، اختر ما إذا كان مسموحًا بإضافة البنود وتعديل البنود والتخطيط الذي يجب استخدامه بشكل افتراضي</span><span class="sxs-lookup"><span data-stu-id="b46e6-253">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="b46e6-254">*ملاحظة: يمكنك إنشاء تخطيطات المستند الإضافية وقم بتعيينها لتكون متوفرة في مرحلة سير عمل تخطيط الموازنة عن طريق النقر فوق الزر تخطيطات بديلة.*</span><span class="sxs-lookup"><span data-stu-id="b46e6-254">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="b46e6-255">[![التخطيطات البديلة](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-255">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="b46e6-256">6.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-256">6.2.</span></span> <span data-ttu-id="b46e6-257">حدد الإجراءات &gt; تنشيط لتنشيط سير عمل تخطيط الموازنة هذا</span><span class="sxs-lookup"><span data-stu-id="b46e6-257">Select Actions &gt; Activate to activate this budget planning workflow</span></span> 

<span data-ttu-id="b46e6-258">[![تنشيط](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-258">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="b46e6-259">تمرين 2: محاكاة العملية</span><span class="sxs-lookup"><span data-stu-id="b46e6-259">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="b46e6-260">المهمة 7: إنشاء البيانات الأولية لخطة الموازنة من دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="b46e6-260">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="b46e6-261">7.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-261">7.1.</span></span> <span data-ttu-id="b46e6-262">انتقل إلى إعداد الموازنة &gt; دوري &gt; إنشاء خطة الموازنة من دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="b46e6-262">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="b46e6-263">قم بتعبئة معلمات العملية الدورية وانقر فوق الزر إنشاء.</span><span class="sxs-lookup"><span data-stu-id="b46e6-263">Fill in the periodic process parameters and click button Generate.</span></span> 

<span data-ttu-id="b46e6-264">[![إنشاء](./media/screenshot29.png)](./media/screenshot29.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-264">[![Generate](./media/screenshot29.png)](./media/screenshot29.png)</span></span> 

<span data-ttu-id="b46e6-265">7.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-265">7.2.</span></span> <span data-ttu-id="b46e6-266">انتقل إلى إعداد الموازنة &gt; خطط الموازنة للبحث عن خطة موازنة تم إنشاؤها بواسطة عملية الإنشاء.</span><span class="sxs-lookup"><span data-stu-id="b46e6-266">Navigate to Budgeting &gt; Budget plans to find a budget plan created by Generate process.</span></span> 

<span data-ttu-id="b46e6-267">[![خطة الموازنة](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-267">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="b46e6-268">7.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-268">7.3.</span></span> <span data-ttu-id="b46e6-269">افتح تفاصيل المستند بالنقر فوق الارتباط التشعبي رقم المستند.</span><span class="sxs-lookup"><span data-stu-id="b46e6-269">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="b46e6-270">يتم عرض خطة الموازنة كما هو محدد في التخطيط الذي تم إنشاؤه أثناء الوجود في هذا المعمل</span><span class="sxs-lookup"><span data-stu-id="b46e6-270">Budget plan is displayed as defined in the layout created during this lab</span></span> 

<span data-ttu-id="b46e6-271">[![عرض خطة الموازنة](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-271">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="b46e6-272">المهمة 8: إنشاء موازنة السنة الحالية استناداً إلى القيم الافتراضية للسنة السابقة</span><span class="sxs-lookup"><span data-stu-id="b46e6-272">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="b46e6-273">يمكن استخدام طرق التوزيع في خطة الموازنة نسخ المعلومات الخاصة بخطط الموازنة بسهولة من سيناريو واحد إلى آخر / نشرها عبر فترات/توزيعها على أبعاد.</span><span class="sxs-lookup"><span data-stu-id="b46e6-273">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="b46e6-274">سوف نستخدم التوزيعات لإنشاء موازنة السنة الحالية من القيم الفعلية للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-274">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="b46e6-275">8.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-275">8.1.</span></span> <span data-ttu-id="b46e6-276">اختر كافة البنود في شبكة مستند خطة الموازنة، وانقر فوق الزر "توزيع الموازنة"</span><span class="sxs-lookup"><span data-stu-id="b46e6-276">Pick all lines in the budget plan document grid and click button allocate budget</span></span> 

<span data-ttu-id="b46e6-277">[![كافة البنود](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-277">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="b46e6-278">8.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-278">8.2.</span></span> <span data-ttu-id="b46e6-279">حدد طريقة التخصيص، والمفتاح الدوري، والمصدر وسيناريوهات الوجهة، ثم انقر فوق تخصيص</span><span class="sxs-lookup"><span data-stu-id="b46e6-279">Select allocation method, Period key, Source and destination scenarios and click Allocate</span></span> 

<span data-ttu-id="b46e6-280">[![توزيع](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-280">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="b46e6-281">سوف يتم نسخ المبالغ الفعلية للعام الماضي إلى موازنة السنة الحالية، وتخصصيها عبر الفترات باستخدام مفتاح فترة منحنى المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b46e6-281">The previous year actual amounts will be copied to current year budget and allocate them across periods using Sales curve period key.</span></span> 

<span data-ttu-id="b46e6-282">[![منحنى المبيعات](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-282">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="b46e6-283">المهمة 9: ضبط مستند خطة الموازنة باستخدام Excel ووضع الصيغة النهائية للمستند</span><span class="sxs-lookup"><span data-stu-id="b46e6-283">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="b46e6-284">9.1.</span><span class="sxs-lookup"><span data-stu-id="b46e6-284">9.1.</span></span> <span data-ttu-id="b46e6-285">انقر فوق الزر ورقة عمل لفتح محتويات المستند في Excel.</span><span class="sxs-lookup"><span data-stu-id="b46e6-285">Click Button worksheet to open document contents in Excel</span></span>

<span data-ttu-id="b46e6-286">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-286">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span></span>

<span data-ttu-id="b46e6-287">9.2.</span><span class="sxs-lookup"><span data-stu-id="b46e6-287">9.2.</span></span> <span data-ttu-id="b46e6-288">عند فتح مصنف Excel، اضبط الأرقام في مستند خطة الموازنة، وانقر فوق الزر نشر.</span><span class="sxs-lookup"><span data-stu-id="b46e6-288">When Excel workbook opens, adjust the numbers in budget plan document and click button Publish.</span></span>

<span data-ttu-id="b46e6-289">[![نشر](./media/screenshot36.png)](./media/screenshot36.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-289">[![Publish](./media/screenshot36.png)](./media/screenshot36.png)</span></span>

<span data-ttu-id="b46e6-290">9.3.</span><span class="sxs-lookup"><span data-stu-id="b46e6-290">9.3.</span></span> <span data-ttu-id="b46e6-291">ارجع إلى مستند خطة الموازنة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b46e6-291">Return to budget plan document in Finance and Operations.</span></span> <span data-ttu-id="b46e6-292">انقر فوق سير العمل &gt; إرسال وذلك لاعتماد المستند تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="b46e6-292">Click Workflow &gt; Submit to Auto-approve the document</span></span>

<span data-ttu-id="b46e6-293">[![الاعتماد التلقائي](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-293">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="b46e6-294">بمجرد اكتمال سير العمل، يتم تغيير مرحلة مستند خطة الموازنة إلى "معتمد".</span><span class="sxs-lookup"><span data-stu-id="b46e6-294">Once workflow completes, budget plan document stage changes to Approved.</span></span> <span data-ttu-id="b46e6-295">[![معتمد](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-295">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="b46e6-296">الملحق</span><span class="sxs-lookup"><span data-stu-id="b46e6-296">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="b46e6-297">الاعتماد التلقائي لتكوين سير العمل</span><span class="sxs-lookup"><span data-stu-id="b46e6-297">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="b46e6-298">أ.</span><span class="sxs-lookup"><span data-stu-id="b46e6-298">A.</span></span> <span data-ttu-id="b46e6-299">إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; ‏‫عمليات سير عمل إعداد الموازنة‬ قم بإنشاء سير عمل جديد باستخدام قالب عمليات سير العمل لتخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-299">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="b46e6-300">[![إنشاء سير عمل جديد](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-300">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="b46e6-301">سوف يحتوي سير العمل هذا على مهمة واحدة فقط- مرحلة الانتقال لخطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="b46e6-301">This workflow will contain only one task – Stage transition budget plan</span></span> 

<span data-ttu-id="b46e6-302">[![مرحلة انتقال خطة الموازنة](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-302">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="b46e6-303">احفظ سير العمل ونشّطه.</span><span class="sxs-lookup"><span data-stu-id="b46e6-303">Save and activate the workflow.</span></span> 

<span data-ttu-id="b46e6-304">ب.</span><span class="sxs-lookup"><span data-stu-id="b46e6-304">B.</span></span> <span data-ttu-id="b46e6-305">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-305">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="b46e6-306">في علامة التبويب "المراحل" قم بإنشاء مرحلتين- الأولية والمرسلة</span><span class="sxs-lookup"><span data-stu-id="b46e6-306">In Stages tab create 2 stages – Initial and Submitted</span></span> 

<span data-ttu-id="b46e6-307">[![الأولى والمرسلة](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-307">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="b46e6-308">ج.</span><span class="sxs-lookup"><span data-stu-id="b46e6-308">C.</span></span> <span data-ttu-id="b46e6-309">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="b46e6-309">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="b46e6-310">في علامة التبويب "مراحل سير العمل"، قم بإقران الاعتماد التلقائي لسير العمل الذي تم إنشاؤه في خطوة أ مع المرحلتين الأولية والمرسلة</span><span class="sxs-lookup"><span data-stu-id="b46e6-310">In Workflow Stages tab Associate the workflow Auto – approve created in A step with the stages Initial and Submitted</span></span> 

<span data-ttu-id="b46e6-311">[![إعداد الموازنة‬ وتخطيط الموازنة‬](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="b46e6-311">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  




