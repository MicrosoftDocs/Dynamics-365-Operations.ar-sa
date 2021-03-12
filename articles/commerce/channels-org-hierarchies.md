---
title: إعداد التدرجات الهرمية للمؤسسات
description: يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997765"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="d1cce-103">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d1cce-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d1cce-104">يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1cce-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d1cce-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d1cce-105">Overview</span></span>

<span data-ttu-id="d1cce-106">قبل إنشاء القنوات، يجب أن تتأكد من إعداد التدرجات الهرمية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="d1cce-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="d1cce-107">يمكنك استخدام التدرجات الهرمية المؤسسية لعرض عملك وإنشاء تقارير متعلقة به من منظورات متعددة.</span><span class="sxs-lookup"><span data-stu-id="d1cce-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="d1cce-108">على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية.</span><span class="sxs-lookup"><span data-stu-id="d1cce-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="d1cce-109">ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="d1cce-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="d1cce-110">قبل إنشاء تدرج هرمي للمؤسسات، يتعين عليك إنشاء مؤسسات.</span><span class="sxs-lookup"><span data-stu-id="d1cce-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="d1cce-111">لمزيد من المعلومات، راجع [إنشاء كيانات قانونية](channels-legal-entities.md) أو [إنشاء وحدات تشغيل](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d1cce-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="d1cce-112">لمزيد من المعلومات، راجع الموضوعات التالية.</span><span class="sxs-lookup"><span data-stu-id="d1cce-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="d1cce-113">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d1cce-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="d1cce-114">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d1cce-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="d1cce-115">إنشاء تدرج هرمي لمؤسسة</span><span class="sxs-lookup"><span data-stu-id="d1cce-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="d1cce-116">إنشاء تدرج هرمي مؤسسي</span><span class="sxs-lookup"><span data-stu-id="d1cce-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="d1cce-117">لإنشاء تدرج هرمي للمؤسسات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d1cce-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="d1cce-118">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> التدرجات الهرمية للمؤسسات**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="d1cce-119">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d1cce-120">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="d1cce-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="d1cce-121">في قسم **الغرض**، حدد **تعيين غرض‬**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="d1cce-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d1cce-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="d1cce-123">حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d1cce-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="d1cce-124">في قسم **التدرجات الهرمية المعينة‬**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="d1cce-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d1cce-125">In the list, mark the selected row.</span></span> <span data-ttu-id="d1cce-126">ابحث عن التدرج الهرمي الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="d1cce-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="d1cce-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-127">Select **OK**.</span></span>

<span data-ttu-id="d1cce-128">تعرض الصورة التالية مثالاً لتدرد هرمي للمؤسسات تم إنشاؤها لمجموعة متاجر "Adventure Works".</span><span class="sxs-lookup"><span data-stu-id="d1cce-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![مثال لتدرج هرمي للمؤسسات](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="d1cce-130">إضافة مؤسسات إلى تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="d1cce-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="d1cce-131">لإضافة مؤسسات إلى تدرج هرمي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d1cce-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="d1cce-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d1cce-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="d1cce-133">قم بتحديد التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="d1cce-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="d1cce-134">في جزء الإجراءات، حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="d1cce-135">قم بإضافة المؤسسات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d1cce-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="d1cce-136">لإضافة مؤسسة، حدد **تحرير** ثم حدد **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="d1cce-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="d1cce-137">عند الانتهاء من إجراء التغييرات، يمكنك حفظ مسودة ونشر التغييرات.</span><span class="sxs-lookup"><span data-stu-id="d1cce-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="d1cce-138">تعرض الصورة التالية كيانًا قانونيًا تمت إضافته إلى جذر التدرج الهرمي مع أربع مراكز تكلفة مضافة لقنوات "مركز التسوق" و "المنفذ" و "عبر الإنترنت" و "مركز الاتصال".</span><span class="sxs-lookup"><span data-stu-id="d1cce-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="d1cce-139">بعد ذلك، يمكن إضافة مركز اتصال وقنوات عبر الإنترنت لكل واحد منها.</span><span class="sxs-lookup"><span data-stu-id="d1cce-139">Various retail, call center and online channels can then be added to each.</span></span>

![مثال لمصمم التدرج الهرمي](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="d1cce-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d1cce-141">Additional resources</span></span>

[<span data-ttu-id="d1cce-142">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d1cce-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d1cce-143">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d1cce-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d1cce-144">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="d1cce-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="d1cce-145">إنشاء وحدات تشغيل</span><span class="sxs-lookup"><span data-stu-id="d1cce-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d1cce-146">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="d1cce-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d1cce-147">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="d1cce-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
