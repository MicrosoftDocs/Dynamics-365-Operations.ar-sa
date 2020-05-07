---
title: إنشاء عقود متقدمة للفوترة استنادًا إلى التقدم
description: يوضح هذا الموضوع كيفية إنشاء عقود المشاريع لكي يمكنك إنشاء فواتير للعملاء، استنادا إلى النسبة المئوية للعمل المكتمل.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282809"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="c6ab3-103">إنشاء عقود متقدمة للفوترة استنادًا إلى التقدم</span><span class="sxs-lookup"><span data-stu-id="c6ab3-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6ab3-104">يوضح هذا الموضوع كيفية إنشاء عقود المشاريع لكي يمكنك إنشاء فواتير للعملاء، استنادا إلى النسبة المئوية للعمل المكتمل.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="c6ab3-105">ويتم حساب مبالغ الفاتورة تلقائيًا لفئات ميزانية العمل التي قمت بإعدادها للمشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="c6ab3-106">ويتم تعيين توقيت الفاتورة عندما تتفاوض على عقد المشروع مع العميل.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="c6ab3-107">استخدم الإجراءات في هذا الموضوع لإعداد عقد، ومشروع مقترن، وقواعد الفوترة التي تحسب مبالغ الفاتورة لفئات الموازنة الخاصة بالعمل الذي قمت بإعداده للمشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="c6ab3-108">وبعد إنشاء العقد والمشروع، يمكنك إعداد تفاصيل المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="c6ab3-109">على سبيل المثال، يمكنك تحديد الأنشطة وتعيين عمال إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="c6ab3-110">مثال</span><span class="sxs-lookup"><span data-stu-id="c6ab3-110">Example</span></span>

<span data-ttu-id="c6ab3-111">مؤسستك هي شركة تطوير برامج.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-111">Your organization is a software development firm.</span></span> <span data-ttu-id="c6ab3-112">وقد وافقت على تطوير حزمة محاسبية لكشف الرواتب لأحد العملاء برسوم إجمالية 20000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="c6ab3-113">ووافقت مؤسستك على إرسال فاتورة إلى العميل، نظرًا لأنك قمت بإكمال نسب محددة من المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="c6ab3-114">وقمت بإعداد فئات المشروع التالية للعمل، بحيث يمكنك استخدامها في عملية الفوترة:</span><span class="sxs-lookup"><span data-stu-id="c6ab3-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="c6ab3-115">الاستشارة</span><span class="sxs-lookup"><span data-stu-id="c6ab3-115">Consulting</span></span>
- <span data-ttu-id="c6ab3-116">تصميم</span><span class="sxs-lookup"><span data-stu-id="c6ab3-116">Design</span></span>
- <span data-ttu-id="c6ab3-117">التثبيت</span><span class="sxs-lookup"><span data-stu-id="c6ab3-117">Installation</span></span>

<span data-ttu-id="c6ab3-118">وتقوم بإعداد قواعد الفوترة التي تحسب مبالغ الفاتورة تلقائيًا لنسبة العمل بالمشروع التي تم إكمالها لكل فئة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="c6ab3-119">ينشئ مدير الموازنة‬ موازنة لفئات المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="c6ab3-120">يتم حساب مبلغ العمل الذي تم إكماله تلقائيًا كنسبة مئوية من العمل الحقيقي مقارنة بمبالغ الموازنة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c6ab3-121">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="c6ab3-121">Prerequisites</span></span>

<span data-ttu-id="c6ab3-122">قبل إنشاء مشروع يستخدم قواعد الفوترة، يجب إعداد التسلسلات الرقمية لقواعد الفوترة ودفتر يومية الرسوم الذي يتم استخدامة لترحيل فوترة الإنجاز.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="c6ab3-123">انتقل إلى **إدارة المشاريع‬ والمحاسبة** \> **الإعداد** \> **معلمات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="c6ab3-124">في صفحة **معلمات إدارة المشاريع ومحاسبتها**، في علامة تبويب **التسلسلات الرقمية**، قم بإعداد التسلسل الرقمي الذي تريد استخدامه عند إنشاء قواعد الفوترة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="c6ab3-125">انتقل إلى **إدارة المشاريع ومحاسبتها** \> **دفاتر اليومية** \> **الرسوم**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="c6ab3-126">في صفحة **دفتر يومية الرسوم**، حدد **جديد**، ثم أدخل اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="c6ab3-127">إنشاء عقد لفواتير التقدم</span><span class="sxs-lookup"><span data-stu-id="c6ab3-127">Create a contract for progress billings</span></span>

<span data-ttu-id="c6ab3-128">استخدم هذا الإجراء لإنشاء عقد مشروع لمشروع ثابت السعر.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="c6ab3-129">يلزمك إنشاء فاتورة مشروع عندما تصل نسبة العمل المكتمل في المشروع إلى نسبة محددة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="c6ab3-130">انتقل إلى **إدارة المشاريع والمحاسبة** \> **المشاريع** \> **عقود المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="c6ab3-131">في صفحة **عقود المشروع**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="c6ab3-132">في مربع حوار **عقد مشروع جديد**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="c6ab3-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="c6ab3-133">**الاسم**</span><span class="sxs-lookup"><span data-stu-id="c6ab3-133">**Name**</span></span>
    - <span data-ttu-id="c6ab3-134">**نوع التمويل**</span><span class="sxs-lookup"><span data-stu-id="c6ab3-134">**Funding type**</span></span>
    - <span data-ttu-id="c6ab3-135">**مصدر التمويل**</span><span class="sxs-lookup"><span data-stu-id="c6ab3-135">**Funding source**</span></span>
    - <span data-ttu-id="c6ab3-136">**عملة المبيعات** – تُستخدم هذه العملة افتراضيًا لفواتير العميل المقترنة بعقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="c6ab3-137">إلا أنه يمكنك تغيير عملة المبيعات لفاتورة عميل معينة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="c6ab3-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-138">Select **OK**.</span></span> <span data-ttu-id="c6ab3-139">يتم نسخ المعلومات إلى رأس صفحة **عقود المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="c6ab3-140">في صفحة **عقود المشاريع**، قم بملء باقي المعلومات المطلوبة للمشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="c6ab3-141">إنشاء مشروع لفواتير التقدم</span><span class="sxs-lookup"><span data-stu-id="c6ab3-141">Create a project for progress billings</span></span>

<span data-ttu-id="c6ab3-142">اتبع هذه الخطوات لإنشاء مشروع وأية مشاريع فرعية مقترنة بعقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="c6ab3-143">انتقل إلى **إدارة المشاريع والمحاسبة** \> **المشاريع** \> **كافة المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="c6ab3-144">في صفحة **كافة المشاريع**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="c6ab3-145">في مربع الحوار **مشروع جديد**، في حقل **نوع المشروع**، حدد **الوقت والمواد**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="c6ab3-146">حدد مجموعة المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-146">Select a project group.</span></span> <span data-ttu-id="c6ab3-147">تحدد مجموعة المشروع معلومات الترحيل للمشاريع المعينة إلى المجموعة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="c6ab3-148">حدد **إنشاء المشروع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-148">Select **Create project**.</span></span>
6. <span data-ttu-id="c6ab3-149">بعد إنشاء المشروع، عيّن مرحلة المشروع إلى **‏‫قيد التنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="c6ab3-150">إنشاء موازنة لمشروع</span><span class="sxs-lookup"><span data-stu-id="c6ab3-150">Create a budget for a project</span></span>

<span data-ttu-id="c6ab3-151">تُستخدم فئات الموازنة لحساب مبالغ الفاتورة تلقائيًا مقابل نسبة العمل الذي تم إكماله لكل فئة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="c6ab3-152">اتبع الخطوات التالية لإنشاء فئات موازنة للتكاليف التقديرية.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="c6ab3-153">انتقل إلى **إدارة المشاريع والمحاسبة** \> **المشاريع** \> **كافة المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="c6ab3-154">من الصفحة **كافة المشاريع**، حدد وافتح المشروع الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="c6ab3-155">في صفحة **المشاريع**، ومن جزء الإجراءات، الموجود في علامة التبويب **الخطة**، في مجموعة **الموازنة**، حدد**ميزانية المشروع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="c6ab3-156">في صفحة **ميزانية المشروع**، أدخل تكلفة مقدرة لكل فئة في المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="c6ab3-157">إنشاء قواعد فوترة لفواتير التقدم</span><span class="sxs-lookup"><span data-stu-id="c6ab3-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="c6ab3-158">انتقل إلى **إدارة المشاريع والمحاسبة** \> **المشاريع** \> **عقود المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="c6ab3-159">في صفحة **عقود المشاريع**، حدد عقد مشروع وافتحه.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="c6ab3-160">في الصفحة عقد المشروع، في علامة التبويب السريعة**قواعد الفوترة**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="c6ab3-161">في صفحة **قاعدة الفوترة**، في الحقل **نوع البند**، حدد **التقدم**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="c6ab3-162">في علامة التبويب السريعة **تفاصيل بنود قاعدة الفوترة**، في حقل **قيمة العقد**، أدخل القيمة الإجمالية للعقد.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="c6ab3-163">في حقل **الفئة**، حدد الفئة التي تريد ترحيل حركة الرسوم لها.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="c6ab3-164">في حقل **المشروع**، حدد المشروع الذي يستخدم قاعدة الفوترة هذه.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="c6ab3-165">اختياري: قم بتعيين قاعدة الفوترة إلى المشاريع الإضافية.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="c6ab3-166">في علامة التبويب السريعة **المشروع**، في قسم **المشاريع المتوفرة**، حدد مشروعًا، ثم حدد زر سهم لليمين لإضافة المشروع إلى قسم **المشاريع المحددة**.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="c6ab3-167">اختياري: احسب نسبة المبلغ الذي يقتطعه العميل من مدفوعات الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="c6ab3-168">في علامة التبويب السريعة **شروط احتجاز الدفع**، حدد مصدر التمويل، ثم في الحقل **نسبة الاحتجاز**، أدخل النسبة المئوية للاحتجاز.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="c6ab3-169">كرر هذه الخطوات لإنشاء قواعد فوترة إضافية لعقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="c6ab3-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
