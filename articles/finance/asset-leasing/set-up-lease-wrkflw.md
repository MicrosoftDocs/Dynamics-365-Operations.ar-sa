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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249571"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="1d173-103">إعداد سير عمل الموافقة على الإيجار</span><span class="sxs-lookup"><span data-stu-id="1d173-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d173-104">يوضح الموضوع كيفية إعداد سير عمل معتمدة سيتم تشغيله عند إنشاء عقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="1d173-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="1d173-105">للحصول على معلومات حول كيفية استخدام سير العمل، راجع [استخدام عمليات سير عمل معتمدة لعقد الإيجار](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="1d173-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="1d173-106">انتقل إلى **تأجير الأصول \> الضبط \> سير عمل عقود الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="1d173-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="1d173-107">في صفحة **سير عمل عقد الإيجار‬**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1d173-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="1d173-108">في مربع الحوار الذي يظهر، ضمن **نوع سير العمل**، حدد الارتباط **سير عمل الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="1d173-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="1d173-109">يتم فتح استمارة التقديم.</span><span class="sxs-lookup"><span data-stu-id="1d173-109">The application is opened.</span></span> <span data-ttu-id="1d173-110">بعد تشغيله، قم بتسجيل الدخول إلى Azure Active Directory (Azure AD) ليتم إعادة التوجيه إلى استمارة تقديم سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1d173-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="1d173-111">اسحب العنصر **اعتماد سير عمل عقد الإيجار** إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1d173-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="1d173-112">قم بتوصيل عقدة واحدة من **البدء** إلى **اعتماد سير عمل عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="1d173-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="1d173-113">قم بتوصيل **اعتماد سير عمل عقد الإيجار** إلى **النهاية**.</span><span class="sxs-lookup"><span data-stu-id="1d173-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="1d173-114">انقر نقرًا مزدوجًا فوق **اعتماد سير عمل عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="1d173-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="1d173-115">حدد **الخصائص**، ثم، ضمن **إعدادات الأساسية**، أدخل اسمًا لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="1d173-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="1d173-116">في هذه الصفحة، يمكنك أيضًا تعيين المزيد من المعلمات لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="1d173-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="1d173-117">إذا قمت بتشغيل **الإجراءات التلقائية**، سيقوم النظام تلقائيًا بتنفيذ إجراء معين.</span><span class="sxs-lookup"><span data-stu-id="1d173-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="1d173-118">يمكن إرسال الإخطارات إذا تم تحديدها في علامة التبويب **الإخطارات**. في علامة التبويب **إعدادات متقدمة**، ويمكنك تحديد معتمد نهائي وتعيين حد زمني وتعيين إجراءات معينة يجب إكمالها.</span><span class="sxs-lookup"><span data-stu-id="1d173-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="1d173-119">عند الانتهاء من إعداد معلمات سير العمل، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="1d173-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="1d173-120">حدد **الخطوة 1**، ثم حدد **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="1d173-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="1d173-121">ضمن **الإعدادات الأساسية**، أدخل اسمًا للخطوة، وقم بإنشاء بند موضوع للاعتماد، وحدد الإرشادات الخاصة بالاعتماد.</span><span class="sxs-lookup"><span data-stu-id="1d173-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="1d173-122">في الصفحة **مهمة**، حدد نوع المهمة.</span><span class="sxs-lookup"><span data-stu-id="1d173-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="1d173-123">لتعيين مستخدمين محددين للاعتماد، حدد **مستخدم**، ثم حدد المستخدمين الذين يوافقوا على عقود الإيجار، ثم حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="1d173-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="1d173-124">حدد **حفظ وإغلاق** لإنشاء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="1d173-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="1d173-125">ثم، عند المطالبة، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1d173-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="1d173-126">في صفحة **إنشاء سير عمل‬**، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="1d173-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="1d173-127">حدد سير العمل الجديد، ثم حدد **إصدارات**.</span><span class="sxs-lookup"><span data-stu-id="1d173-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="1d173-128">ثم حدد **تنشيط** لضمان أن سير العمل نشطًا.</span><span class="sxs-lookup"><span data-stu-id="1d173-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="1d173-129">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="1d173-129">Select **Close**.</span></span> <span data-ttu-id="1d173-130">يظهر الإصدار النشط الجديد.</span><span class="sxs-lookup"><span data-stu-id="1d173-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]