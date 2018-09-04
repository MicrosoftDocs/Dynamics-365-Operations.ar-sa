---
title: "محددات تكامل Project Service Automation"
description: "يشرح هذا الموضوع كيفية تكوين طريقة إدخال البيانات الافتراضية عند إجراء تكامل بين Microsoft Dynamics 365 for Project Service Automation وMicrosoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="1974d-103">محددات تكامل Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1974d-103">Project Service Automation integration parameters</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1974d-104">في صفحة **محددات تكامل Project Service Automation**، يمكنك تكوين طريقة إدخال البيانات الافتراضية عند إجراء تكامل بين Microsoft Dynamics 365 for Project Service Automation وMicrosoft Dynamics 365 for Finance and Operations.‬</span><span class="sxs-lookup"><span data-stu-id="1974d-104">On the **Project Service Automation integration parameters** page, you can configure how default data is entered when you integrate Microsoft Dynamics 365 for Project Service Automation with Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1974d-105">لكي تتم مزامنة المشاريع بشكل ناجح من Project Service Automation إلى Finance and Operations، يجب إعداد الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="1974d-105">For projects to be successfully synchronized from Project Service Automation to Finance and Operations, you must set up the following fields.</span></span>

> [!NOTE]
> - <span data-ttu-id="1974d-106">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1974d-106">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="1974d-107">يتوافر تكامل القيم الفعلية في Microsoft Dynamics 365 for Finance and Operations، الإصدار 8.01 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="1974d-107">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="1974d-108">إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستتمكن من استخدام القوالب لإجراء تكامل لمهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية ولتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1974d-108">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="1974d-109">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="1974d-109">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>

| <span data-ttu-id="1974d-110">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="1974d-110">Tab</span></span>                    | <span data-ttu-id="1974d-111">الحقل</span><span class="sxs-lookup"><span data-stu-id="1974d-111">Field</span></span>                | <span data-ttu-id="1974d-112">الوصف</span><span class="sxs-lookup"><span data-stu-id="1974d-112">Description</span></span> |
|------------------------|----------------------|-------------|
| <span data-ttu-id="1974d-113">عام</span><span class="sxs-lookup"><span data-stu-id="1974d-113">General</span></span>                | <span data-ttu-id="1974d-114">نوع المشروع الافتراضي</span><span class="sxs-lookup"><span data-stu-id="1974d-114">Default project type</span></span> | <span data-ttu-id="1974d-115">حدد نوع المشروع الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="1974d-115">Select the default project type.</span></span> <span data-ttu-id="1974d-116">عند مزامنة المشاريع من Project Service Automation، تُستخدم هذه القيمة إذا لم تحدد قيمة افتراضية في قالب التكامل.</span><span class="sxs-lookup"><span data-stu-id="1974d-116">When projects are synchronized from Project Service Automation, this value is used if you didn't provide a default value in the integration template.</span></span> <span data-ttu-id="1974d-117">أثناء المزامنة، يتم تعيين حقل **نوع المشروع** للمشاريع الجديدة إلى هذه القيمة.</span><span class="sxs-lookup"><span data-stu-id="1974d-117">During synchronization, the **Project type** field of new projects is set to this value.</span></span> <span data-ttu-id="1974d-118">ومع ذلك، قد يتم تحديث القيمة عندما تتم مزامنة بنود عقد المشروع من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1974d-118">However, the value might be updated when the project contract lines are synchronized from Project Service Automation.</span></span> |
|                        | <span data-ttu-id="1974d-119">فئة الوقت</span><span class="sxs-lookup"><span data-stu-id="1974d-119">Time category</span></span>        | <span data-ttu-id="1974d-120">حدد فئة الوقت الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="1974d-120">Select the default time category.</span></span> <span data-ttu-id="1974d-121">يتم استخدام هذه القيمة عند مزامنة تقديرات الساعات من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1974d-121">This value is used when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="1974d-122">عند مزامنة تقديرات الساعات والقيم الفعلية للساعات من Project Service Automation، يتم تعيين حقل **الفئة** لتقديرات ساعات المشروع الجديد في Finance and Operations إلى هذه القيمة.</span><span class="sxs-lookup"><span data-stu-id="1974d-122">When the hour estimates and hour actuals are synchronized from Project Service Automation, the **Category** field of new project hour forecasts in Finance and Operations is set to this value.</span></span> |
|                        | <span data-ttu-id="1974d-123">فئة الرسوم</span><span class="sxs-lookup"><span data-stu-id="1974d-123">Fee category</span></span>         | <span data-ttu-id="1974d-124">حدد فئة الرسوم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="1974d-124">Select the default fee category.</span></span> <span data-ttu-id="1974d-125">يتم استخدام هذه القيمة عند مزامنة القيم الفعلية للرسوم من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1974d-125">This value is used when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="1974d-126">عند مزامنة القيم الفعلية للرسوم من Project Service Automation، يتم تعيين حقل **الفئة** لحركات الرسوم الجديدة في Finance and Operations إلى هذه القيمة.</span><span class="sxs-lookup"><span data-stu-id="1974d-126">When the fee actuals are synchronized from Project Service Automation, the **Category** field of new fee transactions in Finance and Operations is set to this value.</span></span> |
| <span data-ttu-id="1974d-127">القيم الافتراضية لمجموعة المشاريع</span><span class="sxs-lookup"><span data-stu-id="1974d-127">Project group defaults</span></span> | <span data-ttu-id="1974d-128">نوع المشروع</span><span class="sxs-lookup"><span data-stu-id="1974d-128">Project type</span></span>         | <span data-ttu-id="1974d-129">انقر فوق **جديد** لإضافة صف حيث يمكنك تحديد نوع المشروع لتعيين مجموعة المشاريع الافتراضية له.</span><span class="sxs-lookup"><span data-stu-id="1974d-129">Click **New** to add a row where you can select the project type to set the default project group for.</span></span> <span data-ttu-id="1974d-130">يمكن تحديد نوع مشروع محدد مرة واحدة فقط في التكوين.</span><span class="sxs-lookup"><span data-stu-id="1974d-130">A specific project type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="1974d-131">تصنيف المشروع</span><span class="sxs-lookup"><span data-stu-id="1974d-131">Project group</span></span>        | <span data-ttu-id="1974d-132">حدد مجموعة المشاريع الافتراضية لنوع المشروع المحدد.</span><span class="sxs-lookup"><span data-stu-id="1974d-132">Select the default project group for the selected project type.</span></span> <span data-ttu-id="1974d-133">عند مزامنة مشروعات جديدة من Project Service Automation، يتم تعيين حقل **مجموعة المشاريع** إلى القيمة الافتراضية لنوع المشروع إذا لم تحدد قيمة افتراضية في قالب التكامل.</span><span class="sxs-lookup"><span data-stu-id="1974d-133">When new projects are synchronized from Project Service Automation, the **Project group** field is set to the default value for the project type if you didn't provide a default value in the integration template.</span></span> |
| <span data-ttu-id="1974d-134">القيم الافتراضية لنوع الفوترة</span><span class="sxs-lookup"><span data-stu-id="1974d-134">Billing type defaults</span></span>  | <span data-ttu-id="1974d-135">نوع الفوترة</span><span class="sxs-lookup"><span data-stu-id="1974d-135">Billing type</span></span>         | <span data-ttu-id="1974d-136">انقر فوق **جديد** لإضافة صف حيث يمكنك تحديد نوع الفوترة لتعيين خاصية البند الافتراضي له.</span><span class="sxs-lookup"><span data-stu-id="1974d-136">Click **New** to add a row where you can select the billing type to set the default line property for.</span></span> <span data-ttu-id="1974d-137">يمكن تحديد نوع فوترة محدد مرة واحدة فقط في التكوين.</span><span class="sxs-lookup"><span data-stu-id="1974d-137">A specific billing type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="1974d-138">خاصية السطر</span><span class="sxs-lookup"><span data-stu-id="1974d-138">Line property</span></span>        | <span data-ttu-id="1974d-139">حدد خاصية البند الافتراضي لنوع الفوترة المحدد.</span><span class="sxs-lookup"><span data-stu-id="1974d-139">Select the default line property for the selected billing type.</span></span> <span data-ttu-id="1974d-140">عند مزامنة تقديرات عدد الساعات الجديدة أو تقديرات المصروفات الجديدة أو القيم الفعلية الجديدة من Project Service Automation، يتم تعيين حقل **خاصية البند** إلى القيمة الافتراضية لنوع الفوترة.</span><span class="sxs-lookup"><span data-stu-id="1974d-140">When new hour estimates, new expense estimates, or new actuals are synchronized from Project Service Automation, the **Line property** field is set to the default value for the billing type.</span></span> |
| <span data-ttu-id="1974d-141">تأمين الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1974d-141">Functionality locking</span></span>  | <span data-ttu-id="1974d-142">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1974d-142">Not applicable</span></span>       | <span data-ttu-id="1974d-143">حدد الوظيفة التي يتم عندها التعطيل في Finance and Operations بالنسبة للمشاريع والعقود التي تم إنشاؤها من Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1974d-143">Select the functionality to disable in Finance and Operations for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="1974d-144">على سبيل المثال، يمكنك إيقاف تشغيل القدرة على تحرير العقود والمشاريع، وإنشاء هياكل تنظيم العمل وإدخال جداول زمنية في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1974d-144">For example, you can turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance and Operations.</span></span> <span data-ttu-id="1974d-145">سوف يستمر تمكين الحقول المرتبطة بالمحاسبة، حتى لو ألغيت إتاحتها من خلال إعداد المُعلمة.</span><span class="sxs-lookup"><span data-stu-id="1974d-145">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="1974d-146">بشكل افتراضي، تكون كافة الوظائف ممكّنة.</span><span class="sxs-lookup"><span data-stu-id="1974d-146">By default, all functionality is enabled.</span></span> |
