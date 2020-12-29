---
title: إعداد سير عمل الموافقة على الإيجار
description: يوضح الموضوع كيفية إعداد سير عمل معتمدة سيتم تشغيله عند إنشاء عقد إيجار جديد.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440136"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="ff7a0-103">إعداد سير عمل الموافقة على الإيجار</span><span class="sxs-lookup"><span data-stu-id="ff7a0-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff7a0-104">يوضح الموضوع كيفية إعداد سير عمل معتمدة سيتم تشغيله عند إنشاء عقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="ff7a0-105">للحصول على معلومات حول كيفية استخدام سير العمل، راجع [استخدام عمليات سير عمل معتمدة لعقد الإيجار](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="ff7a0-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="ff7a0-106">انتقل إلى **تأجير الأصول \> الضبط \> سير عمل عقود الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="ff7a0-107">في صفحة **سير عمل عقد الإيجار‬**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="ff7a0-108">في مربع الحوار الذي يظهر، ضمن **نوع سير العمل**، حدد الارتباط **سير عمل الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="ff7a0-109">يتم فتح استمارة التقديم.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-109">The application is opened.</span></span> <span data-ttu-id="ff7a0-110">بعد تشغيله، قم بتسجيل الدخول إلى Azure Active Directory (Azure AD) ليتم إعادة التوجيه إلى استمارة تقديم سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="ff7a0-111">اسحب العنصر **اعتماد سير عمل عقد الإيجار** إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="ff7a0-112">قم بتوصيل عقدة واحدة من **البدء** إلى **اعتماد سير عمل عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="ff7a0-113">قم بتوصيل **اعتماد سير عمل عقد الإيجار** إلى **النهاية**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="ff7a0-114">انقر نقرًا مزدوجًا فوق **اعتماد سير عمل عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="ff7a0-115">حدد **الخصائص**، ثم، ضمن **إعدادات الأساسية**، أدخل اسمًا لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="ff7a0-116">في هذه الصفحة، يمكنك أيضًا تعيين المزيد من المعلمات لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="ff7a0-117">إذا قمت بتشغيل **الإجراءات التلقائية**، سيقوم النظام تلقائيًا بتنفيذ إجراء معين.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="ff7a0-118">يمكن إرسال الإخطارات إذا تم تحديدها في علامة التبويب **الإخطارات**. في علامة التبويب **إعدادات متقدمة**، ويمكنك تحديد معتمد نهائي وتعيين حد زمني وتعيين إجراءات معينة يجب إكمالها.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="ff7a0-119">عند الانتهاء من إعداد معلمات سير العمل، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="ff7a0-120">حدد **الخطوة 1**، ثم حدد **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="ff7a0-121">ضمن **الإعدادات الأساسية**، أدخل اسمًا للخطوة، وقم بإنشاء بند موضوع للاعتماد، وحدد الإرشادات الخاصة بالاعتماد.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="ff7a0-122">في الصفحة **مهمة**، حدد نوع المهمة.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="ff7a0-123">لتعيين مستخدمين محددين للاعتماد، حدد **مستخدم**، ثم حدد المستخدمين الذين يوافقوا على عقود الإيجار، ثم حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="ff7a0-124">حدد **حفظ وإغلاق** لإنشاء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="ff7a0-125">ثم، عند المطالبة، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="ff7a0-126">في صفحة **إنشاء سير عمل‬**، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="ff7a0-127">حدد سير العمل الجديد، ثم حدد **إصدارات**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="ff7a0-128">ثم حدد **تنشيط** لضمان أن سير العمل نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="ff7a0-129">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-129">Select **Close**.</span></span> <span data-ttu-id="ff7a0-130">يظهر الإصدار النشط الجديد.</span><span class="sxs-lookup"><span data-stu-id="ff7a0-130">The new active version appears.</span></span>
