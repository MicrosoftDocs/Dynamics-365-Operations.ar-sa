---
title: عمليات سير عمل صفقات إدارة الخصومات
description: يشرح هذا الموضوع كيفية إعداد سير عمل صفقة إدارة الخصم للموافقة على الصفقات وتنشيطها.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 37b8022633e61c4d98d6f5d129bcf494a9ed92e0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831712"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="90368-103">عمليات سير عمل صفقات إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="90368-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="90368-104">للموافقة على صفقات الخصم، تستخدم إدارة الخصم نفس نظام سير العمل الأساسي مثل تطبيقات Finance and Operations الأخرى.</span><span class="sxs-lookup"><span data-stu-id="90368-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="90368-105">كما يتم اقران عمليتي وظيفة بكل سير عمل:</span><span class="sxs-lookup"><span data-stu-id="90368-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="90368-106">يقوم أحد عناصر سير العمل بتنشيط الصفقة بحيث يمكن للمستخدم أو عمليه سير العمل اعتماد الحركات.</span><span class="sxs-lookup"><span data-stu-id="90368-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="90368-107">يقوم أحد عناصر سير العمل باعتماد الصفقة.</span><span class="sxs-lookup"><span data-stu-id="90368-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="90368-108">قبل ان تتمكن من استخدام صفقة خصم، يجب ان تكون نشطه في وحدة **إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="90368-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="90368-109">لتنشيط صفقة، يجب أولا إنشاء وتكوين *سير عمل لصفقة إدارة الخصومات*.</span><span class="sxs-lookup"><span data-stu-id="90368-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="90368-110">وبعد تنشيط سير العمل لأداره الخصم، لا يمكن للمستخدمين اعتماد الصفقات يدويا.</span><span class="sxs-lookup"><span data-stu-id="90368-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="90368-111">يجب استخدام سير العمل دائما.</span><span class="sxs-lookup"><span data-stu-id="90368-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="90368-112">إنشاء وإدارة عمليات سير عمل صفقات إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="90368-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="90368-113">للعمل مع مهام سير عمل صفقة إدارة الخصم، انتقل إلى **إدارة الخصومات \> الإعداد \> عمليات سير عمل إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="90368-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="90368-114">هناك، يمكنك عرض مهام سير العمل وإنشاءها وتحديثها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="90368-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="90368-115">يمكن أن يكون سير عمل واحد فقط من هذا النوع نشطًا في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="90368-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="90368-116">لمزيد من المعلومات حول مهام سير العمل، وكيفيه العمل مع صفحة **مهام سير عمل إدارة الخصومات**، وكيفية إنشاء مهام سير العمل، راجع [نظرة عامة على سير العمل](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ومواضيعها ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="90368-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="90368-117">استخدام سير عمل لتنشيط صفقة</span><span class="sxs-lookup"><span data-stu-id="90368-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="90368-118">لتنشيط أحدي الصفقات من خلال سير العمل، افتح الصفقة (علي سبيل المثال، في صفحة **كل صفقات إدارة الخصومات**).</span><span class="sxs-lookup"><span data-stu-id="90368-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="90368-119">ثم في جزء الإجراء، حدد **سير العمل \> إرسال**.</span><span class="sxs-lookup"><span data-stu-id="90368-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="90368-120">بعد معالجه الصفقة الجديدة واعتمادها من خلال سير العمل، ستكون نشطه وجاهزه للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="90368-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="90368-121">وبعد تنشيط أحدي الصفقات، لا يمكنك تغيير الاعداد الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="90368-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="90368-122">إذا كان من الضروري تغيير أحدي الصفقات النشطة، قم بإلغاء تنشيطها، ثم قم بإنشاء صفقة جديده.</span><span class="sxs-lookup"><span data-stu-id="90368-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="90368-123">إذا كانت الصفقة الجديدة تشبه الصفقة القديمة، فيمكنك إنشاؤها عن طريق نسخ الصفقة القديمة.</span><span class="sxs-lookup"><span data-stu-id="90368-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
