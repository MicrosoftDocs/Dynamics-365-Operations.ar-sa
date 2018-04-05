---
title: "تحديد حقوق الوصول لمراقبي كائن التكلفة"
description: "يوفر هذا الموضوع معلومات حول حقوق الوصول لمراقبي كائن التكلفة."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6403aabb6b029807b42ab1ccb11756dcb0dda5dc
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="a08a5-103">حقوق الوصول لمراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a08a5-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a08a5-104">مساحة العمل **مراقبة التكلفة** هي نقطة مركزية يمكن للمديرين فيها عرض أداء كائنات التكلفة الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="a08a5-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="a08a5-105">تسمح مساحة العمل هذه للمديرين باستهلاك بيانات محاسبة التكاليف على الرغم من أنهم ليسوا محاسبي التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a08a5-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="a08a5-106">ولأسباب أمنية، يجب السماح للمديرين بمشاهدة بيانات محاسبة التكاليف المرتبطة بكائنات التكاليف المحددة الذين يتحملون مسؤوليتها فقط.</span><span class="sxs-lookup"><span data-stu-id="a08a5-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="a08a5-107">توجد أربعة أدوار فريدة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a08a5-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="a08a5-108">اسم الدور</span><span class="sxs-lookup"><span data-stu-id="a08a5-108">Role name</span></span>               | <span data-ttu-id="a08a5-109">الترخيص</span><span class="sxs-lookup"><span data-stu-id="a08a5-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="a08a5-110">مدير محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="a08a5-110">Cost accounting manager</span></span> | <span data-ttu-id="a08a5-111">النشاط</span><span class="sxs-lookup"><span data-stu-id="a08a5-111">Activity</span></span>     |
| <span data-ttu-id="a08a5-112">محاسب التكاليف</span><span class="sxs-lookup"><span data-stu-id="a08a5-112">Cost accountant</span></span>         | <span data-ttu-id="a08a5-113">Operations</span><span class="sxs-lookup"><span data-stu-id="a08a5-113">Operations</span></span>   |
| <span data-ttu-id="a08a5-114">موظف حساب التكلفة</span><span class="sxs-lookup"><span data-stu-id="a08a5-114">Cost accountant clerk</span></span>   | <span data-ttu-id="a08a5-115">Operations</span><span class="sxs-lookup"><span data-stu-id="a08a5-115">Operations</span></span>   |
| <span data-ttu-id="a08a5-116">مراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a08a5-116">Cost object controller</span></span>  | <span data-ttu-id="a08a5-117">أعضاء الفريق</span><span class="sxs-lookup"><span data-stu-id="a08a5-117">Team members</span></span> |

<span data-ttu-id="a08a5-118">يشرح هذا المقال كيفية تعيين دور **مراقب كائن التكلفة** لأحد المديرين.</span><span class="sxs-lookup"><span data-stu-id="a08a5-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="a08a5-119">عند تعيين دور **مراقب كائن التكلفة** للمدير، فمن ثم يمكن للمدير تنفيذ المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="a08a5-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="a08a5-120">الوصول إلى مساحة عمل **مراقبة التكاليف** (في العميل).</span><span class="sxs-lookup"><span data-stu-id="a08a5-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="a08a5-121">التصفح وأن يكون لديه صلاحية عرض الوصول إلى الصفحات التي تدعم خاصية/خبرة التصفح.</span><span class="sxs-lookup"><span data-stu-id="a08a5-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="a08a5-122">الوصول إلى مساحة عمل **مراقبة التكاليف** (في تطبيق الجوال).</span><span class="sxs-lookup"><span data-stu-id="a08a5-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="a08a5-123">لا يتحكم دور **مراقبة كائن التكلفة** في أي كائنات تكلفة يمكن للمستخدم الوصول إليها وعرض بياناتها.</span><span class="sxs-lookup"><span data-stu-id="a08a5-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="a08a5-124">يتم توفير أمان على مستوى الصف من خلال التسلسلات الهرمية للأبعاد والتسلسل الهرمي لقائمة الوصول.</span><span class="sxs-lookup"><span data-stu-id="a08a5-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="a08a5-125">منح حقوق الوصول</span><span class="sxs-lookup"><span data-stu-id="a08a5-125">Grant access rights</span></span>
<span data-ttu-id="a08a5-126">يوضح المثال التالي شكل وهيئة التدرج الهرمي للأبعاد.</span><span class="sxs-lookup"><span data-stu-id="a08a5-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="a08a5-127">**تفاصيل التدرج الهرمي للبعد**</span><span class="sxs-lookup"><span data-stu-id="a08a5-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="a08a5-128">اسم التدرج الهرمي للبُعد</span><span class="sxs-lookup"><span data-stu-id="a08a5-128">Dimension hierarchy name</span></span> | <span data-ttu-id="a08a5-129">البعد</span><span class="sxs-lookup"><span data-stu-id="a08a5-129">Dimension</span></span>    | <span data-ttu-id="a08a5-130">اسم نوع التدرج الهرمي للبُعد</span><span class="sxs-lookup"><span data-stu-id="a08a5-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="a08a5-131">التدرج الهرمي لقائمة الوصول</span><span class="sxs-lookup"><span data-stu-id="a08a5-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="a08a5-132">المؤسسة</span><span class="sxs-lookup"><span data-stu-id="a08a5-132">Organization</span></span>             | <span data-ttu-id="a08a5-133">مراكز تكلفة</span><span class="sxs-lookup"><span data-stu-id="a08a5-133">Cost centers</span></span> | <span data-ttu-id="a08a5-134">التدرج الهرمي لتصنيف الأبعاد</span><span class="sxs-lookup"><span data-stu-id="a08a5-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="a08a5-135">**نعم**</span><span class="sxs-lookup"><span data-stu-id="a08a5-135">**Yes**</span></span>               |

<span data-ttu-id="a08a5-136">يمكنك استخدام علامة التبويب السريعة **المستخدمون** الموجودة في مصمم التدرج الهرمي لإدراج معرف مستخدم واحد أو أكثر في كل عقده.</span><span class="sxs-lookup"><span data-stu-id="a08a5-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="a08a5-137">المستخدمون</span><span class="sxs-lookup"><span data-stu-id="a08a5-137">Users</span></span>            | <span data-ttu-id="a08a5-138">نطاقات أعضاء البُعد</span><span class="sxs-lookup"><span data-stu-id="a08a5-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="a08a5-139">**العُقد**</span><span class="sxs-lookup"><span data-stu-id="a08a5-139">**Nodes**</span></span>                         | <span data-ttu-id="a08a5-140">**معرف المستخدم**</span><span class="sxs-lookup"><span data-stu-id="a08a5-140">**User ID**</span></span>      | <span data-ttu-id="a08a5-141">**من عضو البعد**</span><span class="sxs-lookup"><span data-stu-id="a08a5-141">**From dimension member**</span></span> | <span data-ttu-id="a08a5-142">**إلى عضو البُعد**</span><span class="sxs-lookup"><span data-stu-id="a08a5-142">**To dimension member**</span></span> |
| <span data-ttu-id="a08a5-143">المؤسسة</span><span class="sxs-lookup"><span data-stu-id="a08a5-143">Organization</span></span>                      | <span data-ttu-id="a08a5-144">بنجامين، كلير</span><span class="sxs-lookup"><span data-stu-id="a08a5-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="a08a5-145">&nbsp;&nbsp;المسؤول</span><span class="sxs-lookup"><span data-stu-id="a08a5-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="a08a5-146">أبريل</span><span class="sxs-lookup"><span data-stu-id="a08a5-146">April</span></span>            |                           |                         |
| <span data-ttu-id="a08a5-147">&nbsp;&nbsp;&nbsp;&nbsp;المالية</span><span class="sxs-lookup"><span data-stu-id="a08a5-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="a08a5-148">أليسيا</span><span class="sxs-lookup"><span data-stu-id="a08a5-148">Alicia</span></span>           | <span data-ttu-id="a08a5-149">CC002</span><span class="sxs-lookup"><span data-stu-id="a08a5-149">CC002</span></span>                     | <span data-ttu-id="a08a5-150">CC003</span><span class="sxs-lookup"><span data-stu-id="a08a5-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="a08a5-151">CC007</span><span class="sxs-lookup"><span data-stu-id="a08a5-151">CC007</span></span>                     | <span data-ttu-id="a08a5-152">CC007</span><span class="sxs-lookup"><span data-stu-id="a08a5-152">CC007</span></span>                   |
| <span data-ttu-id="a08a5-153">&nbsp;&nbsp;&nbsp;&nbsp;الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a08a5-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="a08a5-154">أرني</span><span class="sxs-lookup"><span data-stu-id="a08a5-154">Arnie</span></span>            | <span data-ttu-id="a08a5-155">CC001</span><span class="sxs-lookup"><span data-stu-id="a08a5-155">CC001</span></span>                     | <span data-ttu-id="a08a5-156">CC001</span><span class="sxs-lookup"><span data-stu-id="a08a5-156">CC001</span></span>                   |
| <span data-ttu-id="a08a5-157">&nbsp;&nbsp;الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a08a5-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="a08a5-158">ديفيد</span><span class="sxs-lookup"><span data-stu-id="a08a5-158">David</span></span>            |                           |                         |
| <span data-ttu-id="a08a5-159">&nbsp;&nbsp;&nbsp;&nbsp;التعبئة</span><span class="sxs-lookup"><span data-stu-id="a08a5-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="a08a5-160">الين</span><span class="sxs-lookup"><span data-stu-id="a08a5-160">Ellen</span></span>            | <span data-ttu-id="a08a5-161">CC005</span><span class="sxs-lookup"><span data-stu-id="a08a5-161">CC005</span></span>                     | <span data-ttu-id="a08a5-162">CC005</span><span class="sxs-lookup"><span data-stu-id="a08a5-162">CC005</span></span>                   |
| <span data-ttu-id="a08a5-163">&nbsp;&nbsp;&nbsp;&nbsp;التجميع</span><span class="sxs-lookup"><span data-stu-id="a08a5-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="a08a5-164">كريس</span><span class="sxs-lookup"><span data-stu-id="a08a5-164">Chris</span></span>            | <span data-ttu-id="a08a5-165">CC006</span><span class="sxs-lookup"><span data-stu-id="a08a5-165">CC006</span></span>                     | <span data-ttu-id="a08a5-166">CC006</span><span class="sxs-lookup"><span data-stu-id="a08a5-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="a08a5-167">ينبغي تعيين محاسبي التكلفة إلى أعلى مستوى من التسلسل الهرمي، حتى يتمكنوا من رؤية جميع الإدخالات في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a08a5-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="a08a5-168">قبل تطبيق التدرج الهرمي لقائمة الوصول وإعدادات الأمان الخاصة به، يجب أولًا تعيين خيار **تمكين عرض الوصول لأعضاء أبعاد كائنات التكلفة** إلى **نعم** الموجود في علامة تبويب **عام** في صفحة **محددات محاسبة التكاليف** (**محاسبة التكاليف** > **الإعداد** > **المحددات**).</span><span class="sxs-lookup"><span data-stu-id="a08a5-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="a08a5-169">يتم استخدام الإعدادات الخاصة بالتدرج الهرمي لقائمة الوصول للتحكم في البيانات التي يتم عرضها في المناطق التالية:</span><span class="sxs-lookup"><span data-stu-id="a08a5-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="a08a5-170">مساحة عمل **مراقب التكلفة** (في العميل):</span><span class="sxs-lookup"><span data-stu-id="a08a5-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="a08a5-171">البيانات الموجودة في الصفحة التي يتم استخدامها للتصفح</span><span class="sxs-lookup"><span data-stu-id="a08a5-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="a08a5-172">مساحة عمل **مراقبة التكاليف** (في تطبيق الجوال):</span><span class="sxs-lookup"><span data-stu-id="a08a5-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="a08a5-173">الأرصدة في بطاقات</span><span class="sxs-lookup"><span data-stu-id="a08a5-173">Balances in cards</span></span>

- <span data-ttu-id="a08a5-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="a08a5-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="a08a5-175">البيانات المعروضة في الرسوم المرئية لـ Power BI</span><span class="sxs-lookup"><span data-stu-id="a08a5-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="a08a5-176">بيانات الرسوم المرئية لـ Power BI المضمنة في Microsoft Dynamics 365 for Finance and Operations، عميل</span><span class="sxs-lookup"><span data-stu-id="a08a5-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="a08a5-177">قبل أن يؤثر التدرج الهرمي لقائمة الوصول على البيانات في Power BI، يجب أن يتم إقران التدرج الهرمي لقائمة الوصول والأمان على مستوى الصف في Power BI.</span><span class="sxs-lookup"><span data-stu-id="a08a5-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="a08a5-178">للحصول على مزيد من المعلومات، راجع [إعداد الأمان لحزمة محتوى محاسبة التكاليف](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a08a5-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="a08a5-179">يوضح هذا الموضوع المتطلبات الأساسية التي يجب توافرها قبل أن تتمكن من استخدام مساحة عمل **مراقب التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="a08a5-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="a08a5-180">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="a08a5-180">See also</span></span>

- [<span data-ttu-id="a08a5-181">مساحة عمل مراقبة التكلفة</span><span class="sxs-lookup"><span data-stu-id="a08a5-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="a08a5-182">التدرج الهرمي للأبعاد</span><span class="sxs-lookup"><span data-stu-id="a08a5-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="a08a5-183">إعداد الأمان لحزمة محتوى محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="a08a5-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

