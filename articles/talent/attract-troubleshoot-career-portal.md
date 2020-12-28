---
title: لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل المهن
description: يشرح هذا الموضوع كيفية استكشاف مشكلة حيث يتعذر على مستخدمي Attract التقدم للوظائف من مدخل الوظائف.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460176"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="b6b32-103">لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل المهن</span><span class="sxs-lookup"><span data-stu-id="b6b32-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="b6b32-104">إصدار</span><span class="sxs-lookup"><span data-stu-id="b6b32-104">Issue</span></span>

<span data-ttu-id="b6b32-105">لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b6b32-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="b6b32-106">عندما يحاولون التقدم لوظيفة تم إنشاؤها في Dynamics 365 Talent: Attract، يقوم المتصفح بتحميل الصفحة بشكل مستمر ولا يكمل الإجراء.</span><span class="sxs-lookup"><span data-stu-id="b6b32-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="b6b32-107">السبب</span><span class="sxs-lookup"><span data-stu-id="b6b32-107">Cause</span></span>

<span data-ttu-id="b6b32-108">تحدث هذه المشكلة عندما لا يكون لفريق Talent Relationship دور مستخدم Talent.</span><span class="sxs-lookup"><span data-stu-id="b6b32-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="b6b32-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="b6b32-109">Resolution</span></span>

<span data-ttu-id="b6b32-110">قم بتعيين دور مستخدم Talent إلى فريق Talent Relationship.</span><span class="sxs-lookup"><span data-stu-id="b6b32-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="b6b32-111">سجل الدخول إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com) باستخدام أيٍّ من بيانات اعتماد المسؤول التالية:</span><span class="sxs-lookup"><span data-stu-id="b6b32-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="b6b32-112">إدارة Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b6b32-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="b6b32-113">مسؤول عمومي</span><span class="sxs-lookup"><span data-stu-id="b6b32-113">Global admin</span></span>
   - <span data-ttu-id="b6b32-114">مسؤول Power Platform</span><span class="sxs-lookup"><span data-stu-id="b6b32-114">Power Platform admin</span></span>

2. <span data-ttu-id="b6b32-115">في جزء التنقل، حدد **البيئات**، ثم حدد البيئة التي يتم فيها تعيين دور مستخدم Talent إلى فريق Talent Relationship.</span><span class="sxs-lookup"><span data-stu-id="b6b32-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![تحديد بيئة](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="b6b32-117">في جزء **البيئات**، حدد **عنوان URL للبيئة** وقم بتسجيل الدخول إلى مدخل مسؤول البيئة (على سبيل المثال، https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="b6b32-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="b6b32-118">حدد **الإعدادات**، وحدد **النظام**، ثم حدد **الأمان**.</span><span class="sxs-lookup"><span data-stu-id="b6b32-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![الانتقال إلى الأمان](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="b6b32-120">حدد **Teams**.</span><span class="sxs-lookup"><span data-stu-id="b6b32-120">Select **Teams**.</span></span>

   ![تحديد Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="b6b32-122">ابحث عن **فريق Talent Relationship** في مربع البحث، ثم حدد الفريق من نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="b6b32-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="b6b32-123">حدد **إدارة الأدوار** من الشريط.</span><span class="sxs-lookup"><span data-stu-id="b6b32-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="b6b32-124">في مربع الحوار **إدارة أدوار الفريق**، حدد **مستخدم Talent** من قائمة الأدوار المتاحة، ثم حدد **موافق** لتطبيق الدور.</span><span class="sxs-lookup"><span data-stu-id="b6b32-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![تطبيق الدور](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="b6b32-126">اختبر تغييراتك:</span><span class="sxs-lookup"><span data-stu-id="b6b32-126">Test your changes:</span></span>

   1. <span data-ttu-id="b6b32-127">قم بتسجيل الدخول إلى مدخل الوظائف من نافذة مستعرض جديدة.</span><span class="sxs-lookup"><span data-stu-id="b6b32-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="b6b32-128">تقدم للوظيفة من مدخل الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b6b32-128">Apply for the job from the career portal.</span></span> 