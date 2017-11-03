---
title: "مستندات تبرير تخطيط الموازنة"
description: "توفر مستندات التبرير سردًا لأولئك الذي يطلبون موازنة لتوضيح ضرورة وجود موازنة محددة."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b033f6197e61a6030e12081a9e4f1d820bac458f
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="6c651-103">مستندات تبرير تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="6c651-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6c651-104">توفر مستندات التبرير سردًا لأولئك الذي يطلبون موازنة لتوضيح ضرورة وجود موازنة محددة.</span><span class="sxs-lookup"><span data-stu-id="6c651-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="6c651-105">يتم إنشاء قالب خطة الموازنة من خلال مدير الموازنة في Microsoft Word، ويتم تعيينه إلى عملية تخطيط الموازنة الحالية.</span><span class="sxs-lookup"><span data-stu-id="6c651-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="6c651-106">بعد ذلك، يمكن لملاك الموازنة فتح القالب، وملء البيانات تلقائيًا في Word بناءً على طلبهم للموازنة.</span><span class="sxs-lookup"><span data-stu-id="6c651-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="6c651-107">ثم يمكنهم بعد ذلك إضافة نص إضافي أو البيانات قبل حفظ وإرفاق مستندات مبرراتهم الشخصية لخطة الموازنة الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="6c651-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="6c651-108">قم بإعداد وظيفة Office الإضافية لـ Microsoft Dynamics لـ Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6c651-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="6c651-109">فتح مستند Microsoft Word جديد.</span><span class="sxs-lookup"><span data-stu-id="6c651-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="6c651-110">انقر فوق **إدراج** على الشريط، ثم انقر فوق **متجر**.</span><span class="sxs-lookup"><span data-stu-id="6c651-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="6c651-111">ابحث عن وظيفة Office الإضافية لـ Microsoft Dynamics، وانقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6c651-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="6c651-112">في Word، في الجزء الأيمن، انقر فوق **إضافة معلومات الخادم**.</span><span class="sxs-lookup"><span data-stu-id="6c651-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="6c651-113">اكتب أو الصق عنوان URL للخادم، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c651-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="6c651-114">حدد قالب التبرير في Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6c651-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="6c651-115">انقر فوق **التصميم** في وظيفة Office الإضافية لـ Microsoft Dynamics بعد أن قمت بتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="6c651-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="6c651-116">بالنسبة لمعلومات العنوان، استخدم زر **إضافة حقول**.</span><span class="sxs-lookup"><span data-stu-id="6c651-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="6c651-117">قم بتحديد مصدر بيانات الكيان لـ BudgetPlanJustification، ثم انقر فوق **التالي**.</span><span class="sxs-lookup"><span data-stu-id="6c651-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="6c651-118">**ملاحظة:** هذا الكيان مطلوب لأي مستند تبرير.</span><span class="sxs-lookup"><span data-stu-id="6c651-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="6c651-119">يمكن استخدام الكيانات الأخرى، ولكن سفيشل التحميل للرجوع إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إذا لم يتم تضمين هذا الكيان.</span><span class="sxs-lookup"><span data-stu-id="6c651-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="6c651-120">إضافة تسميات وقيم BudgetPlanName وBudgetPlanPreparer وResponsibilityCenter وDocumentNumber في مستند Word.</span><span class="sxs-lookup"><span data-stu-id="6c651-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="6c651-121">**ملاحظة:** يمكنك استخدام التسميات المخصصة لك بدلاً من التسميات القياسية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="6c651-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="6c651-122">انقر فوق **تم** لإكمال قسم العنوان.</span><span class="sxs-lookup"><span data-stu-id="6c651-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="6c651-123">بالنسبة لتفاصيل مستوى بنود مبالغ خطة الموازنة، انقر فوق **إضافة جدول**.</span><span class="sxs-lookup"><span data-stu-id="6c651-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="6c651-124">مرة أخرى، قم بتحديد مصدر بيانات الكيان لـ BudgetPlanJustification، ثم انقر فوق **التالي**.</span><span class="sxs-lookup"><span data-stu-id="6c651-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="6c651-125">قم بإضافة حقول إلى EffectiveDate وScenarioName وAccountDisplayValue و AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="6c651-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="6c651-126">**ملاحظة:** إذا توفرت إضافة تعليقات ضمن بنود خطة الموازنة الفردية، فمن ثم يمكن إضافة هذه التعليمات إلى الجدول هنا.</span><span class="sxs-lookup"><span data-stu-id="6c651-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="6c651-127">قم بإضافة أي تعليمات إضافية لتقديمها للمستخدم النهائي، وإجراء أي تنسيق ضروري أو أنماط إلى المستند.</span><span class="sxs-lookup"><span data-stu-id="6c651-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="6c651-128">قم بحفظ المستند إلى الكمبيوتر المحلي الخاص بك، وأغلق الملف قبل المتابعة.</span><span class="sxs-lookup"><span data-stu-id="6c651-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="6c651-129">قم بإعداد عملية التخطيط للموازنة لاستخدام قالب التبرير.</span><span class="sxs-lookup"><span data-stu-id="6c651-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="6c651-130">في Finance and Operations، انتقل إلى **إعداد الموازنة** &gt; **إعداد** &gt; **تخطيط الموازنة** &gt; **‎قوالب مستندات التبرير**.</span><span class="sxs-lookup"><span data-stu-id="6c651-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="6c651-131">انقر فوق **جديد** واستعرض مستند Microsoft Word الذي تم إنشاؤه حديثًا.</span><span class="sxs-lookup"><span data-stu-id="6c651-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="6c651-132">أدخل اسم عرض قالب ووصفًا.</span><span class="sxs-lookup"><span data-stu-id="6c651-132">Enter a template display name and description.</span></span> <span data-ttu-id="6c651-133">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c651-133">Click **OK**.</span></span>
4.  <span data-ttu-id="6c651-134">انتقل إلى **إعداد الموازنة** &gt; **إعداد** &gt; **الموازنة** **تخطيط** &gt; **عملية تخطيط الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="6c651-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="6c651-135">حدد العملية التي يجب فيها استخدام قالب التبرير، وانقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="6c651-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="6c651-136">في حقل **قالب مستند تبرير**، حدد القالب المناسب ثم انقر حفظ.</span><span class="sxs-lookup"><span data-stu-id="6c651-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="6c651-137">تحرير وحفظ مستندات التبرير المخصصة</span><span class="sxs-lookup"><span data-stu-id="6c651-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="6c651-138">في Finance and Operations، قم بإنشاء خطة موازنة جديدة أو فتح خطة الموازنة الموجود.</span><span class="sxs-lookup"><span data-stu-id="6c651-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="6c651-139">في قائمة **تبرير** المنسدلة، حدد **إنشاء مبررات جديدة**.</span><span class="sxs-lookup"><span data-stu-id="6c651-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="6c651-140">بعد ملء التفاصيل، حدد تحميل المستند المخصص من قائمة **تبرير** المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="6c651-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





