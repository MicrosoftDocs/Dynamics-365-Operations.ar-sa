---
title: عمليات سير عمل صفقات إدارة الخصومات
description: يشرح هذا الموضوع كيفية إعداد سير عمل صفقة إدارة الخصم للموافقة على الصفقات وتنشيطها.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270947"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="fee9f-103">عمليات سير عمل صفقات إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="fee9f-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fee9f-104">للموافقة على صفقات الخصم، تستخدم إدارة الخصم نفس نظام سير العمل الأساسي مثل تطبيقات Finance and Operations الأخرى.</span><span class="sxs-lookup"><span data-stu-id="fee9f-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="fee9f-105">كما يتم اقران عمليتي وظيفة بكل سير عمل:</span><span class="sxs-lookup"><span data-stu-id="fee9f-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="fee9f-106">يقوم أحد عناصر سير العمل باعتماد الصفقة.</span><span class="sxs-lookup"><span data-stu-id="fee9f-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="fee9f-107">يقوم أحد عناصر سير العمل بتنشيط الصفقة بحيث يمكن للمستخدم أو عمليه سير العمل اعتماد الحركات.</span><span class="sxs-lookup"><span data-stu-id="fee9f-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="fee9f-108">قبل ان تتمكن من استخدام صفقة خصم، يجب ان تكون نشطه في وحدة **إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="fee9f-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="fee9f-109">لتنشيط صفقة، يجب أولا إنشاء وتكوين *سير عمل لصفقة إدارة الخصومات*.</span><span class="sxs-lookup"><span data-stu-id="fee9f-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="fee9f-110">لا يمكن للمستخدمين الموافقة يدويًا على الصفقات.</span><span class="sxs-lookup"><span data-stu-id="fee9f-110">Users can't manually approve deals.</span></span> <span data-ttu-id="fee9f-111">يجب استخدام سير العمل دائمًا.</span><span class="sxs-lookup"><span data-stu-id="fee9f-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="fee9f-112">إنشاء وإدارة عمليات سير عمل صفقات إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="fee9f-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="fee9f-113">للعمل مع مهام سير عمل صفقة إدارة الخصم، انتقل إلى **إدارة الخصومات \> الإعداد \> عمليات سير عمل إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="fee9f-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="fee9f-114">هناك، يمكنك عرض مهام سير العمل وإنشاءها وتحديثها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="fee9f-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="fee9f-115">يمكن أن يكون سير عمل واحد فقط من هذا النوع نشطًا في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="fee9f-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="fee9f-116">لمزيد من المعلومات حول مهام سير العمل، وكيفيه العمل مع صفحة **مهام سير عمل إدارة الخصومات**، وكيفية إنشاء مهام سير العمل، راجع [نظرة عامة على سير العمل](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ومواضيعها ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="fee9f-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="fee9f-117">استخدام سير عمل لتنشيط صفقة</span><span class="sxs-lookup"><span data-stu-id="fee9f-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="fee9f-118">لتنشيط أحدي الصفقات من خلال سير العمل، افتح الصفقة (علي سبيل المثال، في صفحة **كل صفقات إدارة الخصومات**).</span><span class="sxs-lookup"><span data-stu-id="fee9f-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="fee9f-119">ثم في جزء الإجراء، حدد **سير العمل \> إرسال**.</span><span class="sxs-lookup"><span data-stu-id="fee9f-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="fee9f-120">بعد معالجه الصفقة الجديدة واعتمادها من خلال سير العمل، ستكون نشطه وجاهزه للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="fee9f-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="fee9f-121">وبعد تنشيط إحدى الصفقات، لا يمكنك تغيير معظم الإعدادات الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="fee9f-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="fee9f-122">إذا كان من الضروري تغيير إحدى الصفقات النشطة، قم بإلغاء تنشيطها أولاً، ثم قم بإنشاء صفقة جديدة.</span><span class="sxs-lookup"><span data-stu-id="fee9f-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="fee9f-123">إذا كانت الصفقة الجديدة تشبه الصفقة القديمة، فيمكنك إنشاؤها عن طريق نسخ الصفقة القديمة.</span><span class="sxs-lookup"><span data-stu-id="fee9f-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="fee9f-124">يمكنك تغيير الإعدادات التالية لصفقة بعد تنشيطها:</span><span class="sxs-lookup"><span data-stu-id="fee9f-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="fee9f-125">تسوية حسب</span><span class="sxs-lookup"><span data-stu-id="fee9f-125">Reconcile by</span></span>
- <span data-ttu-id="fee9f-126">الضمان التراكمي</span><span class="sxs-lookup"><span data-stu-id="fee9f-126">Cumulative guarantee</span></span>
- <span data-ttu-id="fee9f-127">ملف تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="fee9f-127">Posting profile</span></span>
- <span data-ttu-id="fee9f-128">ملف تعريف الترحيل لضمان</span><span class="sxs-lookup"><span data-stu-id="fee9f-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="fee9f-129">ملاحظات المستندات</span><span class="sxs-lookup"><span data-stu-id="fee9f-129">Document notes</span></span>
- <span data-ttu-id="fee9f-130">عملة</span><span class="sxs-lookup"><span data-stu-id="fee9f-130">Currency</span></span>
- <span data-ttu-id="fee9f-131">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="fee9f-131">From date</span></span>
- <span data-ttu-id="fee9f-132">تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="fee9f-132">To date</span></span>

<span data-ttu-id="fee9f-133">بالإضافة إلى ذلك، يمكن إزالة بنود الخصم.</span><span class="sxs-lookup"><span data-stu-id="fee9f-133">In addition, rebate lines can be removed.</span></span>
