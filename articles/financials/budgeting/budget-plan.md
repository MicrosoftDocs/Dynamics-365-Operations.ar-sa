---
title: "تخطيط الموازنة"
description: "يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations في مجال تخطيط الموازنة. الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين."
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b8f2f3a33dc19c2ebc941d1a504eae0c276f3cdf
ms.openlocfilehash: ac2e98dbbd45becf06e28b6ea4eb9d0ec15e30f6
ms.contentlocale: ar-sa
ms.lasthandoff: 06/25/2018

---

# <a name="budget-planning"></a><span data-ttu-id="17a1b-104">تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-104">Budget planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17a1b-105">يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations في مجال تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-105">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 for Finance and Operations functionality updates in Budget planning area.</span></span> <span data-ttu-id="17a1b-106">الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="17a1b-106">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="17a1b-107">سيركز هذا المعمل تحديداً على المهام أو العمليات التجارية التالية:</span><span class="sxs-lookup"><span data-stu-id="17a1b-107">This lab will focus specifically on the following business processes or tasks:</span></span>
- <span data-ttu-id="17a1b-108">إنشاء تدرج هرمي تنظيمي لتخطيط الموازنة وتكوين أمان المستخدم</span><span class="sxs-lookup"><span data-stu-id="17a1b-108">Creating organizational hierarchy for budget planning and configuring user security</span></span>
- <span data-ttu-id="17a1b-109">تحديد سيناريوهات خطة الموازنة وأعمدة خطة الموازنة والتخطيطات وقوالب Excel</span><span class="sxs-lookup"><span data-stu-id="17a1b-109">Defining budget plan scenarios, budget plan columns, layouts and Excel templates</span></span>
- <span data-ttu-id="17a1b-110">إنشاء عملية تخطيط الموازنة وتنشيطها</span><span class="sxs-lookup"><span data-stu-id="17a1b-110">Creating and activating budget planning process</span></span>
- <span data-ttu-id="17a1b-111">إنشاء مستند خطة الموازنة عن طريق سحب القيم الفعلية من دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="17a1b-111">Creating budget plan document by pulling in actuals from General ledger</span></span>
- <span data-ttu-id="17a1b-112">استخدام التوزيعات لتعديل بيانات مستند خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-112">Using allocations to adjust budget plan document data</span></span>
- <span data-ttu-id="17a1b-113">تحرير بيانات مستند خطة الموازنة في Excel</span><span class="sxs-lookup"><span data-stu-id="17a1b-113">Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="17a1b-114">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="17a1b-114">Prerequisites</span></span> 
------------------

<span data-ttu-id="17a1b-115">بالنسبة إلى البرنامج التعليمي، سوف تحتاج إلى الوصول إلى بيئة Finance and Operations مع بيانات تجريبية لشركة التعمير، ويتم توفيرها كمسؤول في المثيل.</span><span class="sxs-lookup"><span data-stu-id="17a1b-115">For this tutorial, you’ll need to access the Finance and Operations environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="17a1b-116">فلا تستخدم المستعرض الخاص لهذا المعمل - قم بتسجيل الخروج من أي حساب آخر في المستعرض إذا لزم الأمر وتسجيل الدخول باستخدام بيانات اعتماد مسؤول Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17a1b-116">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with Finance and Operations administrator credentials.</span></span> <span data-ttu-id="17a1b-117">عند تسجيل الدخول إلى Finance and Operations، **يجب** عليك تحديد خانة اختيار "الاستمرار في تسجيل الدخول".</span><span class="sxs-lookup"><span data-stu-id="17a1b-117">When signing into Finance and Operations, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="17a1b-118">ويؤدي هذا إلى إنشاء ملف تعريف ارتباط دائم يحتاج تطبيق Excel إليه حاليًا.</span><span class="sxs-lookup"><span data-stu-id="17a1b-118">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="17a1b-119">وفي حالة تسجيل الدخول إلى Finance and Operations باستخدام مستعرض غير IE، فستتم مطالبتك بتسجيل الدخول في تطبيق Excel.</span><span class="sxs-lookup"><span data-stu-id="17a1b-119">If you sign in to the Finance and Operations using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="17a1b-120">وعند النقر فوق "تسجيل الدخول" في تطبيق Excel، سيتم فتح نافذة IE المنبثقة وعند تسجيل الدخول، **يجب** عليك تحديد خانة الاختيار "الاستمرار في تسجيل الدخول".</span><span class="sxs-lookup"><span data-stu-id="17a1b-120">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="17a1b-121">إذا كان النقر فوق "تسجيل الدخول" في تطبيق Excel لا يبدو أنه يفعل أي شيء، فيجب مسح ذاكرة التخزين المؤقت لملف تعريف ارتباط مستعرض IE.</span><span class="sxs-lookup"><span data-stu-id="17a1b-121">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="17a1b-122">**نظرة عامة على السيناريو**</span><span class="sxs-lookup"><span data-stu-id="17a1b-122">**Scenario overview**</span></span>
<span data-ttu-id="17a1b-123">تعمل ليلى كمدير مالي في شركة الرشيدي المحدودة في القاهرة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-123">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="17a1b-124">ومع اقتراب العام المالي 2016، تحتاج إلى العمل في إعداد موازنة الشركة للسنة المقبلة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-124">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="17a1b-125">يبدو إعداد الموازنة على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="17a1b-125">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="17a1b-126">تستخدم ليلى المبالغ الفعلية للسنة السابقة كنقطة بداية لإنشاء الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-126">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="17a1b-127">واستناداً إلى المبالغ الفعلية في العام السابق، تقوم بإنشاء تقديرات لمدة 12 شهرًا في السنة المقبلة</span><span class="sxs-lookup"><span data-stu-id="17a1b-127">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="17a1b-128">وتراجع ليلى الموازنة مع المدير المالي.</span><span class="sxs-lookup"><span data-stu-id="17a1b-128">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="17a1b-129">وبمجرد أن تتنهي من المراجعة، تقوم بإجراء التعديلات اللازمة لخطة الموازنة وتتولى الصياغة النهائية لإعداد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-129">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="17a1b-130">يبدو مخطط تكوين التخطيط للموازنة لهذا السيناريو على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="17a1b-130">Budget planning configuration schema for the scenario looks as follows:</span></span>

![مخطط تكوين تخطيط الموازنة](./media/screenshot1-300x152.png)

<span data-ttu-id="17a1b-132">تستخدم جوليا قالب Excel التالي في إعداد الموازنة:</span><span class="sxs-lookup"><span data-stu-id="17a1b-132">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="17a1b-133">[![قالب Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-133">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="17a1b-134">التمرين 1: التكوين</span><span class="sxs-lookup"><span data-stu-id="17a1b-134">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="17a1b-135">**المهمة 1: إنشاء تدرج هرمي للمؤسسات**</span><span class="sxs-lookup"><span data-stu-id="17a1b-135">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="17a1b-136">نظرًا لأن عملية إعداد الموازنة تحدث في إدارة الشؤون المالية، يلزم ليلى إنشاء تدرجي هرمي للمؤسسات بسيطة جداً - يتكون من القسم المالي.</span><span class="sxs-lookup"><span data-stu-id="17a1b-136">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> <span data-ttu-id="17a1b-137">1.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-137">1.1.</span></span> <span data-ttu-id="17a1b-138">الانتقال إلى التدرجات الهرمية للمؤسسات (إدارة المؤسسة &gt; المؤسسات &gt; التدرجات الهرمية للمؤسسات)، وانقر فوق زر جديد</span><span class="sxs-lookup"><span data-stu-id="17a1b-138">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click New button</span></span>

![التدرج الهرمي للمؤسسة](./media/screenshot3.png) 

<span data-ttu-id="17a1b-140">1.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-140">1.2.</span></span> <span data-ttu-id="17a1b-141">اكتب اسم للتدرج الهرمي للمؤسسات، ثم انقر فوق زر تعيين الغرض</span><span class="sxs-lookup"><span data-stu-id="17a1b-141">Type the name for the organizational hierarchy and click button Assign purpose</span></span>

<span data-ttu-id="17a1b-142">[![الاسم](./media/screenshot4.png)](./media/screenshot4.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-142">[![Name](./media/screenshot4.png)](./media/screenshot4.png)</span></span> 

<span data-ttu-id="17a1b-143">1.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-143">1.3.</span></span> <span data-ttu-id="17a1b-144">حدد غرض تخطيط الموازنة، ثم انقر فوق زر "إضافة" وقم بتعيين التدرج الهرمي للمؤسسات الذي تم إنشاؤه حديثًا:</span><span class="sxs-lookup"><span data-stu-id="17a1b-144">Select Budget planning purpose, click button Add and assign newly created organizational hierarchy:</span></span> 

<span data-ttu-id="17a1b-145">[![تعيين غرض](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-145">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="17a1b-146">1.4.</span><span class="sxs-lookup"><span data-stu-id="17a1b-146">1.4.</span></span> <span data-ttu-id="17a1b-147">كرر الخطوة أعلاه للأغراض التنظيمية الأمنية.</span><span class="sxs-lookup"><span data-stu-id="17a1b-147">Repeat the step above for Security organizational purpose.</span></span> <span data-ttu-id="17a1b-148">وأغلق النموذج عند الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="17a1b-148">Close the form when done.</span></span>

<span data-ttu-id="17a1b-149">[![مؤسسة الأمان](./media/screenshot6.png)](./media/screenshot6.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-149">[![Security org](./media/screenshot6.png)](./media/screenshot6.png)</span></span>

<span data-ttu-id="17a1b-150">1.5.</span><span class="sxs-lookup"><span data-stu-id="17a1b-150">1.5.</span></span> <span data-ttu-id="17a1b-151">في نموذج التدرجات الهرمية للمؤسسات، انقر فوق الزر عرض.</span><span class="sxs-lookup"><span data-stu-id="17a1b-151">In the Organizational Hierarchies form click button View.</span></span> <span data-ttu-id="17a1b-152">انقر فوق "تحرير" في مصمم التدرج الهرمي وأنشئ تدرجًا هرميًا بواسطة النقر فوق الزر إدراج.</span><span class="sxs-lookup"><span data-stu-id="17a1b-152">Click Edit in the Hierarchy designer and create a hierarchy by clicking button Insert.</span></span>

<span data-ttu-id="17a1b-153">[![إدراج](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-153">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="17a1b-154">1.6.</span><span class="sxs-lookup"><span data-stu-id="17a1b-154">1.6.</span></span> <span data-ttu-id="17a1b-155">حدد القسم المالي للتدرج الهرمي لإعداد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-155">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="17a1b-156">[![المالية](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-156">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="17a1b-157">1.7.</span><span class="sxs-lookup"><span data-stu-id="17a1b-157">1.7.</span></span> <span data-ttu-id="17a1b-158">عند الانتهاء، انقر فوق الزر نشر وإغلاق.</span><span class="sxs-lookup"><span data-stu-id="17a1b-158">When done, click button Publish and Close.</span></span> <span data-ttu-id="17a1b-159">حدد 1/1/2015 كتاريخ سريان لنشر التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="17a1b-159">Select 1/1/2015 as effective date for hierarchy publishing.</span></span>

<span data-ttu-id="17a1b-160">[![تاريخ السريان](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-160">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="17a1b-161">المهمة 2: تكوين أمان المستخدم</span><span class="sxs-lookup"><span data-stu-id="17a1b-161">Task 2: Configure user security</span></span>
<span data-ttu-id="17a1b-162">يستخدم تخطيط الموازنة سياسات أمان خاصة لتكوين الوصول إلى بيانات خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-162">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="17a1b-163">وتحتاج ليلى إلى منح حق الوصول إلى خطط الموازنة المالية لنفسها.</span><span class="sxs-lookup"><span data-stu-id="17a1b-163">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="17a1b-164">2.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-164">2.1.</span></span> <span data-ttu-id="17a1b-165">التبديل إلى سياق الكيان القانوني لشركة الرشيدي المحدودة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-165">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="17a1b-166">2.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-166">2.2.</span></span> <span data-ttu-id="17a1b-167">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-167">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="17a1b-168">في علامة تبويب "المعلمات"، قم بتعيين قيمة نموذج الأمان إلى "استنادًا إلى مؤسسات الأمان".</span><span class="sxs-lookup"><span data-stu-id="17a1b-168">In Parameters tab, set the Security model value to Based on security organizations</span></span> 

<span data-ttu-id="17a1b-169">[![المعلمات](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-169">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="17a1b-170">2.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-170">2.3.</span></span> <span data-ttu-id="17a1b-171">انتقل إلى إدارة النظام &gt; المستخدمين &gt; المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="17a1b-171">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="17a1b-172">إعطاء مستخدم مسؤول (ليلى فوزي) دور مدير الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-172">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="17a1b-173">[![مدير الموازنة](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-173">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="17a1b-174">2.4.</span><span class="sxs-lookup"><span data-stu-id="17a1b-174">2.4.</span></span> <span data-ttu-id="17a1b-175">اختر دور المستخدم وانقر فوق "تعيين مؤسسات".</span><span class="sxs-lookup"><span data-stu-id="17a1b-175">Pick user role and click Assign organizations</span></span> 

<span data-ttu-id="17a1b-176">[![تعيين مؤسسات](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-176">[![Assign org](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="17a1b-177">2.5.</span><span class="sxs-lookup"><span data-stu-id="17a1b-177">2.5.</span></span> <span data-ttu-id="17a1b-178">حدد "منح الوصول إلى مؤسسات محددة".</span><span class="sxs-lookup"><span data-stu-id="17a1b-178">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="17a1b-179">اختيار التدرج الهرمي للمؤسسات الذي تم إنشاؤه في الخطوة الأولى.</span><span class="sxs-lookup"><span data-stu-id="17a1b-179">Pick Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="17a1b-180">اختر عقدة المالية وانقر فوق الزر "‏‫منح الوصول مع المؤسسات الفرعية‬".</span><span class="sxs-lookup"><span data-stu-id="17a1b-180">Pick Finance node and click Grant with children button</span></span> 

<span data-ttu-id="17a1b-181">***هام!***</span><span class="sxs-lookup"><span data-stu-id="17a1b-181">***Important!***</span></span> <span data-ttu-id="17a1b-182">*تأكد من أنك موجود في سياق الكيان القانوني لشركة الرشيدي المحدودة عند تنفيذ هذه المهمة، إذ يتم تطبيق الأمان التنظيمي لكل كيان قانوني*</span><span class="sxs-lookup"><span data-stu-id="17a1b-182">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

### <a name="task-3-create-scenarios"></a><span data-ttu-id="17a1b-183">المهمة 3: إنشاء السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="17a1b-183">Task 3: Create scenarios</span></span>
<span data-ttu-id="17a1b-184">3.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-184">3.1.</span></span> <span data-ttu-id="17a1b-185">انتقل إلى إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-185">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="17a1b-186">في صفحة السيناريوهات، لاحظ السيناريوهات التي سنقوم باستخدامها في هذا المعمل: القيم الفعلية والقيم المدرجة في الموازنة للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-186">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="17a1b-187">*ملاحظة: يمكنك إنشاء سيناريوهات جديدة لهذه العملية عند الضرورة واستخدامها بدلاً من ذلك.*</span><span class="sxs-lookup"><span data-stu-id="17a1b-187">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="17a1b-188">[![سيناريوهات جديدة](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-188">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="17a1b-189">*ملاحظة: بما أن ليلى لا تستخدم عملية الموافقة الرسمية لإعداد الموازنة، سوف نتخطى إعداد مهام سير العمل، والمراحل ومراحل سير العمل في هذا المعمل، وسنستخدم الإعداد الموجود لسير عمل الاعتماد التلقائي لسير العمل. انظر الملحق لتكوين سير العمل هذا.*</span><span class="sxs-lookup"><span data-stu-id="17a1b-189">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="17a1b-190">المهمة 4: إنشاء أعمدة خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-190">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="17a1b-191">وتكون اعمدة خطة الموازنة إما أعمدة مستندة إلى النقد أو الكمية ويمكن استخدامها في تخطيط مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-191">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="17a1b-192">وفي المثال الخاص بنا، نحتاج إلى إنشاء عمود للقيم الفعلية للسنة السابقة و12 عمودًا لتمثيل كل شهر في السنة المدرجة في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-192">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="17a1b-193">ويمكن إنشاء الأعمدة أما بمجرد النقر فوق الزر "إضافة" وتعبئة القيم، أو بمساعدة من وحدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="17a1b-193">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="17a1b-194">في هذا المعمل، سوف نستخدم وحدة بيانات لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="17a1b-194">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="17a1b-195">4.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-195">4.1.</span></span> <span data-ttu-id="17a1b-196">‏‫في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة الأعمدة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-196">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Columns page.</span></span> <span data-ttu-id="17a1b-197">انقر فوق زر Office في الركن العلوي الأيسر من النموذج واختر الأعمدة (غير المصفاة).</span><span class="sxs-lookup"><span data-stu-id="17a1b-197">Click Office button on the top right corner of the form and pick Columns (unfiltered)</span></span> 

<span data-ttu-id="17a1b-198">[![أعمدة غير مصفاة](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-198">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="17a1b-199">4.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-199">4.2.</span></span> <span data-ttu-id="17a1b-200">سيقوم النظام بفتح مصنف Excel لاستخدامه لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="17a1b-200">System will open Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="17a1b-201">انقر فوق "تمكين التحرير والثقة في هذا التطبيق"، عند ظهور المطالبة</span><span class="sxs-lookup"><span data-stu-id="17a1b-201">If prompted, click Enable Editing and Trust this app</span></span> 

<span data-ttu-id="17a1b-202">[![تمكين ‏‏التحرير](./media/screenshot18.png)](./media/screenshot18.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-202">[![Enable editing](./media/screenshot18.png)](./media/screenshot18.png)</span></span> 

<span data-ttu-id="17a1b-203">[![الثقة في هذا التطبيق](./media/screenshot17.png)](./media/screenshot17.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-203">[![Trust this app](./media/screenshot17.png)](./media/screenshot17.png)</span></span>

<span data-ttu-id="17a1b-204">4.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-204">4.3.</span></span> <span data-ttu-id="17a1b-205">‏‫وسنحتاج إلى مزيد من الأعمدة لتعبئة القيم.</span><span class="sxs-lookup"><span data-stu-id="17a1b-205">We will need more columns to fill the values in.</span></span> <span data-ttu-id="17a1b-206">انقر فوق "تصميم" في الجزء الأيسر لإضافة الأعمدة إلى الشبكة:</span><span class="sxs-lookup"><span data-stu-id="17a1b-206">Click Design on the right side pane to add the columns to the grid:</span></span> 

<span data-ttu-id="17a1b-207">[![تصميم](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-207">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="17a1b-208">4.4.</span><span class="sxs-lookup"><span data-stu-id="17a1b-208">4.4.</span></span> <span data-ttu-id="17a1b-209">‏‫انقر فوق زر القلم الصغير بجوار أعمدة الخطة لمشاهدة الأعمدة المتوفرة لإضافتها إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-209">Click little pencil button next to PlanColumns to see available columns to add to the grid</span></span> 

<span data-ttu-id="17a1b-210">[![تحرير](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-210">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="17a1b-211">4.5.</span><span class="sxs-lookup"><span data-stu-id="17a1b-211">4.5.</span></span> <span data-ttu-id="17a1b-212">‏‫انقر نقرًا مزدوجًا فوق كل حقل متوفر لإضافته إلى الحقول المحددة وانقر فوق "تحديث"</span><span class="sxs-lookup"><span data-stu-id="17a1b-212">Double click on each available field to add them to Selected fields and click Update</span></span> 

![تحديث](./media/screenshot21.png)<span data-ttu-id="17a1b-214">](./media/screenshot21.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-214">](./media/screenshot21.png)</span></span> 

<span data-ttu-id="17a1b-215">4.6.</span><span class="sxs-lookup"><span data-stu-id="17a1b-215">4.6.</span></span> <span data-ttu-id="17a1b-216">في جدول Excel، أضف كافة الأعمدة التي يلزم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="17a1b-216">In Excel table add all the columns that need to be created.</span></span> <span data-ttu-id="17a1b-217">استخدم ميزة الملء التلقائي في Excel لإضافة البنود بسرعة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-217">Use AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="17a1b-218">‏‫تأكد من إضافة البنود كجزء من الجدول (عند استخدام التمرير العمودي، يجب أن تتمكن من رؤية رؤوس الأعمدة أعلى الشبكة)</span><span class="sxs-lookup"><span data-stu-id="17a1b-218">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid)</span></span> 

<span data-ttu-id="17a1b-219">[![تعبئة تلقائية](./media/screenshot22.png)](./media/screenshot22.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-219">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span></span> 

<span data-ttu-id="17a1b-220">4.7.</span><span class="sxs-lookup"><span data-stu-id="17a1b-220">4.7.</span></span> <span data-ttu-id="17a1b-221">قم بالرجوع إلى Finance and Operations، ثم قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-221">Return to Finance and Operations and refresh the page.</span></span> <span data-ttu-id="17a1b-222">سوف تظهر القيم المنشورة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17a1b-222">Published values will appear in Finance and Operations.</span></span> 

<span data-ttu-id="17a1b-223">[![تحديث](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-223">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="17a1b-224">المهمة 5: إنشاء قوالب وتخطيطات وثيقة خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-224">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="17a1b-225">يحدد المخطط كيف ستبدو شبكة بنود وثيقة خطة الموازنة عندما يقوم المستخدم بفتح مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-225">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="17a1b-226">كما أنه من الممكن تبديل تخطيط مستند خطة الموازنة لعرض نفس البيانات الموجودة في زوايا مختلفة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-226">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="17a1b-227">والآن، عندما حصلت ليلى على الأعمدة المحددة لاستخدامها مع مستند خطة الموازنة، فهي تحتاج إلى إنشاء تخطيط مستند خطة موازنة يبدو مماثلاً لجدول Excel يمكنها استخدامه لإنشاء بيانات الموازنة (راجع قسم نظرة عامة على السيناريو في هذا المعمل)</span><span class="sxs-lookup"><span data-stu-id="17a1b-227">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="17a1b-228">5.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-228">5.1.</span></span> <span data-ttu-id="17a1b-229">في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة التخطيطات.</span><span class="sxs-lookup"><span data-stu-id="17a1b-229">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Layouts page.</span></span> <span data-ttu-id="17a1b-230">قم بإنشاء تخطيط جديد لإدخال الموازنة الشهرية:</span><span class="sxs-lookup"><span data-stu-id="17a1b-230">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="17a1b-231">اختر مجموعة الأبعاد MA+BU لتضمين الحسابات الرئيسية ووحدات الأعمال في التخطيط.</span><span class="sxs-lookup"><span data-stu-id="17a1b-231">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="17a1b-232">اسرد كافة أعمدة خطة الموازنة التي تم إنشاؤها في الخطوة السابقة في قسم العناصر.</span><span class="sxs-lookup"><span data-stu-id="17a1b-232">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="17a1b-233">اجعل كافة القيم الفعلية قابلة للتحرير ما عدا القيم الفعلية للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-233">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="17a1b-234">انقر فوق الزر أوصاف لتحديد الأبعاد المالية التي ينبغي أن تعرض الأوصاف في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-234">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="17a1b-235">[![الأوصاف](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-235">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="17a1b-236">استنادًا إلى تعريف تخطيط خطة الموازنة، يمكننا إنشاء قالب Excel لاستخدامه كطريقة بديلة لتحرير بيانات الموازنة.‬</span><span class="sxs-lookup"><span data-stu-id="17a1b-236">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="17a1b-237">ونظرًا لأنه يجب أن يتطابق قالب Excel مع تعريف تخطيط خطة الموازنة، لن تتمكن من تحرير تخطيط خطة الموازنة بعد إنشاء قالب Excel، وبالتالي يجب تنفيذ هذه المهمة بعد أن يتم تحديد كافة مكونات تخطيط.</span><span class="sxs-lookup"><span data-stu-id="17a1b-237">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="17a1b-238">5.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-238">5.2.</span></span> <span data-ttu-id="17a1b-239">بالنسبة للتخطيط الذي تم إنشاؤه في الخطوة 5.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-239">For the layout created in the 5.1.</span></span> <span data-ttu-id="17a1b-240">انقر فوق الزر قالب &gt; إنشاء.</span><span class="sxs-lookup"><span data-stu-id="17a1b-240">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="17a1b-241">تأكيد رسالة التحذير.</span><span class="sxs-lookup"><span data-stu-id="17a1b-241">Confirm the warning message.</span></span> <span data-ttu-id="17a1b-242">لعرض القالب، انقر فوق قالب &gt; عرض.</span><span class="sxs-lookup"><span data-stu-id="17a1b-242">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="17a1b-243">*ملاحظة: تأكد من اختيار "حفظ باسم" وحدد المكان الذي ينبغي تخزين القالب فيه من أجل تحريره. إذا اختار المستخدم "فتح" في مربع الحوار بدون الحفظ، فلن يتم الاحتفاظ بالتغييرات التي أُجريت على الملف عند إغلاق الملف.* 
[![طريقة عرض القالب](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-243">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="17a1b-244">5.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-244">5.3.</span></span> <span data-ttu-id="17a1b-245">&lt; خطوة اختيارية&gt; اعمل على تعديل قالب Excel لكي يكون مألوفًا أكثر بالنسبة إلى المستخدم – أضف المعادلات الإجمالية وحقول الرأس والتنسيقات وغير ذلك. احفظ التغييرات وقم بتحميل الملف إلى تخطيط خطة الموازنة بالنقر فوق تخطيط &gt; تحميل [![تحميل](./media/screenshot26.png)](./media/screenshot26.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-245">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload [![Upload](./media/screenshot26.png)](./media/screenshot26.png)</span></span>

### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="17a1b-246">المهمة 6: إنشاء عملية تخطيط موازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-246">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="17a1b-247">تحتاج ليلى إلى إنشاء وتنشيط عملية تخطيط موازنة جديدة تجمع كافة خطوات الإعداد السابقة للبدء في إدخال خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-247">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="17a1b-248">تحدد عملية تخطيط الموازنة مؤسسات إعداد الموازنة، وسير العمل، والتخطيطات، والقوالب التي سيتم استخدامها لإنشاء خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-248">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="17a1b-249">6.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-249">6.1.</span></span> <span data-ttu-id="17a1b-250">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; عملية تخطيط الموازنة وإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="17a1b-250">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process and create a new record.</span></span>

-   <span data-ttu-id="17a1b-251">عملية تخطيط الموازنة - إعداد الموازنة لشركة الرشيدي المحدودة للعام المالي 2016</span><span class="sxs-lookup"><span data-stu-id="17a1b-251">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="17a1b-252">دورة الموازنة - العام المالي 2016</span><span class="sxs-lookup"><span data-stu-id="17a1b-252">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="17a1b-253">دفتر الأستاذ - شركة الرشيدي المحدودة</span><span class="sxs-lookup"><span data-stu-id="17a1b-253">Ledger – DEMF</span></span>
-   <span data-ttu-id="17a1b-254">بنية الحساب الافتراضي - أرباح وخسائر التصنيع</span><span class="sxs-lookup"><span data-stu-id="17a1b-254">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="17a1b-255">التدرج الهرمي للمؤسسات – اختيار التدرج الهرمي الذي تم إنشاؤه في بداية المعمل</span><span class="sxs-lookup"><span data-stu-id="17a1b-255">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="17a1b-256">سير عمل تخطيط الموازنة – تعيين تلقائي – اعتماد سير العمل لإدارة الشؤون المالية</span><span class="sxs-lookup"><span data-stu-id="17a1b-256">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="17a1b-257">في قوالب وقواعد مرحلة تخطيط الموازنة، بالنسبة لكل مرحلة تخطيط موازنة سير عمل، اختر ما إذا كان مسموحًا بإضافة البنود وتعديل البنود والتخطيط الذي يجب استخدامه بشكل افتراضي</span><span class="sxs-lookup"><span data-stu-id="17a1b-257">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="17a1b-258">*ملاحظة: يمكنك إنشاء تخطيطات المستند الإضافية وقم بتعيينها لتكون متوفرة في مرحلة سير عمل تخطيط الموازنة عن طريق النقر فوق الزر تخطيطات بديلة.*</span><span class="sxs-lookup"><span data-stu-id="17a1b-258">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="17a1b-259">[![التخطيطات البديلة](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-259">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="17a1b-260">6.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-260">6.2.</span></span> <span data-ttu-id="17a1b-261">حدد الإجراءات &gt; تنشيط لتنشيط سير عمل تخطيط الموازنة هذا</span><span class="sxs-lookup"><span data-stu-id="17a1b-261">Select Actions &gt; Activate to activate this budget planning workflow</span></span> 

<span data-ttu-id="17a1b-262">[![تنشيط](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-262">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="17a1b-263">تمرين 2: محاكاة العملية</span><span class="sxs-lookup"><span data-stu-id="17a1b-263">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="17a1b-264">المهمة 7: إنشاء البيانات الأولية لخطة الموازنة من دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="17a1b-264">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="17a1b-265">7.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-265">7.1.</span></span> <span data-ttu-id="17a1b-266">انتقل إلى إعداد الموازنة &gt; دوري &gt; إنشاء خطة الموازنة من دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="17a1b-266">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="17a1b-267">قم بتعبئة معلمات العملية الدورية وانقر فوق الزر إنشاء.</span><span class="sxs-lookup"><span data-stu-id="17a1b-267">Fill in the periodic process parameters and click button Generate.</span></span> 

<span data-ttu-id="17a1b-268">[![إنشاء](./media/screenshot29.png)](./media/screenshot29.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-268">[![Generate](./media/screenshot29.png)](./media/screenshot29.png)</span></span> 

<span data-ttu-id="17a1b-269">7.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-269">7.2.</span></span> <span data-ttu-id="17a1b-270">انتقل إلى إعداد الموازنة &gt; خطط الموازنة للبحث عن خطة موازنة تم إنشاؤها بواسطة عملية الإنشاء.</span><span class="sxs-lookup"><span data-stu-id="17a1b-270">Navigate to Budgeting &gt; Budget plans to find a budget plan created by Generate process.</span></span> 

<span data-ttu-id="17a1b-271">[![خطة الموازنة](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-271">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="17a1b-272">7.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-272">7.3.</span></span> <span data-ttu-id="17a1b-273">افتح تفاصيل المستند بالنقر فوق الارتباط التشعبي رقم المستند.</span><span class="sxs-lookup"><span data-stu-id="17a1b-273">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="17a1b-274">يتم عرض خطة الموازنة كما هو محدد في التخطيط الذي تم إنشاؤه أثناء الوجود في هذا المعمل</span><span class="sxs-lookup"><span data-stu-id="17a1b-274">Budget plan is displayed as defined in the layout created during this lab</span></span> 

<span data-ttu-id="17a1b-275">[![عرض خطة الموازنة](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-275">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="17a1b-276">المهمة 8: إنشاء موازنة السنة الحالية استناداً إلى القيم الافتراضية للسنة السابقة</span><span class="sxs-lookup"><span data-stu-id="17a1b-276">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="17a1b-277">يمكن استخدام طرق التوزيع في خطة الموازنة نسخ المعلومات الخاصة بخطط الموازنة بسهولة من سيناريو واحد إلى آخر / نشرها عبر فترات/توزيعها على أبعاد.</span><span class="sxs-lookup"><span data-stu-id="17a1b-277">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="17a1b-278">سوف نستخدم التوزيعات لإنشاء موازنة السنة الحالية من القيم الفعلية للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-278">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="17a1b-279">8.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-279">8.1.</span></span> <span data-ttu-id="17a1b-280">اختر كافة البنود في شبكة مستند خطة الموازنة، وانقر فوق الزر "توزيع الموازنة"</span><span class="sxs-lookup"><span data-stu-id="17a1b-280">Pick all lines in the budget plan document grid and click button allocate budget</span></span> 

<span data-ttu-id="17a1b-281">[![كافة البنود](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-281">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="17a1b-282">8.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-282">8.2.</span></span> <span data-ttu-id="17a1b-283">حدد طريقة التخصيص، والمفتاح الدوري، والمصدر وسيناريوهات الوجهة، ثم انقر فوق تخصيص</span><span class="sxs-lookup"><span data-stu-id="17a1b-283">Select allocation method, Period key, Source and destination scenarios and click Allocate</span></span> 

<span data-ttu-id="17a1b-284">[![توزيع](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-284">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="17a1b-285">سوف يتم نسخ المبالغ الفعلية للعام الماضي إلى موازنة السنة الحالية، وتخصصيها عبر الفترات باستخدام مفتاح فترة منحنى المبيعات.</span><span class="sxs-lookup"><span data-stu-id="17a1b-285">The previous year actual amounts will be copied to current year budget and allocate them across periods using Sales curve period key.</span></span> 

<span data-ttu-id="17a1b-286">[![منحنى المبيعات](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-286">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="17a1b-287">المهمة 9: ضبط مستند خطة الموازنة باستخدام Excel ووضع الصيغة النهائية للمستند</span><span class="sxs-lookup"><span data-stu-id="17a1b-287">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="17a1b-288">9.1.</span><span class="sxs-lookup"><span data-stu-id="17a1b-288">9.1.</span></span> <span data-ttu-id="17a1b-289">انقر فوق الزر ورقة عمل لفتح محتويات المستند في Excel.</span><span class="sxs-lookup"><span data-stu-id="17a1b-289">Click Button worksheet to open document contents in Excel</span></span>

<span data-ttu-id="17a1b-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span></span>

<span data-ttu-id="17a1b-291">9.2.</span><span class="sxs-lookup"><span data-stu-id="17a1b-291">9.2.</span></span> <span data-ttu-id="17a1b-292">عند فتح مصنف Excel، اضبط الأرقام في مستند خطة الموازنة، وانقر فوق الزر نشر.</span><span class="sxs-lookup"><span data-stu-id="17a1b-292">When Excel workbook opens, adjust the numbers in budget plan document and click button Publish.</span></span>

<span data-ttu-id="17a1b-293">[![نشر](./media/screenshot36.png)](./media/screenshot36.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-293">[![Publish](./media/screenshot36.png)](./media/screenshot36.png)</span></span>

<span data-ttu-id="17a1b-294">9.3.</span><span class="sxs-lookup"><span data-stu-id="17a1b-294">9.3.</span></span> <span data-ttu-id="17a1b-295">ارجع إلى مستند خطة الموازنة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17a1b-295">Return to budget plan document in Finance and Operations.</span></span> <span data-ttu-id="17a1b-296">انقر فوق سير العمل &gt; إرسال وذلك لاعتماد المستند تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="17a1b-296">Click Workflow &gt; Submit to Auto-approve the document</span></span>

<span data-ttu-id="17a1b-297">[![الاعتماد التلقائي](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-297">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="17a1b-298">بمجرد اكتمال سير العمل، يتم تغيير مرحلة مستند خطة الموازنة إلى "معتمد".</span><span class="sxs-lookup"><span data-stu-id="17a1b-298">Once workflow completes, budget plan document stage changes to Approved.</span></span> <span data-ttu-id="17a1b-299">[![معتمد](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-299">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="17a1b-300">الملحق</span><span class="sxs-lookup"><span data-stu-id="17a1b-300">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="17a1b-301">الاعتماد التلقائي لتكوين سير العمل</span><span class="sxs-lookup"><span data-stu-id="17a1b-301">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="17a1b-302">أ.</span><span class="sxs-lookup"><span data-stu-id="17a1b-302">A.</span></span> <span data-ttu-id="17a1b-303">إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; ‏‫عمليات سير عمل إعداد الموازنة‬ قم بإنشاء سير عمل جديد باستخدام قالب عمليات سير العمل لتخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-303">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="17a1b-304">[![إنشاء سير عمل جديد](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-304">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="17a1b-305">سوف يحتوي سير العمل هذا على مهمة واحدة فقط- مرحلة الانتقال لخطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="17a1b-305">This workflow will contain only one task – Stage transition budget plan</span></span> 

<span data-ttu-id="17a1b-306">[![مرحلة انتقال خطة الموازنة](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-306">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="17a1b-307">احفظ سير العمل ونشّطه.</span><span class="sxs-lookup"><span data-stu-id="17a1b-307">Save and activate the workflow.</span></span> 

<span data-ttu-id="17a1b-308">ب.</span><span class="sxs-lookup"><span data-stu-id="17a1b-308">B.</span></span> <span data-ttu-id="17a1b-309">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-309">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="17a1b-310">في علامة التبويب "المراحل" قم بإنشاء مرحلتين- الأولية والمرسلة</span><span class="sxs-lookup"><span data-stu-id="17a1b-310">In Stages tab create 2 stages – Initial and Submitted</span></span> 

<span data-ttu-id="17a1b-311">[![الأولى والمرسلة](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-311">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="17a1b-312">ج.</span><span class="sxs-lookup"><span data-stu-id="17a1b-312">C.</span></span> <span data-ttu-id="17a1b-313">انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="17a1b-313">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="17a1b-314">في علامة التبويب "مراحل سير العمل"، قم بإقران الاعتماد التلقائي لسير العمل الذي تم إنشاؤه في خطوة أ مع المرحلتين الأولية والمرسلة</span><span class="sxs-lookup"><span data-stu-id="17a1b-314">In Workflow Stages tab Associate the workflow Auto – approve created in A step with the stages Initial and Submitted</span></span> 

<span data-ttu-id="17a1b-315">[![إعداد الموازنة‬ وتخطيط الموازنة‬](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="17a1b-315">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  




