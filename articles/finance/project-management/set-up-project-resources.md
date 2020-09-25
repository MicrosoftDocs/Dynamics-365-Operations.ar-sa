---
title: إعداد موارد المشروع
description: يوفر هذا الموضوع معلومات حول إعداد موارد المشروع أو طلبها‬.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760468"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="134c7-103">إعداد موارد المشروع</span><span class="sxs-lookup"><span data-stu-id="134c7-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="134c7-104">يجب إعداد تقويم وربطه بموظف أو عامل.</span><span class="sxs-lookup"><span data-stu-id="134c7-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="134c7-105">يستخدم التقويم لجدولة المشروع ووقت عمل الموارد التي تم حجزها للمشروع.</span><span class="sxs-lookup"><span data-stu-id="134c7-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="134c7-106">أثناء إعداد التقويم، بإمكان مدراء المشاريع تنفيذ تسوية الموارد كجزء من تحسين الموارد.</span><span class="sxs-lookup"><span data-stu-id="134c7-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="134c7-107">استنادًا إلى جدول التقويم، يمكن وضع قيود على الموارد.</span><span class="sxs-lookup"><span data-stu-id="134c7-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="134c7-108">يمكنك إعداد تقويم على صفحة **تقويمات**.</span><span class="sxs-lookup"><span data-stu-id="134c7-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="134c7-109">عندما تقوم بإعداد عامل كمورد مشروع، يمكنك الاختيار من ضمن العاملين في الشركة التي تعمل على إعداد الموارد لها.</span><span class="sxs-lookup"><span data-stu-id="134c7-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="134c7-110">بدلاً من ذلك، يمكنك اختيار عاملين من شركات أخرى في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="134c7-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="134c7-111">يعرف العاملون من هذا النوع بالموارد بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="134c7-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="134c7-112">تشرح الإجراءات التالية كيفية إعداد عامل كمورد مشروع في شركتك، وكيفية إعداد مورد مشروع بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="134c7-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="134c7-113">إعداد عامل كمورد مشروع</span><span class="sxs-lookup"><span data-stu-id="134c7-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="134c7-114">في صفحة **العاملون**، في قائمة **العاملون**، حدد العامل الذي تضيفه كمورد مشروع وافتح سجل العامل.</span><span class="sxs-lookup"><span data-stu-id="134c7-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="134c7-115">في جزء الإجراءات، حدد **مشروع** &gt; **إعداد** &gt; **إعداد المشروع**.</span><span class="sxs-lookup"><span data-stu-id="134c7-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="134c7-116">حدد التقويم، ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="134c7-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="134c7-117">يمكنك أيضًا تحديد مشاريع افتراضية لأحد الموارد كنوع من التعيين المسبق.</span><span class="sxs-lookup"><span data-stu-id="134c7-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="134c7-118">يمكن استخدام التعيينات المسبقة عندما يكون مدير الموارد أو مدير المشروع على علم مسبق بالمشاريع التي سيعمل عليها المورد.</span><span class="sxs-lookup"><span data-stu-id="134c7-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="134c7-119">يمكن أيضًا إنشاء التعيينات المسبقة بالاستناد إلى طلب الجهة الراعية للمشروع أو العميل.</span><span class="sxs-lookup"><span data-stu-id="134c7-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="134c7-120">لتعيين مشروع بشكل مسبق، في صفحة **تعيين المشاريع**، على علامة تبويب **المشاريع**، في قائمة **المشاريع المتبقية**، حدد المشروع المناسب.</span><span class="sxs-lookup"><span data-stu-id="134c7-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="134c7-121">إعداد مورد بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="134c7-121">Set up an intercompany resource</span></span>

<span data-ttu-id="134c7-122">عندما تقوم بإعداد عامل كمورد بين الشركات الشقيقة، يجب عليك إتمام الإعداد في كل من الشركة المُقرضة والشركة المقترضة.</span><span class="sxs-lookup"><span data-stu-id="134c7-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="134c7-123">في الشركة المُقرضة</span><span class="sxs-lookup"><span data-stu-id="134c7-123">In the lending company</span></span>

1. <span data-ttu-id="134c7-124">في Finance، تحقق من أن الشركة المُقرضة تم تحديدها، ثم أكمل الإجراء الوارد في المقطع السابق، "إعداد عامل كمورد مشروع".</span><span class="sxs-lookup"><span data-stu-id="134c7-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="134c7-125">في صفحة **المحاسبة بين الشركات الشقيقة**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="134c7-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="134c7-126">في حقل **مُعرف الكيان القانوني**، حدد الشركة المُقرضة.</span><span class="sxs-lookup"><span data-stu-id="134c7-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="134c7-127">قم بملء الحقول المتبقية على النحو المناسب، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="134c7-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="134c7-128">في صفحة **سعر التحويل**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="134c7-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="134c7-129">في حقل **الكيان القانوني المقترض**، حدد الشركة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="134c7-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="134c7-130">إذا كنت تريد إقراض الشركة المقترضة فقط المورد الذي قمت بإنشائه في بداية هذا القسم، في حقل **المورد**، حدد اسم المورد الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="134c7-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="134c7-131">لإتاحة جميع الموارد في الشركة المُقرضة للشركة المُقترضة، اترك حقل **المورد** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="134c7-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="134c7-132">في صفحة **محددات إدارة المشاريع ومحاسبتها‬**، على علامة التبويب **بين الشركات الشقيقة**، عيّن الخيار **تمكين الجداول الزمنية وجدولة الموارد بين الشركات الشقيقة‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="134c7-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="134c7-133">في الشركة المُقترضة</span><span class="sxs-lookup"><span data-stu-id="134c7-133">In the borrowing company</span></span>

- <span data-ttu-id="134c7-134">في صفحة **قائمة الموارد**، في عامل تصفية البحث، أدخل اسم المورد الذي أنشأته في للشركة المُقرضة‬‏‫ للتحقق من تضمين الاسم في قائمة الموارد للشركة المُقترضة.</span><span class="sxs-lookup"><span data-stu-id="134c7-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="134c7-135">طلب موارد المشروع</span><span class="sxs-lookup"><span data-stu-id="134c7-135">Request project resources</span></span>
<span data-ttu-id="134c7-136">تسمح وظيفة جدولة موارد المشروع فقط لمديري الموارد بتوزيع الموارد التي تم تعيين عاملين لها على المشاركات أو المشاريع.</span><span class="sxs-lookup"><span data-stu-id="134c7-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="134c7-137">لتمكين هذه الوظيفة، أكمل المهام التالية، أو تأكد من استكمالها:</span><span class="sxs-lookup"><span data-stu-id="134c7-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="134c7-138">إعداد التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="134c7-138">Set up number sequences.</span></span>
- <span data-ttu-id="134c7-139">إعداد عمليات سير العمل الخاصة بإدارة المشروع والمحاسبة.</span><span class="sxs-lookup"><span data-stu-id="134c7-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="134c7-140">تمكين مهام سير عمل طلب المورد.</span><span class="sxs-lookup"><span data-stu-id="134c7-140">Enable resource request workflows.</span></span>

<span data-ttu-id="134c7-141">بعد استكمال المهام السابقة، يمكنك إكمال المهام التالية وفق ما تقتضي الحاجة:</span><span class="sxs-lookup"><span data-stu-id="134c7-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="134c7-142">إنشاء طلب مورد من مورد الحجز المبدئي للعمالة الموظفة.</span><span class="sxs-lookup"><span data-stu-id="134c7-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="134c7-143">مراقبة طلبات المورد</span><span class="sxs-lookup"><span data-stu-id="134c7-143">Monitor resource requests.</span></span>
- <span data-ttu-id="134c7-144">تحقيق طلبات الموارد.</span><span class="sxs-lookup"><span data-stu-id="134c7-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="134c7-145">طلب مورد تم تعيين عاملين له من WBS.</span><span class="sxs-lookup"><span data-stu-id="134c7-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="134c7-146">حجز الموارد لمشروع من دون الحصول على طلب مورد تم تعيين عاملين له.</span><span class="sxs-lookup"><span data-stu-id="134c7-146">Book resources to a project without having a request for a staffed resource.</span></span>
