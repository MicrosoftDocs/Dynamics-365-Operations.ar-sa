---
title: إعداد التدرجات الهرمية للمؤسسات
description: يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800557"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="c70e7-103">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c70e7-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c70e7-104">يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c70e7-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c70e7-105">قبل إنشاء القنوات، يجب أن تتأكد من إعداد التدرجات الهرمية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c70e7-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="c70e7-106">يمكنك استخدام التدرجات الهرمية المؤسسية لعرض عملك وإنشاء تقارير متعلقة به من منظورات متعددة.</span><span class="sxs-lookup"><span data-stu-id="c70e7-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="c70e7-107">على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية.</span><span class="sxs-lookup"><span data-stu-id="c70e7-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="c70e7-108">ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="c70e7-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="c70e7-109">قبل إنشاء تدرج هرمي للمؤسسات، يتعين عليك إنشاء مؤسسات.</span><span class="sxs-lookup"><span data-stu-id="c70e7-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="c70e7-110">لمزيد من المعلومات، راجع [إنشاء كيانات قانونية](channels-legal-entities.md) أو [إنشاء وحدات تشغيل](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c70e7-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="c70e7-111">لمزيد من المعلومات، راجع الموضوعات التالية.</span><span class="sxs-lookup"><span data-stu-id="c70e7-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="c70e7-112">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c70e7-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c70e7-113">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c70e7-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c70e7-114">إنشاء تدرج هرمي لمؤسسة</span><span class="sxs-lookup"><span data-stu-id="c70e7-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="c70e7-115">إنشاء تدرج هرمي مؤسسي</span><span class="sxs-lookup"><span data-stu-id="c70e7-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="c70e7-116">لإنشاء تدرج هرمي للمؤسسات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c70e7-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c70e7-117">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> التدرجات الهرمية للمؤسسات**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="c70e7-118">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c70e7-119">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="c70e7-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c70e7-120">في قسم **الغرض**، حدد **تعيين غرض‬**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="c70e7-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c70e7-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="c70e7-122">حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c70e7-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="c70e7-123">في قسم **التدرجات الهرمية المعينة‬**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="c70e7-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c70e7-124">In the list, mark the selected row.</span></span> <span data-ttu-id="c70e7-125">ابحث عن التدرج الهرمي الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="c70e7-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="c70e7-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-126">Select **OK**.</span></span>

<span data-ttu-id="c70e7-127">تعرض الصورة التالية مثالاً لتدرد هرمي للمؤسسات تم إنشاؤها لمجموعة متاجر "Adventure Works".</span><span class="sxs-lookup"><span data-stu-id="c70e7-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![مثال لتدرج هرمي للمؤسسات](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="c70e7-129">إضافة مؤسسات إلى تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="c70e7-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="c70e7-130">لإضافة مؤسسات إلى تدرج هرمي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c70e7-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c70e7-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c70e7-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="c70e7-132">قم بتحديد التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="c70e7-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="c70e7-133">في جزء الإجراءات، حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="c70e7-134">قم بإضافة المؤسسات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="c70e7-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="c70e7-135">لإضافة مؤسسة، حدد **تحرير** ثم حدد **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="c70e7-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="c70e7-136">عند الانتهاء من إجراء التغييرات، يمكنك حفظ مسودة ونشر التغييرات.</span><span class="sxs-lookup"><span data-stu-id="c70e7-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="c70e7-137">تعرض الصورة التالية كيانًا قانونيًا تمت إضافته إلى جذر التدرج الهرمي مع أربع مراكز تكلفة مضافة لقنوات "مركز التسوق" و "المنفذ" و "عبر الإنترنت" و "مركز الاتصال".</span><span class="sxs-lookup"><span data-stu-id="c70e7-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="c70e7-138">بعد ذلك، يمكن إضافة مركز اتصال وقنوات عبر الإنترنت لكل واحد منها.</span><span class="sxs-lookup"><span data-stu-id="c70e7-138">Various retail, call center and online channels can then be added to each.</span></span>

![مثال لمصمم التدرج الهرمي](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="c70e7-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c70e7-140">Additional resources</span></span>

[<span data-ttu-id="c70e7-141">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c70e7-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c70e7-142">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c70e7-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c70e7-143">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="c70e7-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c70e7-144">إنشاء وحدات تشغيل</span><span class="sxs-lookup"><span data-stu-id="c70e7-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c70e7-145">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="c70e7-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c70e7-146">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="c70e7-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
