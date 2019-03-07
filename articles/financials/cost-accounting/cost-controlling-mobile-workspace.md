---
title: مساحة العمل المحمولة للتحكم في التكلفة
description: يقدم هذا الموضوع معلومات حول مساحة العمل المحمولة - التحكم في التكلفة. تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6cdb69f32de2118e685c149605d50b78105c098
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "317558"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="4791b-104">مساحة العمل المحمولة للتحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="4791b-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4791b-105">يقدم هذا الموضوع معلومات حول مساحة العمل المحمولة **التحكم في التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="4791b-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4791b-106">تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.</span><span class="sxs-lookup"><span data-stu-id="4791b-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="4791b-107">مساحة العمل المحمولة هذه مخصصة للاستخدام مع تطبيق Microsoft Dynamics 365 for Unified Operations Mobile.</span><span class="sxs-lookup"><span data-stu-id="4791b-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="4791b-108">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4791b-108">Overview</span></span>
<span data-ttu-id="4791b-109">توفر مساحة العمل المحمولة **التحكم في التكلفة** طريقة عرض فورية للأداء الحالي لمراكز التكلفة من خلال مقارنة التكاليف الفعلية في مقابل التكاليف المُدرجة في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="4791b-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="4791b-110">يمكنك التنقل لأسفل لمشاهدة حالة عناصر التكلفة الفردية.</span><span class="sxs-lookup"><span data-stu-id="4791b-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="4791b-111">على سبيل المثال، يستلم أحد الموظفين دعوة لحضور مؤتمر دولي، ولكن يجب أن تغطي المؤسسة كافة مصروفات السفر.</span><span class="sxs-lookup"><span data-stu-id="4791b-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="4791b-112">يسأل الموظف مديره إذا كان بإمكانه حضور المؤتمر.</span><span class="sxs-lookup"><span data-stu-id="4791b-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="4791b-113">يفتح المدير مساحة العلم المحمولة **التحكم في التكلفة** على جهازه المحمول، لمعرفة إذا ما كان لديه ميزانية تتيح للموظف حضور المؤتمر.</span><span class="sxs-lookup"><span data-stu-id="4791b-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="4791b-114">أمان البيانات</span><span class="sxs-lookup"><span data-stu-id="4791b-114">Data security</span></span>
<span data-ttu-id="4791b-115">تتم حماية البيانات في مساحة العمل المحمولة **التحكم في التكلفة** عبر بيانات اعتماد المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4791b-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="4791b-116">يُسمح لمدير مركز التكلفة فقط برؤية بيانات مركز التكلفة الخاص به.</span><span class="sxs-lookup"><span data-stu-id="4791b-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="4791b-117">تتم إدارة أمان مستوى الوصول ضمن وحدة **محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="4791b-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="4791b-118">يحدد محاسبو التكلفة تكوين مساحة العمل المحمولة **التحكم في التكلفة** في وحدة **التحكم في التكلفة‏‎**.</span><span class="sxs-lookup"><span data-stu-id="4791b-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="4791b-119">بعد نشر مساحة العمل على تطبيق الأجهزة المحمولة، ستكون متوفرة في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4791b-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="4791b-120">وبالتالي، سيتمكن جميع مدراء مراكز التكلفة في المؤسسة من عرض البيانات بالتنسيق نفسه.</span><span class="sxs-lookup"><span data-stu-id="4791b-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="4791b-121">الإجراءات، وطرق العرض والارتباطات</span><span class="sxs-lookup"><span data-stu-id="4791b-121">Actions, views, and links</span></span>
<span data-ttu-id="4791b-122">توفر مساحة العمل المحمولة **التحكم في التكلفة** الإجراءات التالية، وطرق العرض والارتباطات:</span><span class="sxs-lookup"><span data-stu-id="4791b-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="4791b-123">**الإجراءات:**</span><span class="sxs-lookup"><span data-stu-id="4791b-123">**Actions:**</span></span>

    -   <span data-ttu-id="4791b-124">استخدم **تحديد التكوين** لتحديد تخطيط.</span><span class="sxs-lookup"><span data-stu-id="4791b-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="4791b-125">استخدم **حدد الكائن التكلفة** لتحديد مراكز التكلفة لتصفية البيانات عليها.</span><span class="sxs-lookup"><span data-stu-id="4791b-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="4791b-126">تتوقف مراكز التكلفة التي تظهر في القائمة على الوصول الممنوح في وحدة **محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="4791b-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="4791b-127">**طرق العرض:** استنادًا إلى الإجراءات المحددة والتكوين في وحدة **محاسبة التكاليف** يمكنك عرض المعلومات التالية في البطاقات:</span><span class="sxs-lookup"><span data-stu-id="4791b-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="4791b-128">القيمة الفعلية مقابل الموازنة (الفترة الحالية)</span><span class="sxs-lookup"><span data-stu-id="4791b-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="4791b-129">القيمة الفعلية مقابل الموازنة المراجعة (الفترة الحالية)</span><span class="sxs-lookup"><span data-stu-id="4791b-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="4791b-130">الفعلي مقابل الموازنة (الفترة السابقة)</span><span class="sxs-lookup"><span data-stu-id="4791b-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="4791b-131">الفعلي مقابل الموازنة التي تمت مراجعتها (الفترة السابقة)</span><span class="sxs-lookup"><span data-stu-id="4791b-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="4791b-132">الفعلي مقابل الموازنة (السنة حتى تاريخه)</span><span class="sxs-lookup"><span data-stu-id="4791b-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="4791b-133">الفعلي مقابل الموازنة التي تمت مراجعتها (السنة حتى تاريخه)</span><span class="sxs-lookup"><span data-stu-id="4791b-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="4791b-134">تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة والفرق والفرق %.</span><span class="sxs-lookup"><span data-stu-id="4791b-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="4791b-135">**الارتباطات:**</span><span class="sxs-lookup"><span data-stu-id="4791b-135">**Links:**</span></span>

    -   <span data-ttu-id="4791b-136">تفاصيل للفترة الحالية</span><span class="sxs-lookup"><span data-stu-id="4791b-136">Details for current period</span></span>
    -   <span data-ttu-id="4791b-137">تفاصيل للفترة السابقة</span><span class="sxs-lookup"><span data-stu-id="4791b-137">Details for previous period</span></span>
    -   <span data-ttu-id="4791b-138">تفاصيل السنة حتى تاريخه</span><span class="sxs-lookup"><span data-stu-id="4791b-138">Details for year to date</span></span>

    <span data-ttu-id="4791b-139">عندما تقوم بتحديد ارتباط، تظهر بطاقة لكل عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4791b-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="4791b-140">تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة وفرق الموازنة وفرق الموازنة % والموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها %.</span><span class="sxs-lookup"><span data-stu-id="4791b-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="4791b-141">[![بطاقة لعنصر تكلفة ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="4791b-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4791b-142">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="4791b-142">Prerequisites</span></span>
<span data-ttu-id="4791b-143">تختلف المتطلبات الأساسية، استنادًا إلى إصدار Microsoft Dynamics 365 الذي تم نشره لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="4791b-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="4791b-144">المتطلبات الأساسية عند استخدام Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4791b-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="4791b-145">إذا تم نشر Microsoft Dynamics 365 for Finance and Operations لمؤسستك، فيتعين على مسؤول النظام نشر مساحة العمل المحمولة **التحكم في التكلفة‬**.</span><span class="sxs-lookup"><span data-stu-id="4791b-145">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4791b-146">للاطلاع على الإرشادات، راجع [نشر مساحة العمل المحمولة ](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="4791b-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="4791b-147">المتطلبات الأساسية إذا كنت تستخدم الإصدار 1611 من Microsoft Dynamics 365 for Operations مع platform update 3 أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="4791b-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="4791b-148">إذا تم نشر الإصدار 1611 من Microsoft Dynamics 365 for Operations مع platform update 3 أو إصدار أحدث لمؤسستك، فيجب على مسؤول النظام إكمال المتطلبات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="4791b-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4791b-149">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="4791b-149">Prerequisite</span></span></th>
<th><span data-ttu-id="4791b-150">الدور</span><span class="sxs-lookup"><span data-stu-id="4791b-150">Role</span></span></th>
<th><span data-ttu-id="4791b-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4791b-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4791b-152">تطبيق قاعدة المعارف 4013633.</span><span class="sxs-lookup"><span data-stu-id="4791b-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="4791b-153">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="4791b-153">System administrator</span></span></td>

<td><span data-ttu-id="4791b-154">إن KB 4013633 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>التحكم في التكاليف</strong>.</span><span class="sxs-lookup"><span data-stu-id="4791b-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="4791b-155">لتطبيق KB 4013633، يجب أن يتبع مسؤول النظام الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4791b-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="4791b-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">تنزيل الإصلاح العاجل لبيانات التعريف من Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="4791b-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="4791b-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</span><span class="sxs-lookup"><span data-stu-id="4791b-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="4791b-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>SCMMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="4791b-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="4791b-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">تطبيق الحزمة القابلة للنشر</a>.</span><span class="sxs-lookup"><span data-stu-id="4791b-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4791b-160">نشر مساحة العمل المحمولة لـ <strong>التحكم في التكاليف</strong>.</span><span class="sxs-lookup"><span data-stu-id="4791b-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="4791b-161">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="4791b-161">System administrator</span></span></td>
<td><span data-ttu-id="4791b-162">راجع <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></span><span class="sxs-lookup"><span data-stu-id="4791b-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="4791b-163">تحميل وتثبيت تطبيق الجوال</span><span class="sxs-lookup"><span data-stu-id="4791b-163">Download and install the mobile app</span></span>
<span data-ttu-id="4791b-164">تنزيل وتثبيت تطبيق Dynamics 365 for Unified Operations للأجهزة المحمولة:</span><span class="sxs-lookup"><span data-stu-id="4791b-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="4791b-165">لهواتف Android</span><span class="sxs-lookup"><span data-stu-id="4791b-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="4791b-166">لهواتف iPhone</span><span class="sxs-lookup"><span data-stu-id="4791b-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="4791b-167">تسجيل الدخول إلى تطبيق الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="4791b-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="4791b-168">ابدأ تشغيل التطبيق على جهازك المحمول.</span><span class="sxs-lookup"><span data-stu-id="4791b-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="4791b-169">أدخل عنوان URL لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4791b-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="4791b-170">في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="4791b-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="4791b-171">أدخل بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="4791b-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="4791b-172">بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك.</span><span class="sxs-lookup"><span data-stu-id="4791b-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="4791b-173">تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.</span><span class="sxs-lookup"><span data-stu-id="4791b-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="4791b-174">[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="4791b-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="4791b-175">عرض أداء مركز التكلفة باستخدام مساحة العمل المحمولة للتحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="4791b-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="4791b-176">على جهازك المحمول، حدد مساحة عمل **التحكم في التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="4791b-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="4791b-177">حدد **التحكم في كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="4791b-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="4791b-178">حدد **الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="4791b-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="4791b-179">حدد **تحديد التكوين** لتحديد تخطيط التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4791b-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="4791b-180">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="4791b-180">Select **Done**.</span></span>
6.  <span data-ttu-id="4791b-181">حدد **الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="4791b-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="4791b-182">حدد **تحديد كائن التكلفة** لتحديد مراكز التكلفة التي تم منحك حق الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="4791b-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="4791b-183">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="4791b-183">Select **Done**.</span></span>
9.  <span data-ttu-id="4791b-184">عرض الأداء الإجمالي لمركز التكلفة الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="4791b-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="4791b-185">حدد الارتباط **تفاصيل للفترة الحالية**.</span><span class="sxs-lookup"><span data-stu-id="4791b-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="4791b-186">عرض أداء عناصر تكاليف الفردية.</span><span class="sxs-lookup"><span data-stu-id="4791b-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="4791b-187">يمكنك أيضا البحث عن عناصر تكلفة معينة.</span><span class="sxs-lookup"><span data-stu-id="4791b-187">You can also search for specific cost elements.</span></span>

