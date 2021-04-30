---
title: مساحة العمل المحمولة للتحكم في التكلفة
description: يقدم هذا الموضوع معلومات حول مساحة العمل المحمولة - التحكم في التكلفة. تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.
author: AndersGirke
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 569f932b256054f2d93a6d699ca5d5af3da08ca6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897926"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="1ff86-104">مساحة العمل المحمولة للتحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="1ff86-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ff86-105">يقدم هذا الموضوع معلومات حول مساحة العمل المحمولة **التحكم في التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="1ff86-106">تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.</span><span class="sxs-lookup"><span data-stu-id="1ff86-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="1ff86-107">مساحة العمل المحمولة هذه مخصصة للاستخدام مع تطبيق Finance and Operations للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="1ff86-108">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1ff86-108">Overview</span></span>
<span data-ttu-id="1ff86-109">توفر مساحة العمل المحمولة **التحكم في التكلفة** طريقة عرض فورية للأداء الحالي لمراكز التكلفة من خلال مقارنة التكاليف الفعلية في مقابل التكاليف المُدرجة في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="1ff86-110">يمكنك التنقل لأسفل لمشاهدة حالة عناصر التكلفة الفردية.</span><span class="sxs-lookup"><span data-stu-id="1ff86-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="1ff86-111">على سبيل المثال، يستلم أحد الموظفين دعوة لحضور مؤتمر دولي، ولكن يجب أن تغطي المؤسسة كافة مصروفات السفر.</span><span class="sxs-lookup"><span data-stu-id="1ff86-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="1ff86-112">يسأل الموظف مديره إذا كان بإمكانه حضور المؤتمر.</span><span class="sxs-lookup"><span data-stu-id="1ff86-112">The employee asks their manager whether they can attend the conference.</span></span> <span data-ttu-id="1ff86-113">يفتح المدير مساحة العمل المحمولة **التحكم في التكلفة** على جهازه المحمول، لمعرفة إذا ما كان لديه ميزانية تتيح للموظف حضور المؤتمر أم لا.</span><span class="sxs-lookup"><span data-stu-id="1ff86-113">The manager opens the **Cost controlling** mobile workspace on their mobile device to see whether there is budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="1ff86-114">أمان البيانات</span><span class="sxs-lookup"><span data-stu-id="1ff86-114">Data security</span></span>
<span data-ttu-id="1ff86-115">تتم حماية البيانات في مساحة العمل المحمولة **التحكم في التكلفة** عبر بيانات اعتماد المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1ff86-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="1ff86-116">يُسمح لمدير مركز التكلفة فقط برؤية بيانات مركز التكلفة الخاص به.</span><span class="sxs-lookup"><span data-stu-id="1ff86-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="1ff86-117">تتم إدارة أمان مستوى الوصول ضمن وحدة **محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="1ff86-118">يحدد محاسبو التكلفة تكوين مساحة العمل المحمولة **التحكم في التكلفة** في وحدة **التحكم في التكلفة‏‎**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="1ff86-119">بعد نشر مساحة العمل على تطبيق الأجهزة المحمولة، ستكون متوفرة في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="1ff86-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="1ff86-120">وبالتالي، سيتمكن جميع مدراء مراكز التكلفة في المؤسسة من عرض البيانات بالتنسيق نفسه.</span><span class="sxs-lookup"><span data-stu-id="1ff86-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="1ff86-121">الإجراءات، وطرق العرض والارتباطات</span><span class="sxs-lookup"><span data-stu-id="1ff86-121">Actions, views, and links</span></span>
<span data-ttu-id="1ff86-122">توفر مساحة العمل المحمولة **التحكم في التكلفة** الإجراءات التالية، وطرق العرض والارتباطات:</span><span class="sxs-lookup"><span data-stu-id="1ff86-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="1ff86-123">**الإجراءات:**</span><span class="sxs-lookup"><span data-stu-id="1ff86-123">**Actions:**</span></span>

    -   <span data-ttu-id="1ff86-124">استخدم **تحديد التكوين** لتحديد تخطيط.</span><span class="sxs-lookup"><span data-stu-id="1ff86-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="1ff86-125">استخدم **حدد الكائن التكلفة** لتحديد مراكز التكلفة لتصفية البيانات عليها.</span><span class="sxs-lookup"><span data-stu-id="1ff86-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="1ff86-126">تتوقف مراكز التكلفة التي تظهر في القائمة على الوصول الممنوح في وحدة **محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="1ff86-127">**طرق العرض:** استنادًا إلى الإجراءات المحددة والتكوين في وحدة **محاسبة التكاليف** يمكنك عرض المعلومات التالية في البطاقات:</span><span class="sxs-lookup"><span data-stu-id="1ff86-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="1ff86-128">القيمة الفعلية مقابل الموازنة (الفترة الحالية)</span><span class="sxs-lookup"><span data-stu-id="1ff86-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="1ff86-129">القيمة الفعلية مقابل الموازنة المراجعة (الفترة الحالية)</span><span class="sxs-lookup"><span data-stu-id="1ff86-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="1ff86-130">الفعلي مقابل الموازنة (الفترة السابقة)</span><span class="sxs-lookup"><span data-stu-id="1ff86-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="1ff86-131">الفعلي مقابل الموازنة التي تمت مراجعتها (الفترة السابقة)</span><span class="sxs-lookup"><span data-stu-id="1ff86-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="1ff86-132">الفعلي مقابل الموازنة (السنة حتى تاريخه)</span><span class="sxs-lookup"><span data-stu-id="1ff86-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="1ff86-133">الفعلي مقابل الموازنة التي تمت مراجعتها (السنة حتى تاريخه)</span><span class="sxs-lookup"><span data-stu-id="1ff86-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="1ff86-134">تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة والفرق والفرق %.</span><span class="sxs-lookup"><span data-stu-id="1ff86-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="1ff86-135">**الارتباطات:**</span><span class="sxs-lookup"><span data-stu-id="1ff86-135">**Links:**</span></span>

    -   <span data-ttu-id="1ff86-136">تفاصيل للفترة الحالية</span><span class="sxs-lookup"><span data-stu-id="1ff86-136">Details for current period</span></span>
    -   <span data-ttu-id="1ff86-137">تفاصيل للفترة السابقة</span><span class="sxs-lookup"><span data-stu-id="1ff86-137">Details for previous period</span></span>
    -   <span data-ttu-id="1ff86-138">تفاصيل السنة حتى تاريخه</span><span class="sxs-lookup"><span data-stu-id="1ff86-138">Details for year to date</span></span>

    <span data-ttu-id="1ff86-139">عندما تقوم بتحديد ارتباط، تظهر بطاقة لكل عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="1ff86-140">تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة وفرق الموازنة وفرق الموازنة % والموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها %.</span><span class="sxs-lookup"><span data-stu-id="1ff86-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="1ff86-141">[![بطاقة لعنصر تكلفة ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="1ff86-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1ff86-142">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="1ff86-142">Prerequisites</span></span>
<span data-ttu-id="1ff86-143">تختلف المتطلبات الأساسية، استنادًا إلى إصدار Microsoft Dynamics 365 الذي تم نشره لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="1ff86-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="1ff86-144">المتطلبات الأساسية عند استخدام Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1ff86-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="1ff86-145">إذا تم نشر Finance لمؤسستك، فيتعين على مسؤول النظام نشر مساحة العمل المحمولة **التحكم في التكلفة**‬.</span><span class="sxs-lookup"><span data-stu-id="1ff86-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="1ff86-146">للاطلاع على الإرشادات، راجع [نشر مساحة العمل المحمولة ](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1ff86-146">For instructions, see [Publish a mobile workspace](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="1ff86-147">المتطلبات الأساسية إذا كنت تستخدم الإصدار 1611 مع Platform update 3 أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="1ff86-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="1ff86-148">إذا تم نشر الإصدار 1611 مع Platform update 3 أو إصدار أحدث لمؤسستك، فيجب على مسؤول النظام إكمال المتطلبات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="1ff86-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1ff86-149">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="1ff86-149">Prerequisite</span></span></th>
<th><span data-ttu-id="1ff86-150">الدور</span><span class="sxs-lookup"><span data-stu-id="1ff86-150">Role</span></span></th>
<th><span data-ttu-id="1ff86-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="1ff86-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ff86-152">تطبيق قاعدة المعارف 4013633.</span><span class="sxs-lookup"><span data-stu-id="1ff86-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="1ff86-153">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="1ff86-153">System administrator</span></span></td>

<td><span data-ttu-id="1ff86-154">إن KB 4013633 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>التحكم في التكاليف</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff86-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="1ff86-155">لتطبيق KB 4013633، يجب أن يتبع مسؤول النظام الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1ff86-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="1ff86-156"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">تنزيل الإصلاح العاجل لبيانات التعريف من Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="1ff86-156"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="1ff86-157"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</span><span class="sxs-lookup"><span data-stu-id="1ff86-157"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="1ff86-158"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>SCMMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="1ff86-158"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="1ff86-159"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">تطبيق الحزمة القابلة للنشر</a>.</span><span class="sxs-lookup"><span data-stu-id="1ff86-159"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ff86-160">نشر مساحة العمل المحمولة لـ <strong>التحكم في التكاليف</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff86-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="1ff86-161">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="1ff86-161">System administrator</span></span></td>
<td><span data-ttu-id="1ff86-162">راجع <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">نشر مساحة عمل محمولة</a></span><span class="sxs-lookup"><span data-stu-id="1ff86-162">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="1ff86-163">تنزيل وتثبيت تطبيق المحمول</span><span class="sxs-lookup"><span data-stu-id="1ff86-163">Download and install the mobile app</span></span>
<span data-ttu-id="1ff86-164">تنزيل وتثبيت تطبيق Finance and Operations للأجهزة المحمولة:</span><span class="sxs-lookup"><span data-stu-id="1ff86-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="1ff86-165">لهواتف Android</span><span class="sxs-lookup"><span data-stu-id="1ff86-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="1ff86-166">لهواتف iPhone</span><span class="sxs-lookup"><span data-stu-id="1ff86-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="1ff86-167">تسجيل الدخول إلى تطبيق الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="1ff86-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="1ff86-168">ابدأ تشغيل التطبيق على جهازك المحمول.</span><span class="sxs-lookup"><span data-stu-id="1ff86-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="1ff86-169">أدخل عنوان URL لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1ff86-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="1ff86-170">في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1ff86-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="1ff86-171">أدخل بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="1ff86-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="1ff86-172">بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك.</span><span class="sxs-lookup"><span data-stu-id="1ff86-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="1ff86-173">تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="1ff86-174">[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="1ff86-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="1ff86-175">عرض أداء مركز التكلفة باستخدام مساحة العمل المحمولة للتحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="1ff86-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="1ff86-176">على جهازك المحمول، حدد مساحة عمل **التحكم في التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="1ff86-177">حدد **التحكم في كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="1ff86-178">حدد **الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="1ff86-179">حدد **تحديد التكوين** لتحديد تخطيط التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="1ff86-180">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-180">Select **Done**.</span></span>
6.  <span data-ttu-id="1ff86-181">حدد **الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="1ff86-182">حدد **تحديد كائن التكلفة** لتحديد مراكز التكلفة التي تم منحك حق الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="1ff86-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="1ff86-183">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-183">Select **Done**.</span></span>
9.  <span data-ttu-id="1ff86-184">عرض الأداء الإجمالي لمركز التكلفة الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1ff86-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="1ff86-185">حدد الارتباط **تفاصيل للفترة الحالية**.</span><span class="sxs-lookup"><span data-stu-id="1ff86-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="1ff86-186">عرض أداء عناصر تكاليف الفردية.</span><span class="sxs-lookup"><span data-stu-id="1ff86-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="1ff86-187">يمكنك أيضا البحث عن عناصر تكلفة معينة.</span><span class="sxs-lookup"><span data-stu-id="1ff86-187">You can also search for specific cost elements.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]