---
title: عرض الأوامر المخططة وإدارتها والموافقة عليها
description: يوفر هذا الموضوع معلومات حول كيفية عرض الأوامر المخططة وإدارتها والموافقة عليها في "تحسين التخطيط".
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304357"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="8e22d-103">عرض الأوامر المخططة وإدارتها والموافقة عليها</span><span class="sxs-lookup"><span data-stu-id="8e22d-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e22d-104">يوفر هذا الموضوع معلومات حول كيفية عرض الأوامر المخططة وإدارتها والموافقة عليها في "تحسين التخطيط".</span><span class="sxs-lookup"><span data-stu-id="8e22d-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="8e22d-105">عرض وإدارة الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-105">View and manage planned orders</span></span>

<span data-ttu-id="8e22d-106">يمكنك عرض وإدارة الأوامر المخططة في أي صفحة قائمة الأوامر المخططة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="8e22d-107">انتقل إلى أحد الأماكن التالية، بناءً على نوع الأوامر المخططة التي تريد العمل بها:</span><span class="sxs-lookup"><span data-stu-id="8e22d-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="8e22d-108">التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="8e22d-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="8e22d-109">التخطيط الرئيسي \> التخطيط الرئيسي \> الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="8e22d-110">التحكم بالإنتاج‬ \> أوامر الإنتاج \> أوامر الإنتاج المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="8e22d-111">التدبير وتحديد الموارد \> أوامر الشراء \> أوامر الشراء المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="8e22d-112">إدارة المخزون \> الأوامر الواردة \> التحويلات المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="8e22d-113">إدارة المخزون \> الأوامر الصادرة \> التحويلات المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="8e22d-114">عرض وتحرير حالة الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="8e22d-115">يمكنك استخدام حقل **الحالة** لكل أمر مخطط للمساعدة في تتبع التقدم أو تغيير كيفية معالجة الأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="8e22d-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="8e22d-116">تتوفر قيم **الحالة** التالية:</span><span class="sxs-lookup"><span data-stu-id="8e22d-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="8e22d-117">**غير معالجة** – عندما ينشئ التخطيط الرئيسي أوامر مخططة، يتم منحها هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="8e22d-118">سيتم حذف الأوامر المخططة التي لها هذه الحالة أثناء تشغيل التخطيط التالي.</span><span class="sxs-lookup"><span data-stu-id="8e22d-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="8e22d-119">**مكتمل** – تشير هذه الحالة إلى انه تم إكمال الأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="8e22d-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="8e22d-120">إذا قررت عدم تأكيد أمر مخطط، فيمكنك تغيير حالته يدويًا إلى *مكتمل*.</span><span class="sxs-lookup"><span data-stu-id="8e22d-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="8e22d-121">لاحظ أن النظام يتعامل مع حالات *غير معالج* و *مكتمل* بنفس الطريقة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="8e22d-122">**معتمد** - تشير هذه الحالة إلى انه تمت الموافقة علي الأمر المخطط للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="8e22d-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="8e22d-123">إذا كنت ترغب في تأكيد أمر مخطط، يُمكنك تغيير الحالة إلى *موافق عليه*.</span><span class="sxs-lookup"><span data-stu-id="8e22d-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="8e22d-124">إذا كنت ترغب في الاحتفاظ بعمليات التحرير التي تم اجراؤها علي أمر مخطط، أو إذا كنت تخطط لتاكيد أمر مخطط، فقم بتغيير حالته إلى *موافق عليه*.</span><span class="sxs-lookup"><span data-stu-id="8e22d-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="8e22d-125">تعتبر الأوامر المخططة التي تكون حالتها *موافق عليه* ثابتة والتوريد المتوقع بواسطة التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8e22d-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="8e22d-126">لذلك، لا يتم تعديلها أو حذفها أثناء عمليات التخطيط الرئيسية اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="8e22d-127">لتحقيق هذا السلوك، يقوم منطق التخطيط بنسخ الأوامر المخططة التي لها حالة *موافق عليه* من إصدار الخطة القديمة إلى إصدار الخطة الجديدة أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8e22d-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="8e22d-128">لاحظ أن الأوامر المخططة التي لها حالة *موافق عليه* تعتبر توريد فقط ضمن الخطة الرئيسية المحددة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="8e22d-129">لتغيير حالة أمر واحد مخطط، [افتح أي صفحة قائمة أوامر مخططة](#view-planned-orders)، افتح الأمر، ثم اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8e22d-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="8e22d-130">في علامة التبويب السريع **عام**، قم بتغيير قيمة حقل **الحالة**.</span><span class="sxs-lookup"><span data-stu-id="8e22d-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="8e22d-131">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **الأمر المخطط**، في مجموعة **العملية**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="8e22d-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="8e22d-132">في جزء الإجراءات، حدد **موافقة‬** لتمييز الأمر كموافق عليه.</span><span class="sxs-lookup"><span data-stu-id="8e22d-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="8e22d-133">لتغيير حالة عدة أوامر مخططة في نفس الوقت، [افتح أي صفحة قائمة أوامر مخططة](#view-planned-orders)، حدد خانة الاختيار لكل طلب تريد تغييره، ثم اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8e22d-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="8e22d-134">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **الأمر المخطط**، في مجموعة **العملية**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="8e22d-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="8e22d-135">في جزء الإجراءات، حدد **موافقة‬** لتمييز الأوامر كموافق عليه.</span><span class="sxs-lookup"><span data-stu-id="8e22d-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="8e22d-136">الموافقة على الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-136">Approve planned orders</span></span>

<span data-ttu-id="8e22d-137">تعتبر الموافقة على الأوامر المخططة خطوة اختيارية في عملية إنشاء أمر مؤكد من أمر مخطط.</span><span class="sxs-lookup"><span data-stu-id="8e22d-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="8e22d-138">يوضح الرسم التوضيحي التالي كيف يمكنك استخدام قيمة **الحالة** التي تم تعيينها لكل أمر مخطط لتنفيذ سير عمل الموافقة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="8e22d-139">لتنفيذ عملية الموافقة، قم بضبط قيمة **الحالة** لكل أمر مخطط كما هو موضح في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="8e22d-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![سير مهام الأمر المخطط](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="8e22d-141">نوصي بالموافقة على أي أوامر مخططة معدلة.</span><span class="sxs-lookup"><span data-stu-id="8e22d-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="8e22d-142">بخلاف ذلك، سيتم تجاهل عمليات التحرير والكتابة فوقها من خلال تشغيل التخطيط التالي.</span><span class="sxs-lookup"><span data-stu-id="8e22d-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e22d-143">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8e22d-143">Additional resources</span></span>

- [<span data-ttu-id="8e22d-144">تأكيد أوامر مخططة</span><span class="sxs-lookup"><span data-stu-id="8e22d-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
